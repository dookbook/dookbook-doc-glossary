TOPIC: Entity Header
AUTHORS: Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Teoli; teoli@mozilla.net; mdn:teoli

# Entity Header

An entity header is an HTTP header describing the content of the body of the message. Entity headers
are used in both, HTTP requests and responses. Headers like `Content-Length`,
`Content-Language`, `Content-Encoding` are entity headers.

Even if entity headers are neither request nor response headers, they are often included with these terms.

In the following example, Content-Length is an entity header,
while Host and User-Agent are request headers:

```http
POST /myform.html HTTP/1.1

Host: developer.mozilla.org
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.9; rv:50.0) Gecko/20100101 Firefox/50.0
Content-Length: 128
```

## Learn More

### Technical knowledge

- [List of all HTTP headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)
