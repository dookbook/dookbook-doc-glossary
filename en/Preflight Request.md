TOPIC: Preflight Request
AUTHORS: Garry Shutler; garry@robustsoftware.co.uk; github:gshutler
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         David Ross; bunnybooboo@github.com; github:bunnybooboo
         Gabriel Delépine; GabrielDelepine@github.com; github:GabrielDelepine
         Teoli; teoli@mozilla.net; mdn:teoli
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz

# Preflight Request

A CORS preflight request is a CORS request that checks to see if the CORS protocol is understood.

It is an `OPTIONS` request, using three HTTP request headers:
`Access-Control-Request-Method`, `Access-Control-Request-Headers`, and the
`Origin` header.

A preflight request is automatically issued by a browser, when needed. In normal cases,
front-end developers don't need to craft such requests themselves.

For example, a client might be asking a server if it would allow a `DELETE`
request, before sending a `DELETE` request, by using a preflight request:

```http
OPTIONS /resource/foo
Access-Control-Request-Method: DELETE
Access-Control-Request-Headers: origin, x-requested-with
Origin: https://foo.bar.org
```

If the server allows it, then it will respond to the preflight request with an
`Access-Control-Allow-Methods` response header, which lists `DELETE`:

```http
HTTP/1.1 204 No Content
Connection: keep-alive
Access-Control-Allow-Origin: https://foo.bar.org
Access-Control-Allow-Methods: POST, GET, OPTIONS, DELETE
Access-Control-Max-Age: 86400
```

## See Also

- [CORS](https://wiki.developer.mozilla.org/en-US/docs/Glossary/CORS)
- [`OPTIONS`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/OPTIONS)
