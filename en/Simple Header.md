TOPIC: Simple Header
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Anne van Kesteren; annevk@annevk.nl; github:annevk
         Teoli; teoli@mozilla.net; mdn:teoli
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills

# Simple header

A simple header (or CORS-safelisted request header) is one of the following HTTP headers:

- `Accept`,
- `Accept-Language`,
- `Content-Language`,
- `Content-Type` with a MIME type of its parsed value (ignoring parameters) of
either `application/x-www-form-urlencoded`, `multipart/form-data`, or `text/plain`.

Or one of these client hint headers:

- `DPR`
- `Downlink`
- `Save-Data`
- `Viewport-Width`
- `Width`

When containing only simple headers, a requests is deemed simple and doesn't need to
send a preflight request in the context of CORS.
