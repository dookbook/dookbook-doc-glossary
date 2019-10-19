TOPIC: RTP (Real-time Transport Protocol) and SRTP (Secure RTP)
AUTHORS: Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Sphinx; SphinxKnight@github.com; github:SphinxKnight

# RTP (Real-time Transport Protocol) and SRTP (Secure RTP)

The **Real-time Transport Protocol (RTP)** is a network protocol which described how to
transmit various media (audio, video) from one endpoint to another in a real-time
fashion. RTP is suitable for video-streaming application, telephony over IP like Skype
and conference technologies.

The secure version of RTP, **SRTP**, is used by WebRTC, and uses encryption and
authentication to minimize the risk of denial-of-service attacks and security breaches.

RTP is rarely used alone; instead, it is used in conjunction with other protocols like RTSP and SDP.

## Learn More

### General Knowledge

- [Introduction to the Real-time Transport Protocol](https://wiki.developer.mozilla.org/en-US/docs/Web/API/WebRTC_API/Intro_to_RTP)
- [RTP](https://en.wikipedia.org/wiki/Real-time_Transport_Protocol) on Wikipedia
- [RFC 3550](https://tools.ietf.org/html/rfc3550)
(one of the documents that specify precisely how the protocol works)
