TOPIC: Transport Layer Security (TLS)
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         April King; april@pokeinthe.io; github:april
         Sphinx; SphinxKnight@github.com; github:SphinxKnight
         diayan; diayansiat@gmail.com; github:diayan
         Tomisin; ToJen@github.com; github:ToJen
         Alex Rao; alexhrao@github.com; github:alexhrao
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone
         Ali; alispivak@mozilla.net; mdn:alispivak
         Fuqiao Xue; xfq@mozilla.net; mdn:xfq

# Transport Layer Security (TLS)

**Transport Layer Security (TLS)**, short for Transport Layer Security Protocol,
is a replacement for Secure Sockets Layer (SSL). TLS is a protocol used by applications to
communicate securely across a network, preventing tampering with and eavesdropping on email,
web browsing, messaging, and other protocols. Both SSL and TSL are client / server protocols ensuring
communication privacy,  providing cryptographic protocols providing security over a network.
When a server and client communicate, TLS ensures no third party can eavesdrop or tamper with any message.

All modern browsers support the TLS protocol, requiring the server to provide a valid digital
certificate confirming its identity in order to establish a secure connection. It is possible for
both the client and server to mutually authenticate each other, if both parties provide their own
individual digital certificates.

TLS protects against a downgrade of the protocol to a previous (less secure) version or a weaker
cipher suite. Released in January 1999 to create a standard for private communications,
as an upgrade to SSL 3.0, the goals of the TLS protocol are cryptographic security,
interoperability, extensibility, and relative efficiency. These goals are achieved through
implementation of the TLS protocol on two levels: the TLS Record protocol and the TLS Handshake protocol.

**TLS Record Protocol**:

The TLS Record protocol negotiates a private, reliable connection between client and server using
symmetric cryptography keys to ensure private connections
secured through Message Authentication Code() hash functions.

**TLS Handshake Protocol**:

The TLS Handshake protocol allows authenticated communication between the server and client by
agreeing upon an encryption algorithm and encryption keys before the selected application protocol
begins to send data.  TLS using the same handshake protocol procedure as SSL, but is more robust.
