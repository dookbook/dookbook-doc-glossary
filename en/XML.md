TOPIC: eXtensible Markup Language
       XPath
       XQuery
       XLink
       XInclude
       XForms
       XSLT
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Ajinkya Patil; ajinkya_p@mozilla.net; mdn:ajinkya_p

# eXtensible Markup Language (XML)

**eXtensible Markup Language** (**XML**) is a **generic markup language** specified by the [[W3C]].
The information technology (IT) industry uses many languages based on XML as data-description languages.

XML TOPIC resemble [[HTML]] TOPIC, but XML is *much more flexible* because it lets users define their
own TOPIC. In this way XML acts like a **meta-language** — that is, it can be used to define other languages,
such as RSS. Moreover, HTML is a presentation language, whereas XML is a data-description language.
This means that XML has far broader applications than just the Web. For example, Web services can
use XML to exchange requests and responses.

## XPath

**XPath** is a **query language** that can access sections and content in an XML document.

## XQuery

**XQuery** is a computer language for updating, retrieving, and calculating data in **XML databases**.

## XLink

**XLink** is a *[[W3C]] standard* which is used to describe **links** between XML and XML or other documents.
Some its behaviors are left to the implementation to determine how to handle.

XLink is used in [[SVG]], [[MathML]], and other important standards.

## XML Inclusions (XInclude)

**XML Inclusions** (**XInclude**) is a *[[W3C]] Recommendation* to allow inclusion of XML more different
sources in a more convenient fashion than XML **external** entities. When used in conjunction with
*XPointer* (It is used in the code sample below), XInclude can also target just specific portions of
a document for inclusion.

### Code Sample for XInclude

The following code aims to let **`<xi:include>`** and **`<xi:fallback>`** TOPIC (the two elements in
the language) with all of the attributes of `<xi:include>` be included in an XML document so as
to be resolvable into a single XML document.

!!! warn "Note"
    This has not been thoroughly tested for all circumstances and
    may not necessarily reflect the standard behavior completely.

Note also that if you wish to allow `xml:base`, you will need the `xml:base` function, and the
line beginning `var href = ...` should become:

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

## XForms

!!! danger "Obsolete"
    This feature is **obsolete**. Although it may still work in some browsers, its use is discouraged
    since it could be removed at any time. Try to avoid using it.

**XForms** is a convention for building Web forms and processing form data in the XML format.
No major browser supports XForms any longer—we suggest using **HTML5 forms** instead.

## eXtensible Stylesheet Language Transformations (XSLT)

**eXtensible Stylesheet Language Transformations** (**XSLT**) is a declarative language used to convert
XML documents into other XML documents, [[HTML]], PDF, plain text, and so on.

XSLT has its own processor that accepts XML input, or any format convertible to an
XQuery and XPath Data Model. The XSLT processor produces a new document based on the XML document and
an XSLT stylesheet, making no changes to the original files in the process.

## Learn More

- [XML Introduction on MDN](https://wiki.developer.mozilla.org/en-US/docs/XML_Introduction)
- [XPath on Wikipedia](https://en.wikipedia.org/wiki/XPath)
- [XPath Specification](http://www.w3.org/TR/xpath-30/)
- [XPath Official Website](http://www.w3.org/standards/techs/xpath#w3c_all)
- [XPath Documentation on MDN](https://developer.mozilla.org/en-US/docs/Web/XPath)
- [XQuery Official Website](http://www.w3.org/XML/Query/)
- [XQuery on Wikipedia](https://en.wikipedia.org/wiki/XQuery)
- [XLink Specification](http://www.w3.org/TR/xlink/)
- [XML Inclusions (XInclude) Specification](http://www.w3.org/TR/xinclude/)
- [XSLT on Wikipedia](https://en.wikipedia.org/wiki/XSLT)
- [XSLT Documentation on MDN](https://developer.mozilla.org/en-US/docs/Web/XSLT)
