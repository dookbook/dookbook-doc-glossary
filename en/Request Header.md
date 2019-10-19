TOPIC: Request Header
AUTHORS: Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Teoli; teoli@mozilla.net; mdn:teoli

# Request Header

A **request header** is an HTTP header that can be used in an HTTP request, and that
doesn't relate to the content of the message. Request headers, like `Accept`,
`Accept-*`, or `If-*` allow to perform conditional requests; others like
`Cookie`, `User-Agent` or `Referer` precise the context so that the
server can tailor the answer.

Not all headers appearing in a request are request headers. For example, the
`Content-Length` appearing in a `POST` request is actually an entity
header referring to the size of the body of the request message. However, these entity
headers are often called request headers in such a context.

In addition, `CORS` defines a subset of request headers as simple headers,
request headers that are always considered authorized and are not explicitly listed in
responses to preflight requests.

A few request headers after a `GET` request:

```http
GET /home.html HTTP/1.1
Host: developer.mozilla.org
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.9; rv:50.0) Gecko/20100101 Firefox/50.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br
Referer: https://developer.mozilla.org/testpage.html
Connection: keep-alive
Upgrade-Insecure-Requests: 1
If-Modified-Since: Mon, 18 Jul 2016 02:36:04 GMT
If-None-Match: "c561c68d0ba92bbeb8b0fff2a9199f722e3a621a"
Cache-Control: max-age=0
```

Strictly speaking, the `Content-Length` header in this example is not a request
header like the others, but an entity header:

```http
POST /myform.html HTTP/1.1
Host: developer.mozilla.org
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.9; rv:50.0) Gecko/20100101 Firefox/50.0
Content-Length: 128
```

## Learn More

### Technical knowledge

- [List of all HTTP headers](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers)
