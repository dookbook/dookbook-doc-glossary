TOPIC: TCP Slow Start

# TCP Slow Start

**TCP slow start** helps buildup transmission speeds to the network's capabilities without initially
knowing what those capabilities are and without creating congestion. TCP slow start is an algorithm
used to detect the available bandwidth for packet transmission. It prevents the appearance of
network congestion whose capabilities are initially unknown.

To implement TCP slow start, the congestion window (cwnd) sets an upper limit on the amount of data
a source can transmit over the network before receiving an acknowledgment (ACK). The slow start
threshold (ssthresh) determines the (de)activation of slow start. When a new connection is made,
cwnd is initialized to one TCP data or acknowledgment packet, and waits an acknowledgement, or ACK.
When that ACK is received, the congestion window is incremented until the cwnd is less than ssthresh.
Slow start also terminates when congestion is experienced.

## Congestion control

As the server sends data in TCP packets, the user's client confirms delivery by returning acknoledgements,
or ACKs. The connection has a limited capacity depending on hardware and network conditions.
If the server sends too many packets too quickly, they will be dropped. Meaning,
there will be no acknowledgement. The server registers this as missing ACKs.
Congestion control algorithms use this flow of sent packets and ACKs to determine a send rate.

## See Also

- [Populating the page: how browsers work](https://wiki.developer.mozilla.org/en-US/docs/Web/Performance/Populating_the_page:_how_browsers_work)
- [http overview](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Overview)
