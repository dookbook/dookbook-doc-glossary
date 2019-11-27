TOPICS: HyperText Transfer Protocol

# HyperText Transfer Protocol (HTTP)

The **HyperText Transfer Protocol** (**HTTP**) is the underlying network protocol that enables transfer
of hypermedia documents on the Web, typically between a [browser](/en/glossary/Web_browser) and a
server so that humans can read them. The current version of the HTTP specification is called *HTTP/2*.

As part of a [[URI]], the `"http://"` is called "*schema*" and usually stands at the beginning of an
address, for instance in "[https://dookbook.info](https://dookbook.info)" to indicate to
the browser to request the document using the *HTTP* protocol. The `https` in this case refers to the
secure version of the HTTP protocol, *SSL* (also called *TLS*).

HTTP is **textual** (all communication is done in plain text) and **stateless** (no communication is
aware of previous communications). This property makes it ideal for humans to read documents (Web sites)
on the [[World Wide Web]]. However, HTTP can also be used as a basis for *REST* web services from
server to server or *[[AJAX]]* requests within web sites to make them more dynamic.

The default **port** used by HTTP is `80` (HTTPS uses `443` by default).

## HTTPS

**HTTPS** (*HTTP Secure*) is an *encrypted* version of the HTTP protocol. It usually uses
**SSL** or **TLS** to encrypt all communication between a client and a server. This secure
connection allows clients to safely exchange sensitive data with a server, for example for banking
activities or online shopping.

## HTTP/2

**HTTP/2** is a major revision of the HTTP network protocol. The primary goals for HTTP/2 are to
*reduce latency* by **enabling full request and response multiplexing**, *minimize protocol
overhead* via **efficient compression of HTTP header fields**, and add support for
**request prioritization** and **server push**.

HTTP/2 does not modify the application semantics of HTTP in any way. All the core concepts found in
*HTTP 1.1*, such as HTTP methods, status codes, [[URI]]s, and header fields, remain in place.
Instead, HTTP/2 modifies how the data is formatted (*framed*) and *transported* between the client and
server, both of which manage the entire process, and hides application complexity within the new
framing layer. As a result, all existing applications can be delivered without modification.

## Learn More

- [HTTP](https://en.wikipedia.org/wiki/Hypertext%20Transfer%20Protocol) on Wikipedia
- [HTTPS](https://en.wikipedia.org/wiki/HTTPS) on Wikipedia
- [RFC 2616 on HTTP/1.1](https://tools.ietf.org/html/rfc2616 "Hypertext Transfer Protocol -- HTTP/1.1")
- [HTTP on MDN](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP)
- [Moving to HTTPS community guide](https://movingtohttps.com/)
- [Secure Contexts](https://wiki.developer.mozilla.org/en-US/docs/Web/Security/Secure_Contexts)
