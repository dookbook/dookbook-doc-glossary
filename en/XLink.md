TOPIC: XLink
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Rolfe Dlugy-Hegwer; rolfedh@github.com; github:rolfedh
         Teoli; teoli@mozilla.net; mdn:teoli

# XLink

XLink is a W3C standard which is used to describe links between XML and XML or other documents.
Some its behaviors are left to the implementation to determine how to handle.

Simple XLinks are "supported" in Firefox (at least in SVG and MathML), though they do not work as
links if one loads a plain XML document with XLinks and attempts to click on the
relevant points in the XML tree.

For those who may have found XLink 1.0 cumbersome for regular links, XLink 1.1 drops the need to
specify `xlink:type="simple"` for simple links.

XLink is used in SVG, MathML, and other important standards.

## Specification

- [XLink 1.0](http://www.w3.org/TR/xlink/)
- [XLink 1.1](http://www.w3.org/TR/xlink11/) (currently a Working Draft)

## See Also

- [XML in Mozilla](https://wiki.developer.mozilla.org/en/XML_in_Mozilla)
- [Code snippets:getAttributeNS](https://wiki.developer.mozilla.org/en/Code_snippets/getAttributeNS)
- a wrapper for dealing with some browsers not
supporting this DOM method
- [Code `snippets:xml:base` function](https://wiki.developer.mozilla.org/en/Code_snippets/xml/base_function)
- a rough attempt to find a full XLink-based on an
xlink:href attribute (or `<xi:include href=>`) and its or an ancestor's `xml:base`.
