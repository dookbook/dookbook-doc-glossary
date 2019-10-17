TOPIC: CORS-safelisted Request Header
AUTHORS: Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Anne van Kesteren; annevk@annevk.nl; github:annevk

# CORS-safelisted Request Header

A [CORS-safelisted request header](https://fetch.spec.whatwg.org/#cors-safelisted-request-header) is
one of the following HTTP headers:

- `Accept`,
- `Accept-Language`,
- `Content-Language`,
- `Content-Type`.

When containing only these headers (and values that meet the additional requirements laid out below),
a requests doesn't need to send a preflight request in the context of CORS.

You can safelist more headers using the `Access-Control-Allow-Headers` header and also list the above
headers there to circumvent the following additional restrictions:

## Additional Restrictions

CORS-safelisted headers must also fulfill the following requirements in order to be a CORS-safelisted
request header:

- For `Accept-Language` and `Content-Language`: can only have values consisting of `0-9`, `A-Z`, `a-z`,
space or `*,=.;=`.
- For `Accept` and `Content-Type`: can't contain a CORS-unsafe request header byte: `"():<>?@[\]{}, Delete`,
Tab and control characters: 0x00 to 0x19.
- For `Content-Type`: needs to have a MIME type of its parsed value (ignoring parameters) of either
`application/x-www-form-urlencoded`, `multipart/form-data`, or `text/plain`.
- For any header: the value’s length can't be greater than 128.

## Learn More

- CORS-safelisted response header
- Forbidden header name
- Request header
