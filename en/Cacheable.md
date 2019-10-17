TOPIC: Cacheable
AUTHORS: Ryan Grove; yaypie@mozilla.net; mdn:yaypie
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Teoli; teoli@mozilla.net; mdn:teoli

# Cacheable

A **cacheable** response is an HTTP response that can be cached, that is stored to be retrieved and
used later, saving a new request to the server. Not all HTTP responses can be cached, there are the
following constraints for an HTTP response to be cached:

- The method used in the request is itself cacheable, that is either a GET or a HEAD method.
A response to a POST or PATCH request can also be cached if freshness is indicated and the
Content-Location header is set, but this is rarely implemented. (For example, Firefox does not
support it per [https://bugzilla.mozilla.org/show_bug.cgi?id=109553](https://bugzilla.mozilla.org/show_bug.cgi?id=109553).)
Other methods, like PUT or DELETE are not cacheable and their result cannot be cached.
  
- The status code of the response is known by the application caching, and it is considered cacheable.
The following status code are cacheable: `200`, `203`, `204`, `206`,
`300`, `301`, `404`], `405`, `410`, `414`, and `501`.
  
- There is no specific headers in the response, like `Cache-Control`, that prevents caching.

Note that some non-cacheable requests/responses to a specific URI may invalidate previously cached
responses on the same URI. For example, a `PUT` to pageX.html will invalidate all cached
`GET` or `HEAD` requests to the same URI.

When both, the method of the request and the status of the response, are cacheable,
the response to the request can be cached:

```http
GET /pageX.html HTTP/1.1
(…)

200 OK
(…)
```

A `PUT` request cannot be cached. Moreover, it invalidates cached data for request to the
same URI done via `HEAD` or `GET`:

```http
PUT /pageX.html HTTP/1.1
(…)

200 OK
(…)
```

A specific `Cache-Control` header in the response can prevent caching:

```http
GET /pageX.html HTTP/1.1
(…)

200 OK
Cache-Control: no-cache
(…)
```

## Learn More

### General Knowledge

- Definition of [cacheable](https://tools.ietf.org/html/rfc7231#section-4.2.3) in the HTTP specification.

### Technical Knowledge

- Description of common cacheable methods: [`GET`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/GET),
[`HEAD`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/HEAD)
- Description of common non-cacheable methods: [`PUT`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PUT),
[`DELETE`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/DELETE),
often [`POST`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/POST)
