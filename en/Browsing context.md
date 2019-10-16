TOPIC: Browsing context
AUTHORS: Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Teoli; teoli@mozilla.net; mdn:teoli

# Browsing context

A **browsing context** is the environment in which a browser displays a `Document` (normally
a tab nowadays, but possibly also a window or a frame within a page).

Each browsing context has a specific origin, the origin of the active document, and a history that
lists all the displayed documents in order.

Communication between browsing contexts is severely restricted. Between browsing context of the same
origin, a `BroadcastChannel` can be opened and used.

## Learn more

### Technical reference

- [browsing context on WHATWG](https://html.spec.whatwg.org/multipage/browsers.html#windows)
- [browsing context on W3C](http://w3c.github.io/html/browsers.html#sec-browsing-contexts)
