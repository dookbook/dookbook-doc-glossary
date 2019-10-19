TOPIC: Secure Sockets Layer (SSL)
AUTHORS: Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         April King; april@pokeinthe.io; github:april
         Jeremy Gutzwiller; JeremyGutzy@github.com; github:JeremyGutzy

# Secure Sockets Layer (SSL)

SSL (Secure Sockets Layer) is a standard protocol that ensures communication sent
between two computer applications is private and secure
(cannot be read nor changed by outside observers). It is the foundation for the TLS protocol.

Secure Sockets Layer, or SSL, is the old standard security technology for creating an
encrypted link between a server and client (browser), ensuring all data passed is private and secure.
The current version of SSL is version 3.0, released by Netscape in 1999, and is being
superseded by the Transport Layer Security (TLS) protocol.

## How SSL Works

Using a four protocols, including a handshake of nine messages, the server authenticates
itself to a client transmitting and requesting information. The four protocol layers of
the Secure Socket Layer protocol include:

1. Record Layer,
1. ChangeCipherSpec Protocol,
1. Alert Protocol, and
1. Handshake Protocol

These four protocols encapsulate all communication between the client and server.

Record Layer
:   The record layer formats the other protocol messages, providing a 5-byte header for each
    message and a Message Authentication Code (MAC) hash.

ChangeCipherSpec Protocol
:   The ChangeCipherSpec layer is composed a single message signaling the start of secure
    communications between the client and server. The ChangeCipherSpec message is a single
    byte signaling the change in communications protocol by having a value of ‘1’.

Alert Protocol
:   The alert protocol sends a 2-field message regarding connection errors, problems or warnings including:
    Severity Level
    :   The severity level sends messages with a ‘1’ for warnings ‘2’ is fatal. A warning
        suggests parties reconnect using a new handshake. A fatal alert with a value of ‘2’,
        discontinues the session.

    Alert Description
    :   The Alert Description is one byte mapped to 12 numbers indicating the specific error
        causing the alert, including CloseNotify, UnexpectedMessage, BadRecordMAC,
        DecompressionFailure, HandshakeFailure, NoCertificate, BadCertificate,
        UnsupportedCertificate, CertificateRevoked, CertificateExpired, CertificateUnknown,
        and IllegalParameter.

Handshake Protocol
:   Messages passed back and forth between the client and server establish a handshake
    beginning a secure connection. SSL handshake steps include ClientHello, ServerHello,
    ServerKeyExchange, ServerHelloDone, ClientKeyExchange, ChangeCipherSpec, Finished,
    ChangeCipherSpec, Finished. Of interest, the ServerKeyExchange is where encryption begins.
    The server has already okayed data transmission: the ServerKeyExchange determines how that data
    transmission will be encrypted. The server's public key is encrypt a session key to be used by
    the client and server to encrypt the data that is transmitted.
