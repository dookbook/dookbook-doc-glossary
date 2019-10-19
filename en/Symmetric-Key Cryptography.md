TOPIC: Symmetric-Key Cryptography
AUTHORS: Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills

# Symmetric-Key Cryptography

Symmetric-key cryptography is a term used for cryptographic algorithms that use the same key for
encryption and for decryption. The key is usually called a "symmetric key" or a "secret key".

This is usually contrasted with public-key cryptography, in which keys are generated in pairs and
the transformation made by one key can only be reversed using the other key.

Symmetric-key algorithms should be secure when used properly and are highly efficient, so they can
be used to encrypt large amounts of data without having a negative effect on performance.

Most symmetric-key algorithms currently in use are block ciphers: this means that they encrypt data
one block at a time. The size of each block is fixed and determined by the algorithm: for example
AES uses 16-byte blocks. Block ciphers are always used with a mode, which specifies how to
securely encrypt messages that are longer than the block size. For example, AES is a cipher,
while CTR, CBC, and GCM are all modes. Using an inappropriate mode, or using a mode incorrectly,
can completely undermine the security provided by the underlying cipher.
