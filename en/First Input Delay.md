TOPIC: First Input Delay
AUTHORS: Dustin Younse; milsyobtaf@github.com; github:milsyobtaf

# First Input Delay

**First input delay** (FID) measures the time from when a user first interacts with your site
(i.e. when they click a link, tap on a button, or uses a custom, JavaScript-powered control) to the
time when the browser is actually able to respond to that interaction. It is the length of time,
in milliseconds, between the first user interaction on a web page and the browsers response to that
interaction. Scrolling and zooming are not included in this metric.

The time between when content is painted to the page and when all the functionality becomes
responsive to human interaction often varies based on the the size and complexity of the JavaScript
needing to be downloaded, parsed, and executed on the main thread, and on the device speed or lack
thereof (think low end mobile devices).  The longer the delay, the worse the user experience.
Reducing site initialization time and eliminating long tasks can help eliminate first input delays.

## See Also

- [RequestIdleCallback](https://wiki.developer.mozilla.org/en-US/docs/Web/API/Window/requestIdleCallback)
- [Lazy Loading](https://wiki.developer.mozilla.org/en-US/docs/Learn/Performance/Lazy_loading)
