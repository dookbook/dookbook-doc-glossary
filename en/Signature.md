TOPIC: Signature
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Julia Buchner; PetiPandaRou@mozilla.net; mdn:PetiPandaRou
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone
         Teoli; teoli@mozilla.net; mdn:teoli
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         April King; april@pokeinthe.io; github:april

# Signature

The term **signature** can have several meanings depending on the context. It may refer to:

## Signature (security)

A **signature**, or digital signature, is a protocol showing that a message is authentic.

From the hash of a given message, the **signing process** first generates a digital
signature linked to the signing entity, using the entity's private key.

On receiving the message, the **verification process**

- authenticates the sender - uses the sender's public key to decrypt the signature and
recover the hash, which can only be created with the sender's private key, and
- checks message integrity - compares the hash with a newly calculated one from the
received document (the two hashes will differ if the document has been tampered with)

The system fails if the private key is compromised or the recipient is deceitfully given
the wrong public key.

## Learn More

- [Signature](https://en.wikipedia.org/wiki/Signature_(disambiguation)) on Wikipedia

### General Knowledge

- [Digital signature](https://en.wikipedia.org/wiki/Digital%20signature) on Wikipedia
- See digest, encryption
