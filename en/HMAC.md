TOPIC: HMAC
AUTHORS: David Ross; bunnybooboo@github.com; github:bunnybooboo

# HMAC

HMAC is a protocol used for cryptographically authenticating messages. It can use any kind of
cryptographic functions, and its strengh depends on the underlying function (SHA1 or MD5 for instance),
and the chosen secret key. With such a combination, the HMAC verification algorithm is then known
with a compound name such as HMAC-SHA1.

HMAC is used to ensure both integrity and authentication.

## Learn More

### General Knowledge

- [HMAC](https://en.wikipedia.org/wiki/Hash-based%20message%20authentication%20code) on Wikipedia

### Technical Reference

- [RFC 2104](http://www.ietf.org/rfc/rfc2104.txt) on IETF
