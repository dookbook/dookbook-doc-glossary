TOPIC: Fetch Directive
AUTHORS: Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz

# Fetch Directive

**CSP fetch directives** are used in a `Content-Security-Policy` header and control locations
from which certain resource types may be loaded. For instance, `script-src` allows developers
to allow trusted sources of script to execute on a page,
while `font-src` controls the sources of web fonts.

All fetch directives fall back to `default-src`. That means, if a fetch directive is absent
in the CSP header, the user agent will look for the `default-src` directive.

These CSP directives are fetch directives:

[`child-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/child-src)
:   Defines the valid sources for [web workers](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API)
    and nested browsing contexts loaded using elements such as [`<frame>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/frame)
    and[`<iframe>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe).
!!! error "Don't try this at home"
    Instead of `child-src`, authors who wish to regulate nested browsing contexts and workers should
    use the [`frame-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/frame-src)
    and [`worker-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/worker-src)
    directives, respectively.

[`connect-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/connect-src)
:   Restricts the URLs which can be loaded using script interfaces

[`default-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/default-src)
:   Serves as a fallback for the other fetch directives.

[`font-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/font-src)
:   Specifies valid sources for fonts loaded using [`@font-face`](https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face).

[`frame-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/frame-src)
:   Specifies valid sources for nested browsing contexts loading using elements such as
    [`<frame>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/frame)
    and [`<iframe>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe).

[`img-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/img-src)
:   Specifies valid sources of images and favicons.

[`manifest-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/manifest-src)
:   Specifies valid sources of application manifest files.

[`media-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/media-src)
:   Specifies valid sources for loading media using the
    [`<audio>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio),
    [`<video>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video)
    and [`<track>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/track) elements.

[`object-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/object-src)
:   Specifies valid sources for the [`<object>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/object),
    [`<embed>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/embed),
    and [`<applet>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/applet) elements.
!!! node
Elements controlled by `object-src` are perhaps coincidentally considered legacy HTML elements and
are not recieving new standardized features (such as the security attributes `sandbox` or `allow`
for `<iframe>`). Therefore it is **recommended** to restrict this fetch-directive
(e.g. explicitly set `object-src 'none'` if possible).

[`prefetch-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/prefetch-src)
:   Specifies valid sources to be prefetched or prerendered.

[`script-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/script-src)
:   Specifies valid sources for JavaScript.

[`script-src-elem`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/script-src-elem)
:   Specifies valid sources for JavaScript [`<script>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script)
    elements.

[`script-src-attr`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/script-src-attr)
:   Specifies valid sources for JavaScript inline event handlers.

[`style-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/style-src)
:   Specifies valid sources for stylesheets.

[`style-src-elem`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/style-src-elem)
:   Specifies valid sources for stylesheets [`<style>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/style)
    elements and [`<link>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link)
    elements with rel="stylesheet".

[`style-src-attr`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/style-src-attr)
:   Specifies valid sources for inline styles applied to individual DOM elements.

[`worker-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/worker-src)
:   Specifies valid sources for [`Worker`](https://developer.mozilla.org/en-US/docs/Web/API/Worker),
[`SharedWorker`](https://developer.mozilla.org/en-US/docs/Web/API/SharedWorker),
or [`ServiceWorker`](https://developer.mozilla.org/en-US/docs/Web/API/ServiceWorker) scripts.
