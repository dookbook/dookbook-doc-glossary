TOPIC: Round Trip Time (RTT)
AUTHORS: Zac; zacnomore@mozilla.net; mdn:zacnomore

# Round Trip Time (RTT)

**Round Trip Time (RTT)** is the length of time it takes for a data packet to be sent
plus the length of time it takes for an acknowledgment of that packet to be received.
This time delay therefore consists of the propagation times between the two points. An
Internet user can determine the RTT between their network and a server by using the ping command

```http
$ ping example.com
PING example.com (216.58.194.174): 56 data bytes
64 bytes from 216.58.194.174: icmp_seq=0 ttl=55 time=25.050 ms
64 bytes from 216.58.194.174: icmp_seq=1 ttl=55 time=23.781 ms
64 bytes from 216.58.194.174: icmp_seq=2 ttl=55 time=24.287 ms
64 bytes from 216.58.194.174: icmp_seq=3 ttl=55 time=34.904 ms
64 bytes from 216.58.194.174: icmp_seq=4 ttl=55 time=26.119 ms
--- google.com ping statistics ---
5 packets transmitted, 5 packets received, 0.0% packet loss
round-trip min/avg/max/stddev = 23.781/26.828/34.904/4.114 ms
```

In the above example, the round trip time is 26.8ms

## See Also

- [Time to First Byte (TTFB)](https://wiki.developer.mozilla.org/en-US/docs/Glossary/time_to_first_byte)
- [Latency](https://wiki.developer.mozilla.org/en-US/docs/Glossary/Latency)
