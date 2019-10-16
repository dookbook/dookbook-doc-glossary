TOPIC: Block cipher mode of operation
AUTHORS: Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills

# Block cipher mode of operation

A block cipher mode of operation, usually just called a "mode" in context, specifies how a block
cipher should be used to encrypt or decrypt messages that are longer than the block size.

Most symmetric-key algorithms currently in use are block ciphers: this means that they encrypt data
a block at a time. The size of each block is fixed and determined by the algorithm: for example **AES**
uses 16-byte blocks. Block ciphers are always used with a mode, which specifies how to securely
encrypt messages that are longer than the block size. For example, AES is a cipher, while CTR, CBC,
and GCM are all modes. Using an inappropriate mode, or using a mode incorrectly,
can completely undermine the security provided by the underlying cipher.
