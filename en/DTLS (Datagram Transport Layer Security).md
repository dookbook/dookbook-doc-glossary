TOPIC: DTLS (Datagram Transport Layer Security)
AUTHORS: Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy

# DTLS (Datagram Transport Layer Security)

**Datagram Transport Layer Security** (**DTLS**) is a protocol used to secure
datagram-based communications. It's based on the stream-focused Transport Layer Security (TLS),
providing a similar level of security. As a datagram protocol, DTLS doesn't guarantee the
order of message delivery, or even that messages will be delivered at all. However, DTLS gains the
benefits of datagram protocols, too; in particular, the lower overhead and reduced latency.

These features are especially useful for one of the most common arenas in which DTLS comes into
play: WebRTC. All of the WebRTC related protocols are required to encrypt their
communications using DTLS; this includes SCTP, SRTP, and STUN.

## Learn More

### General Knowledge

- [Datagram Transport Layer Security](https://en.wikipedia.org/wiki/Datagram%20Transport%20Layer%20Security)
on Wikipedia

### Specifications

- [RFC 6347: Datagram Transport Layer Security Version 1.2](https://tools.ietf.org/html/rfc6347)
- [Datagram Transport Layer Security Protocol Version 1.3 draft specification](https://tools.ietf.org/html/draft-ietf-tls-dtls13)

### Related Specifications

- [RFC 5763: Framework for Establishing a Secure Real-time Transport Protocol (SRTP) Security Context Using DTLS](https://tools.ietf.org/html/rfc5763)
- [RFC 5764: DTLS Extension to Establish Keys for the Secure Real-time Transport Protocol (SRTP)](https://tools.ietf.org/html/rfc5764)
- [RFC 6083: DTLS for Stream Control Transmission Protocol (SCTP)](https://tools.ietf.org/html/rfc6083)
- [RFC 8261: Datagram Transport Layer Security (DTLS) Encapsulation of SCTP Packets](https://tools.ietf.org/html/rfc8261)
- [RFC 7350: Datagram Transport Layer Security (DTLS) as Transport for Session Traversal Utilities for NAT (STUN)](https://tools.ietf.org/html/rfc7350)
- [RFC 7925: TLS / DTLS Profiles for the Internet of Things](https://tools.ietf.org/html/rfc7925)
