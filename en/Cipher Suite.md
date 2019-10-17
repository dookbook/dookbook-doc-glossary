TOPIC: Cipher Suite
AUTHORS: Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone
         April King; april@pokeinthe.io; github:april

# Cipher Suite

A cipher suite is a combination of a key exchange algorithm, authentication method,
bulk encryption cipher, and message authentication code.

In a **cryptosystem** like TLS, the client and server must agree on a cipher suite before
they can begin communicating securely.  A typical cipher suite looks
like ECDHE_RSA_WITH_AES_128_GCM_SHA256 or ECDHE-RSA-AES128-GCM-SHA256, indicating:

- ECDHE (elliptic curve Diffie-Hellman ephemeral) for key exchange

- RSA for authentication

- AES-128 as the cipher, with Galois/Counter Mode (GCM) as the block cipher mode of operation

- SHA-256 as the hash-based message authentication code (HMAC)

## Learn More

- [Mozilla recommended cipher suite choices for TLS](https://wiki.mozilla.org/Security/Server_Side_TLS)
