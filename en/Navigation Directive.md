TOPIC: Navigation Directive
AUTHORS: Elie Saad; ThunderSon@github.com; github:ThunderSon
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz

# Navigation Directive

**CSP navigation directives** are used in a `Content-Security-Policy` header and govern to
which location a user can navigate to or submit a form to, for example.

Navigation directives don't fall back to the `default-src` directive.

These CSP directives are navigation directives:

- `form-action`
- `frame-ancestors`
- `navigate-to`

## Learn More

### General Knowledge

- [https://www.w3.org/TR/CSP/#directives-navigation](https://www.w3.org/TR/CSP/#directives-navigation)
- Other kinds of directives:
  - Fetch directive
  - Document directive
  - Reporting directive
  - [`upgrade-insecure-requests`](https://wiki.developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy/block-all-mixed-content)
  - [`block-all-mixed-content`](https://wiki.developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy/upgrade-insecure-requests)
  - [`require-sri-for`](https://wiki.developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy/require-sri-for)
  - [`trusted-types`](https://wiki.developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy/trusted-types)
- [`Content-Security-Policy`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy)
