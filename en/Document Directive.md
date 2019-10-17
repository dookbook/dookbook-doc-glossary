TOPIC: Document Directive
AUTHORS: Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz

# Document Directive

CSP document directives are used in a `Content-Security-Policy` header and govern the properties of a
document or worker environment to which a policy applies.

Document directives don't fall back to the `default-src` directive.

## List of CSP document directives

[`base-uri`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/base-uri)

Restricts the URLs which can be used in a document's [`<base>`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/base)
element.

[`plugin-types`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/plugin-types)

Restricts the set of plugins that can be embedded into a document by limiting the types of
resources which can be loaded.

[`sandbox`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/sandbox)

Enables a sandbox for the requested resource similar to the [`<iframe>`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe)
[`sandbox`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#attr-sandbox) attribute.

[`disown-opener`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/disown-opener)

Ensures a resource will disown its opener when navigated to.
