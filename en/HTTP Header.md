TOPIC: HTTP Header
AUTHORS: Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Teoli; teoli@mozilla.net; mdn:teoli

# HTTP Header

An **HTTP header** is a field of an HTTP request or response that passes additional information,
altering or precising the semantics of the message or of the body. Headers are case-insensitive,
begins at the start of a line and are immediately followed by a `':'` and a value depending of the
header itself. The value finish at the next CR or at the end of the message.

Traditionally, headers are classed in categories, though this classification is no more part of any specification:

- General header: Headers applying to both requests and responses but with no relation to the data
eventually transmitted in the body.

- Request header: Headers containing more information about the resource to be fetched or about the
client itself.

- Response header: Headers with additional information about the response, like its location or about
the server itself (name, version, …).

- Entity header: Headers containing more information about the body of the entity, like its content
length or its MIME-type.

A basic request with one header:

```http
GET /example.http HTTP/1.1
Host: example.com
```

Redirects have mandatory headers (`Location`):

```http
302 Found
Location: /NewPage.html
```

A typical set of headers:

```http
304 Not Modified
Access-Control-Allow-Origin: *
Age: 2318192
Cache-Control: public, max-age=315360000
Connection: keep-alive
Date: Mon, 18 Jul 2016 16:06:00 GMT
Server: Apache
Vary: Accept-Encoding
Via: 1.1 3dc30c7222755f86e824b93feb8b5b8c.cloudfront.net (CloudFront)
X-Amz-Cf-Id: TOl0FEm6uI4fgLdrKJx0Vao5hpkKGZULYN2TWD2gAWLtr7vlNjTvZw==
X-Backend-Server: developer6.webapp.scl3.mozilla.com
X-Cache: Hit from cloudfront
X-Cache-Info: cached
```
