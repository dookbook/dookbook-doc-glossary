TOPIC: Client Hints
AUTHORS: Janet Swisher; jmswisher@github.com; github:jmswisher

# Client Hints

**Client Hints** are a set of HTTP request header fields for proactive content negotiation
allowing clients to indicate a list of device and agent specific preferences.
Client Hints enable automated delivery of optimized assets like the automatic
negotiation of image DPR resolution.

Use of client hints isn't automatic: rather, servers must announce that they support client hints.
Servers announce support for Client Hints using the [`Accept-CH`](https://tools.ietf.org/html/draft-grigorik-http-client-hints-03#section-2.2.1)
(accept client hints) header
or an equivalent HTML meta element with the `http-equiv` attribute.

`Accept-CH: DPR, Width, Viewport-Width, Downlink`

and / or

`<meta http-equiv="Accept-CH" content="...">`

When a client receives the Accept-CH header, if supported, it appends Client Hint headers that match
the advertised field-values. For example, based on Accept-CH example above,
the client could append DPR, Width, Viewport-Width, and Downlink headers to all subsequent requests.
In the second example, the server gives the browser the hints by setting the Accept-CH meta tag.

Basically, with the Client Hints header, the developer or application can tell the browser to
advertise information about itself to the server, such as the device pixel ratio, the viewport width,
and the display width. The client can then give the server information about the client's environment,
and the server can determine which resources to send based on that information.

## See Also

- [Client Hints headers](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers#Client_hints)
- [`Vary` HTTP Header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Vary)
