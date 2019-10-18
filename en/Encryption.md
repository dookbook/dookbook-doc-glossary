TOPIC: Encryption
AUTHORS: April King; april@pokeinthe.io; github:april
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone
         Teoli; teoli@mozilla.net; mdn:teoli
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer

# Encryption

In cryptography, **encryption** is the conversion of cleartext into a coded text or ciphertext.
A ciphertext is intended to be unreadable by unauthorized readers.

Encryption is a cryptographic primitive: it transforms a plaintext message into a ciphertext using a
cryptographic algorithm called a cipher. Encryption in modern ciphers is performed using a specific
algorithm and a secret, called the key. Since the algorithm is often public,
the key must stay secret if the encryption stays secure.

![text](https://mdn.mozillademos.org/files/9815/Encryption.png)

Without knowing the secret, the reverse operation, decryption, is mathematically hard to perform.
How hard depends on the security of the cryptographic algorithm
chosen and evolves with the progress of cryptanalysis.

## Learn More

### General Knowledge

- Encryption and Decryption [Encryption and Decryption](https://developer.mozilla.org/en-US/docs/Encryption_and_Decryption)
