TOPICS: User Agent
        Web Browser

# User Agent

A user agent is a computer program representing a person, for example, a Web browser in a Web context.

Besides a browser, a user agent could be a bot scraping webpages, a download manager, or another app
accessing the Web.

Spam bots, download managers, and some browsers often send a *fake* UA string to announce themselves
as a different client. This is known as *user agent spoofing*.

A typical user agent string looks like this:
`"Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:35.0) Gecko/20100101 Firefox/35.0"`.

## Web Browser

The most familiar type of user agent is *Web browser*. A **Web browser** or **browser** is a program
that retrieves and displays pages from the [Web](/en/glossary/World_Wide_Web), and lets users access
further pages through **hyperlinks**.

Along with each request they make to the server, browsers include a
self-identifying `User-Agent` [HTTP](/en/glossary/HyperText_Transfer_Protocol) header called a
**user agent** (**UA**) string. This string often identifies the browser, its version number, and its
host operating system.

The user agent string can be accessed with [[JavaScript]] on the client side using the
`navigator.userAgent` property.

### Popular Browsers

- [Google Chrome](/en/glossary/Google_Chrome_Browser)
- [Mozilla Firefox](http://www.mozilla.org/en-US/firefox/)
- [Microsoft Edge](https://www.microsoft.com/windows/microsoft-edge)
- [Opera Browser](http://www.opera.com/)

## Learn More

### General Knowledge

- [User Agent](https://en.wikipedia.org/wiki/User%20agent) on Wikipedia

### Technical Reference

- [`navigator.userAgent`](https://wiki.developer.mozilla.org/en-US/docs/Web/API/Navigator/userAgent)
- [Browser detection using the user agent](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Browser_detection_using_the_user_agent)
- [RFC 2616: 14.43](https://tools.ietf.org/html/rfc2616): The `User-Agent` header
