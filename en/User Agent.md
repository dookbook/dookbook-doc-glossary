TOPIC: User Agent
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         ExE Boss; ExE-Boss@github.com; github:ExE-Boss
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Michiel Renty; mrenty@mozilla.net; mdn:mrenty
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone
         Saurabh / Jsx; jsx@mozilla.net; mdn:jsx

# User Agent

A user agent is a computer program representing a person, for example, a browser in a Web context.

Besides a browser, a user agent could be a bot scraping webpages, a download manager, or another app
accessing the Web. Along with each request they make to the server, browsers include a
self-identifying `User-Agent` HTTP header called a user agent (UA) string. This string often
identifies the browser, its version number, and its host operating system.

Spam bots, download managers, and some browsers often send a fake UA string to announce themselves
as a different client. This is known as user agent spoofing.

The user agent string can be accessed with JavaScript on the client side using the
`navigator.userAgent` property.

A typical user agent string looks like this:
`"Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:35.0) Gecko/20100101 Firefox/35.0"`.

## Learn More

### General Knowledge

- [User Agent](https://en.wikipedia.org/wiki/User%20agent) on Wikipedia

### Technical Reference

- [`navigator.userAgent`](https://wiki.developer.mozilla.org/en-US/docs/Web/API/Navigator/userAgent)
- [Browser detection using the user agent](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Browser_detection_using_the_user_agent)
- [RFC 2616: 14.43](https://tools.ietf.org/html/rfc2616): The `User-Agent` header
