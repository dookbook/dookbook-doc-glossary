TOPIC: TOFU
AUTHORS: Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         anoopprasad; anoop.prasad5@gmail.com; github:anoopprasad

# TOFU

**Trust On First Use (TOFU)** is a security model in which a client needs to create a trust
relationship with an unknown server. To do that, clients will look for identifiers
(for example public keys) stored locally. If an identifier is found, the client can establish the
connection. If no identifier is found, the client can prompt the user to
determine if the client should trust the identifier.

TOFU is used in the SSH protocol, in HTTP Public Key Pinning (HPKP) where the browsers will
accept the first public key returned by the server, and in `Strict-Transport-Security`
(HSTS) where a browser will obey the redirection rule.

## Learn More

### General Knowledge

- [HTTP Public Key Pinning](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Public_Key_Pinning)
(HPKP)
- [`Public-Key-Pins`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Public-Key-Pins)
- Wikipedia: [TOFU](https://en.wikipedia.org/wiki/Trust_on_first_use)
