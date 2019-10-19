TOPIC: Safe
AUTHORS: Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Steve Hart; steve@stevehart.net; github:stevehartdata
         Teoli; teoli@mozilla.net; mdn:teoli

# Safe

An HTTP method is **safe** if it doesn't alter the state of the server. In other words,
a method is safe if it leads to a read-only operation. Several common HTTP methods are
safe: `GET`, `HEAD`, or `OPTIONS`. All safe methods are also
idempotent as well as some, but not all, unsafe methods like `PUT`, or `DELETE`.

Even if safe methods have a read-only semantic, servers can alter their state: e.g. they
can log or keep statistics. What is important here is that by calling a safe method, the
client doesn't request any server change itself, and therefore won't create an
unnecessary load or burden for the server. Browsers can call safe methods without
fearing to cause any harm to the server: this allows them to perform activities like
pre-fetching without risk. Web crawlers also rely on calling safe methods.

Safe methods don't need to serve static files only; a server can generate an answer to a
safe method on-the-fly, as long as the generating script guarantees safety: it should
not trigger external effects, like triggering an order in an e-commerce Web site.

It is the responsibility of the application on the server to implement the safe semantic
correctly, the web server itself, being Apache, nginx or IIS, can't enforce it by
itself. In particular, an application should not allow `GET` requests to alter
its state.

A call to a safe method, not changing the state for the server:

```http
GET /pageX.html HTTP/1.1
```

A call to a non-safe method, that may change the state of the server:

```http
POST /pageX.html HTTP/1.1
```

A call to an idempotent but non-safe method:

```http
DELETE /idX/delete HTTP/1.1
```

## Learn More

### General Knowledge

- Definition of [safe](https://tools.ietf.org/html/rfc7231#section-4.2.1) in the HTTP specification.

### Technical knowledge

- Description of common safe methods: [`GET`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/GET),
[`HEAD`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/HEAD),
[`OPTIONS`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/OPTIONS)
- Description of common unsafe methods: [`PUT`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PUT),
[`DELETE`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/DELETE),
[`POST`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Methods/POST)
