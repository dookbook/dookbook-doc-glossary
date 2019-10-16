TOPIC: ALPN
AUTHORS: Dustin Younse; milsyobtaf@github.com; github:milsyobtaf
         ExE Boss; ExE-Boss@github.com; github:ExE-Boss

# ALPN

**Application-Layer Protocol Negotiation (ALPN)** is a TLS extension which indicates what application
layer protocol is negotiating the encryped connection without requiring additional round trips.

**Important protocol identifiers:**

| Protocol | Identification sequence |
|--|--|
| HTTP/1.1 | 0x68 0x74 0x74 0x70 0x2F 0x31 0x2E 0x31 ("http/1.1") |
| HTTP/2 | 0x68 0x32 ("h2") |
| HTTP/2 over cleartext TCP | 0x68 0x32 0x63 ("h2c") |

## Specifications

| Specification | Status | Notes |
|--|--|--|
| [RFC 7301](https://tools.ietf.org/html/rfc7301) | IETF RFC | Initial definition. |

## See also

- [IANA registered ALPN identifiers](https://www.iana.org/assignments/tls-extensiontype-values/tls-extensiontype-values.xhtml#alpn-protocol-ids)
