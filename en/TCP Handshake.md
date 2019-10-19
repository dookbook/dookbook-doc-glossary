TOPIC: TCP Handshake

# TCP Handshake

TCP (Transmission Control Protocol) is a Transport Layer host-to-host protocol for connection-oriented
communication between two computers on an IP network. TCP uses a **three-way** **handshake** (aka TCP-handshake,
three message handshake, and/or SYN-SYN-ACK) to set up a TCP/IP connection over an IP based network.
The three messages transmitted by TCP to negotiate and start a TCP session are nicknamed SYN, SYN-ACK,
and ACK for **SYN**chronize, **SYN**chronize-**ACK**nowledgement, and ACKnowledge respectively. The
three message mechanism is designed so that two computers that want to pass information back and
forth to each other can negotiate the parameters of the connection before transmitting data such as
HTTP browser requests.

The host, generally the browser, sends a TCP SYNchronize packet to the server. The server receives
the SYN and sends back a SYNchronize-ACKnowledgement. The host receives the server's SYN-ACK and
sends an ACKnowledge. The server receives ACK and the TCP socket connection is established.

This handshake step happens after a DNS lookup and before the TLS handshake, when creating a secure
connection. The connection can be terminated independently by each side of the connection via a
four-way handshake.

## See Also

- [Transport Layer Security (TLS) protocol](https://wiki.developer.mozilla.org/en-US/docs/Web/Security/Transport_Layer_Security)
- HTTPS
- [Transport Layer Security](https://en.wikipedia.org/wiki/Transport%20Layer%20Security) on Wikipedia
