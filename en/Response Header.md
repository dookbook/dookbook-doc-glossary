TOPIC: Response Header
AUTHORS: Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Teoli; teoli@mozilla.net; mdn:teoli

# Response Header

A **response header** is an HTTP header that can be used in an HTTP response and that
doesn't relate to the content of the message. Response headers, like `Age`,
`Location` or `Server` are used to give a more detailed context of the response.

Not all headers appearing in a response are response headers. For example, the
`Content-Length` header is an entity header referring to the size of the body of
the response message. However, these entity requests are usually called responses headers in such a context.

The following shows a few response headers after a `GET` request. Note that
strictly speaking, the `Content-Encoding` and `Content-Type` headers are entity header:

```http
200 OK
Access-Control-Allow-Origin: *
Connection: Keep-Alive
Content-Encoding: gzip
Content-Type: text/html; charset=utf-8
Date: Mon, 18 Jul 2016 16:06:00 GMT
Etag: "c561c68d0ba92bbeb8b0f612a9199f722e3a621a"
Keep-Alive: timeout=5, max=997
Last-Modified: Mon, 18 Jul 2016 02:36:04 GMT
Server: Apache
Set-Cookie: mykey=myvalue; expires=Mon, 17-Jul-2017 16:06:00 GMT; Max-Age=31449600; Path=/; secure
Transfer-Encoding: chunked
Vary: Cookie, Accept-Encoding
X-Backend-Server: developer2.webapp.scl3.mozilla.com
X-Cache-Info: not cacheable; meta data too large
X-kuma-revision: 1085259
x-frame-options: DENY
```

## Learn More

### Technical knowledge

- [List of all HTTP headers](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers)
