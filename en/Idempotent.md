TOPIC: Idempotent
AUTHORS: Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Teoli; teoli@mozilla.net; mdn:teoli

# Idempotent

An HTTP method is **idempotent if** an identical request can be made once or several times in a row
with the same effect while leaving the server in the same state. In other words, an idempotent method
should not have any side-effects (except for keeping statistics). Implemented correctly, the
`GET`, `HEAD`, `PUT`, and `DELETE` method are **idempotent**, but not the
`POST` method. All safe methods are also idempotent.

To be idempotent, only the actual back-end state of the server is considered, the status code
returned by each request may differ: the first call of a `DELETE` will likely return a
`200`, while successive ones will likely return a `404`. Another implication of
`DELETE` being idempotent is that developers should not implement RESTful APIs with a delete
last entry functionality using the `DELETE` method.

Note that the idempotence of a method is not guaranteed by the server and some applications may
incorrectly break the idempotence constraint.

`GET /pageX HTTP/1.1` is idempotent. Called several times in a row, the client gets the same results:

```http
GET /pageX HTTP/1.1
GET /pageX HTTP/1.1
GET /pageX HTTP/1.1
GET /pageX HTTP/1.1
```

`POST /add_row HTTP/1.1` is not idempotent; if it is called several times, it adds several rows:

```http
POST /add_row HTTP/1.1
POST /add_row HTTP/1.1   -> Adds a 2nd row
POST /add_row HTTP/1.1   -> Adds a 3rd row
```

`DELETE /idX/delete HTTP/1.1` is idempotent, even if the returned status code may change between requests:

```http
DELETE /idX/delete HTTP/1.1   -> Returns 200 if idX exists
DELETE /idX/delete HTTP/1.1   -> Returns 404 as it just got deleted
DELETE /idX/delete HTTP/1.1   -> Returns 404
```

## Learn More

### General Knowledge

- Definition of [idempotent](https://tools.ietf.org/html/rfc7231#section-4.2.2) in the HTTP specification.

### Technical knowledge

- Description of common idempotent methods: [`GET`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/GET),
[`HEAD`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/HEAD),
[`PUT`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PUT),
[`DELETE`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/DELETE),
[`OPTIONS`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/OPTIONS),
[`TRACE`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/TRACE)
- Description of common non-idempotent methods: [`POST`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/POST),
[`PATCH`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PATCH),
[`CONNECT`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/CONNECT)
