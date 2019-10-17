TOPIC: Doctype
AUTHORS: Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Federico Culloca; federicoculloca@github.com; github:federicoculloca
         luke crouch; lcrouch@mozilla.com; github:groovecoder

# Doctype

In HTML, the doctype is the required "`<!DOCTYPE html>`" preamble found at the top of all documents.
Its sole purpose is to prevent a browser from switching into so-called “quirks mode” when
rendering a document; that is, the "`<!DOCTYPE html>`" doctype ensures that the browser makes a
best-effort attempt at following the relevant specifications, rather than using a different rendering
mode that is incompatible with some specifications.

## Learn More

### General Knowledge

- [Definition of the DOCTYPE in the HTML specification](https://html.spec.whatwg.org/multipage/syntax.html#the-doctype)
- [Quirks Mode and Standards Mode](https://wiki.developer.mozilla.org/en-US/docs/Quirks_Mode_and_Standards_Mode)

### Technical Reference

- [Document.doctype](https://wiki.developer.mozilla.org/en-US/docs/Web/API/Document/doctype),
a JavaScript method that returns the doctype
