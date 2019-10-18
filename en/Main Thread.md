TOPIC: Main Thread
AUTHORS: Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Andy Stevens; andystevensname@github.com; github:andystevensname

# Main Thread

The **main thread** is where a browser processes user events and paints. By default, the browser
uses a single thread to run all the JavaScript in your page, as well as to perform layout, reflows,
and garbage collection. This means that long-running JavaScript functions can block the thread,
leading to an unresponsive page and a bad user experience.

Unless intentionally using a web worker, such as a service worker, JavaScript runs on
the main thread, so it's easy for a script to cause delays in event processing or painting.
The less work required of the main thread, the more that thread can respond to user events, paint,
and generally be responsive to the user.