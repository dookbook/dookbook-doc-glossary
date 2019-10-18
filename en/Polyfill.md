TOPIC: Polyfill
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Sphinx; SphinxKnight@github.com; github:SphinxKnight
         Michiel Renty; mrenty@mozilla.net; mdn:mrenty

# Polyfill

A polyfill is a piece of code (usually JavaScript on the Web) used to provide modern functionality
on older browsers that do not natively support it.

For example a polyfill could be used to mimic the functionality of an HTML Canvas element on Microsoft
Internet Explorer 7 using a Silverlight plugin, or mimic support for CSS rem units, or `text-shadow`,
or whatever you want.

The reason for why polyfills are not used exclusively is for better functionality and better performance.
Native implementations of APIs can do more and are faster than polyfills. For example,
the Object.create polyfill only contains the functionalities that are possible in a non-native
implementation of Object.create.

Other times, polyfills are used to address issues where browsers implement the same features in
different ways. The polyfill uses non-standard features in a certain browser to give JavaScript a
standards-complaint way to access the feature. Although this reason for polyfilling is very rare today,
it was especially prevalent back in the days of IE6, Netscape, and NNav where each browser implemented
Javascript very differently. The [1st version of JQuery](https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.js)
was an early example of a polyfill. It was
essentially a compilation of browser-specific workarounds so that JavaScript developers could have a
single common API that worked in all browsers. At the time, JavaScript developers were grasping at
straws trying to get their website to work across all devices because there was such a discrepancy
between browsers that the website might have to be programmed radically differently and have a much
different user interface based upon the user's browser. Thus, the JavaScript developer had access to
only a very tiny handful of JavaScript APIs that worked more-or-less consistently across all browsers.
Using a polyfill to handle browser-specific implementations is practically non-existence today because
modern browsers mostly implement a broad set of APIs according to standard semantics.

## Learn More

### General Knowledge

- [What is a polyfill?](https://remysharp.com/2010/10/08/what-is-a-polyfill) (article by Remy Sharp,
originator of the term)
