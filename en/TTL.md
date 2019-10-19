TOPIC: TTL
AUTHORS: David Ross; bunnybooboo@github.com; github:bunnybooboo

# TTL

TTL can refer either to :

- the lifetime of a packet in a network can do before being released
- the expiry time of cached data

## Networking

In networking, the TTL, embedded in the packet, is a usually defined as a number of hops or as an
expiration timestamp after which the packet is dropped. It provides a way to avoids network
congestion, but releasing packets after they roamed the network too long.

## Caching

In the context of caching, TTL (as an unsigned 32-bit integer) being a part of the HTTP response
header or the DNS query, indicates the amount of time in seconds during which the ressource
can be cached by the requester.

## Learn More

### General Knowledge

- [TTL](https://en.wikipedia.org/wiki/Time%20to%20live) on Wikipedia

### Technical Reference

- [RFC 2181](https://tools.ietf.org/html/rfc2181#section-8) on IETF
- [RFC 1035](https://tools.ietf.org/html/rfc1035) on IETF
