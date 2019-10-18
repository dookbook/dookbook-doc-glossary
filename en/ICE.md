TOPIC: ICE
AUTHORS: Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Teoli; teoli@mozilla.net; mdn:teoli

# ICE

**ICE** (Interactive Connectivity Establishment) is a framework used by WebRTC (among other
technologies) for connecting two peers to each other, regardless of network topology (usually for
audio and/or video chat). This protocol lets two peers find and establish a connection with one another
even though they may both be using Network Address Translator (NAT) to share a global IP address with
other devices on their respective local networks.

The framework algorithm looks for the lowest-latency path for connecting the two peers, trying these
options in order:

1. Direct UDP connection (In this case—and only this case—a STUN server is used to find out the
network-facing address of a peer
1. Direct TCP connection, via the HTTP port
1. Direct TCP connection, via the HTTPS port
1. Indirect connection via a relay/TURN server (if a direct connection fails, e.g. if one peer is
behind a firewall that blocks NAT traversal)

## Learn More

### General Knowledge

- [WebRTC](https://wiki.developer.mozilla.org/en-US/docs/Web/API/WebRTC_API), the principal
web-related protocol which uses ICE
- [WebRTC protocols](https://wiki.developer.mozilla.org/en-US/docs/Web/API/WebRTC_API/Architecture/Protocols)

### Technical Reference

- [RFC 5245](https://tools.ietf.org/html/rfc5245), the IETF specification for ICE
- [`RTCIceCandidate`](https://wiki.developer.mozilla.org/en-US/docs/Web/API/RTCIceCandidate),
the interface representing a ICE candidate
