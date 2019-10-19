TOPIC: XHTML
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         ExE Boss; ExE-Boss@github.com; github:ExE-Boss
         Johan; JohanX@mozilla.net; mdn:JohanX
         Janet Swisher; jmswisher@github.com; github:jmswisher
         WOO JIN JEON; jeonnoej@mozilla.net; mdn:jeonnoej
         Teoli; teoli@mozilla.net; mdn:teoli
         khanh; khanh0w3n@mozilla.net; mdn:khanh0w3n
         Keiichi; ethertank@mozilla.net; mdn:ethertank
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Jesper Kristensen; Dikrib@mozilla.net; mdn:Dikrib
         Onur Avsar; avsaro@mozilla.net; mdn:avsaro
         Benoit; BenoitL@mozilla.net; mdn:BenoitL

# XHTML

HTML can travel over the network to a browser either in HTML syntax or an XML syntax called XHTML.

## HTML5 and HTML/XHTML

The HTML5 standard defines both these syntaxes.  The MIME type
(sent in the HTTP `Content-Type` header) indicates the choice of syntax: for XHTML the MIME
type will be  `application/xhtml+xml`, otherwise `text/html`.

This example shows an HTML document and an XHTML document including the appropriate HTTP headers:

### HTML document

```http
HTTP/1.1 200 OK
Content-Type: text/html

<!DOCTYPE html>
<html lang=en>
  <head>
    <meta charset=utf-8>
    <title>HTML</title>
  </head>
  <body>
    <p>I am a HTML document</p>
  </body>
</html>
```

### XHTML document

```http
HTTP/1.1 200 OK
Content-Type: application/xhtml+xml

<?xml version="1.0" encoding="UTF-8"?>
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en">
  <head>
    <title>XHTML</title>
  </head>
  <body>
    <p>I am a XHTML document</p>
  </body>
</html>
```

## MIME type versus DOCTYPE

Before HTML5, the two separate specifications defined the two syntaxes
([HTML 4.01 Specification](https://www.w3.org/TR/html401/) and [XHTML 1.0 specification](https://www.w3.org/TR/xhtml1)).
According to the XHTML1 standard,
you could use XHTML by declaring a special DOCTYPE. However, no browsers have ever implemented this,
and the HTML5 standard has reversed the decision.
**If your page is sent as `text/html`, you are not using XHTML**.

Instead, the proper MIME type must be present in the `Content-Type` HTTP header. If you only put the
MIME type into an HTML meta tag like `<meta http-equiv=…>`, it will be ignored and treated like `text/html`.

If you serve your pages as `text/html` and believe that you are writing XHTML, you may face several
problems, as described in these articles:

- [No to XHTML](http://www.spartanicus.utvinternet.ie/no-xhtml.htm) an excellent article from Spartanicus

- [Beware of XHTML](http://www.webdevout.net/articles/beware-of-xhtml) by David Hammond

- [Sending XHTML as text/html Considered Harmful](http://www.hixie.ch/advocacy/xhtml) by Ian Hickson

- [XHTML's Dirty Little Secret](http://www.xml.com/pub/a/2003/03/19/dive-into-xml.html) by Mark Pilgrim

- [XHTML - What's the Point?](http://hsivonen.iki.fi/xhtml-the-point/) by Henri Sivonen

- [XHTML is not for Beginners](http://lachy.id.au/log/2005/12/xhtml-beginners) by Lachlan Hunt

## Support

Most browsers currently support XHTML, including Firefox, Chrome, Safari, Opera, and Internet
Explorer (since IE 9). (Internet Explorer 8 and older browsers instead show a download dialog box for
unknown file types when they see an XHTML document with the correct XHTML MIME type.)

Also be aware that many popular JavaScript libraries and
developer tools have limited or no support for XHTML.

## Differences from HTML

See [Properly Using CSS and JavaScript in XHTML Documents](https://wiki.developer.mozilla.org/en-US/docs/Properly_Using_CSS_and_JavaScript_in_XHTML_Documents)
for a partial list of differences between HTML and XHTML.

## Tools

- [Standards-Compliant Authoring Tools](https://wiki.developer.mozilla.org/en-US/docs/Archive/Web/Standards-Compliant_Authoring_Tools)

## See Also

- [HTML](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML)
- [Namespaces](https://wiki.developer.mozilla.org/en-US/docs/Namespaces)

[View All...](https://wiki.developer.mozilla.org/en-US/docs/tag/XHTML)
