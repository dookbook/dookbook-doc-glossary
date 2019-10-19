TOPIC: Reporting Directive
AUTHORS: Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz

# Reporting Directive

**CSP reporting directives** are used in a `Content-Security-Policy` header and
control the reporting process of CSP violations.

## List of CSP reporting directives

[`report-uri`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/report-uri)
:   Instructs the user agent to report attempts to violate the Content Security Policy. These violation
    reports consist of JSON documents sent via an HTTP POST request to the specified URI.
!!! error "Don't try this at home"
    Though the [`report-to`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/report-to)
    directive is intended to replace the deprecated `report-uri` directive, [`report-to`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/report-to)
    isn’t supported in most browsers yet. So for compatibility with current browsers while also adding
    forward compatibility when browsers get [`report-to`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/report-to)
    support, you can specify both `report-uri` and [`report-to`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/report-to):
     >Content-Security-Policy: ...; report-uri
     >`https://endpoint.example.com`; report-to groupname
     In browsers that support [`report-to`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/report-to),
     the `report-uri` directive will be ignored.

[`report-to`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/report-to)
:   Fires a `SecurityPolicyViolationEvent`.
