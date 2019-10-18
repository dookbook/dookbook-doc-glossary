TOPIC: HTTP/2
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Andy Stevens; andystevensname@github.com; github:andystevensname

# HTTP/2

HTTP/2 is a major revision of the HTTP network protocol. The primary goals for HTTP/2 are to
reduce latency by enabling full request and response multiplexing, minimize protocol
overhead via efficient compression of HTTP header fields,
and add support for request prioritization and server push.

HTTP/2 does not modify the application semantics of HTTP in any way. All the core concepts found in
HTTP 1.1, such as HTTP methods, status codes, URIs, and header fields, remain in place. Instead,
HTTP/2 modifies how the data is formatted (framed) and transported between the client and server,
both of which manage the entire process, and hides application complexity within the new framing layer.
As a result, all existing applications can be delivered without modification.
