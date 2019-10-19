TOPIC: Simple Response Header
AUTHORS: Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Teoli; teoli@mozilla.net; mdn:teoli

# Simple Response Header

A simple response header (or a CORS-safelisted response header) is an HTTP header
which has been safelisted so that it will not be filtered when responses are processed
by CORS, since they're considered safe (as the headers listed in
`Access-Control-Expose-Headers`). By default, the safelist includes the following response headers:

- `Cache-Control`
- `Content-Language`
- `Content-Type`
- `Expires`
- `Last-Modified`
- `Pragma`

## Examples

### Extending the safelist

You can extend the list of CORS-safelisted response headers by using the
`Access-Control-Expose-Headers` header:

```http
Access-Control-Expose-Headers: X-Custom-Header, Content-Length
```
