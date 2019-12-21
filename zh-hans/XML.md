TOPIC: eXtensible Markup Language

# 可扩展标记语言 (XML)

**可扩展标记语言**（**XML**）是由[[W3C]]指定的一种**通用标记语言**。信息技术行业使用许多基于XML的语言作为数据描述性语言。

XML标签类似[[HTML]]标签，但由于XML允许用户定义他们自己的标签，所以XML*更加灵活*。从这个层面来看，XML表现的像一种**元语言** —— 也就是说，它可以被用来定义其他语言，例如RSS。
不仅如此，HTML是陈述性语言，而XML是数据描述性语言。这意味着XML除了Web之外有更远更广的应用。例如，Web服务可以利用XML去交换请求和响应。

## XPath

**XPath**是一种可以访问XML文件中的节和内容的**查询语言**。

## XQuery

**XQuery**是一门用于更新、检索以及计算**XML数据库**中数据的计算机语言。

## XLink

**XLink**是 *[[W3C]]标准*，用于描述XML与XML或其他文档之间的**链接**。 它的某些行为留给实现来确定如何处理。

XLink用于[[SVG]]，[[MathML]]和其他重要标准中。

## XML Inclusions (XInclude)

**XML包含**（**XInclude**）是一项 *[[W3C]]建议*，允许比XML**外部**实体更方便地包含XML。当与*XPointer*（在下面的代码示例中使用）结合使用时，XInclude还可以仅将文档的特定部分作为目标。

### XInclude代码样例

以下代码旨在使 **`<xi:include>`** 和 **`<xi:fallback>`**的两个元素具有所有`<xi:include>`的属性包含在XML文档中，以便可以解析为单个XML文档。

!!! warn "Note"
    尚未针对所有情况进行全面测试，并且不一定完全反映标准行为。

还请注意，如果您希望允许使用`xml:base`，则需要使用`xml:base`函数，并且以`var href = ...`开头的行应变为：

```javascript
var href = getXmlBaseLink (/* XLink sans xml:base */ xinclude.getAttribute('href'),
/* Element to query from */ xinclude);
```

```javascript
function resolveXIncludes(docu) {
  // http://www.w3.org/TR/xinclude/#xml-included-items
  var xincludes = docu.getElementsByTagNameNS('http://www.w3.org/2001/XInclude', 'include');
  if (xincludes) {
    for (i=0; i < xincludes.length; i++) {
      var xinclude = xincludes[i];
      var href = xinclude.getAttribute('href');
      var parse = xinclude.getAttribute('parse');
      var xpointer = xinclude.getAttribute('xpointer');
      var encoding = xinclude.getAttribute('encoding');
      /* e.g., UTF-8 // "text/xml or application/xml or matches text/*+xml or
application/*+xml" before encoding (then UTF-8) */
      var accept = xinclude.getAttribute('accept'); // header "Accept: "+x
      var acceptLanguage = xinclude.getAttribute('accept-language'); // "Accept-Language: "+x
      var xiFallback = xinclude.getElementsByTagNameNS('http://www.w3.org/2001/XInclude', 'fallback')[0];
      /* Only one such child is allowed */
      if (href === '' || href === null) {
        // Points to same document if empty (null is equivalent to empty string)
        href = null; // Set for uniformity in testing below
        if (parse === 'xml' && xpointer === null) {
          alert('There must be an XPointer attribute present if "href" is empty an parse is "xml"');
          return false;
        }
      }
      else if (href.match(/#$/, '') || href.match(/^#/, '')) {
        alert('Fragment identifiers are disallowed in an XInclude "href" attribute');
        return false;
      }
      var j;
      var xincludeParent = xinclude.parentNode;
      try {
        netscape.security.PrivilegeManager.enablePrivilege('UniversalXPConnect UniversalBrowserRead');
        // Necessary with file:///-located files trying to reach external sites
        if (href !== null) {
          var response, responseType;
          var request = new XMLHttpRequest();
          request.open('GET', href, false);
          request.setRequestHeader('If-Modified-Since', 'Thu, 1 Jan 1970 00:00:00 GMT');
          request.setRequestHeader('Cache-Control', 'no-cache');
          if (accept) {
            request.setRequestHeader('Accept', accept);
          }
          if (acceptLanguage) {
            request.setRequestHeader('Accept-Language', acceptLanguage);
          }
          switch (parse) {
            case 'text':
              // Priority should be on media type:

              var contentType = request.getResponseHeader('Content-Type');

              //text/xml; charset="utf-8" // Send to get headers first?
              /* Fix: We test for file extensions as well in case file:// doesn't return
content type (as seems to be the case); can some other tool be uesd in FF (or IE) to detect
encoding of local file? Probably just need BOM test since other encodings must be specified */
              var patternXML = /\.(svg|xml|xul|rdf|xhtml)$/;
              if ((contentType && contentType.match(/[text|application]\/(.*)\+?xml/)) ||
(href.indexOf('file://') === 0 && href.match(patternXML))) {
                /* Grab the response as text (see below for that routine) and then find encoding within*/
                var encName = '([A-Za-z][A-Za-z0-9._-]*)';
                var pattern = new RegExp('^<\\?xml\\s+.*encoding\\s*=\\s*([\'"])'+encName+'\\1.*\\?>');
                // Check document if not?
                // Let the request be processed below
              }
              else {
                if (encoding === '' || encoding === null) { // Encoding has no effect on XML
                  encoding = 'utf-8';
                }
                request.overrideMimeType('text/plain; charset='+encoding); //'x-user-defined'
              }
              responseType = 'responseText';
            break;
            case null:
            case 'xml':
              responseType = 'responseXML';
              break;
            default:
              alert('XInclude element contains an invalid "parse" attribute value');
              return false;
              break;
          }
          request.send(null);
          if((request.status === 200 || request.status === 0) && request[responseType] !== null){
            response = request[responseType];
            if (responseType === 'responseXML') {
              // apply xpointer (only xpath1() subset is supported)
              var responseNodes;

              if (xpointer) {
                var xpathResult = response.evaluate(
                  xpointer,
                  response,
                  null,
                  XPathResult.ORDERED_NODE_SNAPSHOT_TYPE,
                  null
                );
                var a = [];
                for(var k = 0; k < xpathResult.snapshotLength; k++) {
                  a[k] = xpathResult.snapshotItem(k);
                }
                responseNodes = a;
              }
              else { // Otherwise, the response must be a single well-formed document response
                responseNodes = [response.documentElement];
                // Put in array so can be treated the same way as the above
              }
              // PREPEND ANY NODE(S) (AS XML) THEN REMOVE XINCLUDE
              for (j=0; j < responseNodes.length ; j++) {
                xincludeParent.insertBefore(responseNodes[j], xinclude);
              }
              xincludeParent.removeChild(xinclude);
            }
            else if (responseType === 'responseText') {
              if (encName) {
                var encodingType = response.match(pattern);
                if (encodingType) {
                  encodingType = encodingType[2];
                }
                else {
                  encodingType = 'utf-8';
                }
                /* Need to make a whole new request apparently
since cannot convert the encoding after receiving it (to know what the encoding was)*/
                var request2 = new XMLHttpRequest();
                request2.overrideMimeType('text/plain; charset='+encodingType);
                request2.open('GET', href, false);
                request2.setRequestHeader('If-Modified-Since', 'Thu, 1 Jan 1970 00:00:00 GMT');
                request2.setRequestHeader('Cache-Control', 'no-cache');
                request2.send(null);
                response = request2[responseType]; // Update the response for processing
              }

              // REPLACE XINCLUDE WITH THE RESPONSE AS TEXT
              var textNode = docu.createTextNode(response);
              xincludeParent.replaceChild(textNode, xinclude);
            }

            // replace xinclude in doc with response now (as plain text or XML)
          }
        }
      }
      catch (e) { // Use xi:fallback if XInclude retrieval above failed
        var xiFallbackChildren = xiFallback.childNodes;
        // PREPEND ANY NODE(S) THEN REMOVE XINCLUDE
        for (j=0; j < xiFallbackChildren.length ; j++) {
          xincludeParent.insertBefore(xiFallbackChildren[j], xinclude);
        }
        xincludeParent.removeChild(xinclude);
      }
    }
  }
  return docu;
}
```

## 更多

- [XML简介 - MDN](https://wiki.developer.mozilla.org/en-US/docs/XML_Introduction)
- [XPath - 维基百科](https://en.wikipedia.org/wiki/XPath)
- [XPath规范](http://www.w3.org/TR/xpath-30/)
- [XPath官网](http://www.w3.org/standards/techs/xpath#w3c_all)
- [XPath文档 - MDN](https://developer.mozilla.org/en-US/docs/Web/XPath)
- [XQuery官网](http://www.w3.org/XML/Query/)
- [XQuery - 维基百科](https://en.wikipedia.org/wiki/XQuery)
- [XLink规范](http://www.w3.org/TR/xlink/)
- [XML Inclusions (XInclude)规范](http://www.w3.org/TR/xinclude/)
