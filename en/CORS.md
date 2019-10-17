TOPIC: CORS
AUTHORS: Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Dan Dascalescu; ddascalescu+github@gmail.com; github:dandv
         Teoli; teoli@mozilla.net; mdn:teoli
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         danielle vincent; dvincent@mozilla.net; mdn:dvincent
         Julia Buchner; PetiPandaRou@mozilla.net; mdn:PetiPandaRou
         Federico Culloca; federicoculloca@github.com; github:federicoculloca

# CORS

**CORS** (Cross-Origin Resource Sharing) is a system, consisting of transmitting HTTP headers,
that determines whether browsers block frontend JavaScript code from accessing responses
for cross-origin requests.

The same-origin security policy forbids cross-origin access to resources. But CORS gives web
servers the ability to say they want to opt into allowing cross-origin access to their resources.

## Learn More

### General Knowledge

- [Cross-Origin Resource Sharing (CORS)](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
on MDN
- [Cross-origin resource sharing](https://en.wikipedia.org/wiki/Cross-origin%20resource%20sharing)
on Wikipedia

### CORS Headers

[`Access-Control-Allow-Origin`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Allow-Origin)

Indicates whether the response can be shared.

[`Access-Control-Allow-Credentials`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Allow-Credentials)

Indicates whether or not the response to the request can be exposed when the credentials flag is true.

[`Access-Control-Allow-Headers`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Allow-Headers)

Used in response to a preflight request to indicate which HTTP headers can be used when making
the actual request.

[`Access-Control-Allow-Methods`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Allow-Methods)

Specifies the method or methods allowed when accessing the resource in response to a preflight request.

[`Access-Control-Expose-Headers`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Expose-Headers)

Indicates which headers can be exposed as part of the response by listing their names.

[`Access-Control-Max-Age`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Max-Age)

Indicates how long the results of a preflight request can be cached.

[`Access-Control-Request-Headers`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Request-Headers)

Used when issuing a preflight request to let the server know which HTTP headers will be used when
the actual request is made.

[`Access-Control-Request-Method`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Request-Method)

Used when issuing a preflight request to let the server know which HTTP method will be used when the
actual request is made.

[`Origin`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Origin)

Indicates where a fetch originates from.

### Technical Reference

- [Fetch specification](https://fetch.spec.whatwg.org/)
