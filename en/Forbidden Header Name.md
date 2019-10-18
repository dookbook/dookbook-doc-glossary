TOPIC: Forbidden Header Name
AUTHORS: Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Samuel Bronson; Naesten@mozilla.net; mdn:Naesten
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone

# Forbidden Header Name

A forbidden header name is the name of any HTTP header that cannot be
modified programmatically; specifically, an HTTP **request** header name (in contrast with a
Forbidden response header name).

Modifying such headers is forbidden because the user agent retains full control over them.
Names starting with `Sec-` are reserved for creating new headers safe from APIs using Fetch
that grant developers control over headers, such as `XMLHttpRequest`.

Forbidden header names start with `Proxy-` or `Sec-`, or are one of the following names:

- `Accept-Charset`
- `Accept-Encoding`
- `Access-Control-Request-Headers`
- `Access-Control-Request-Method`
- `Connection`
- `Content-Length`
- `Cookie`
- `Cookie2`
- `Date`
- `DNT`
- `Expect`
- `Host`
- `Keep-Alive`
- `Origin`
- `Proxy-`
- `Sec-`
- `Referer`
- `TE`
- `Trailer`
- `Transfer-Encoding`
- `Upgrade`
- `Via`

!!! note
    The `User-Agent` header is no longer forbidden, [as per spec](https://fetch.spec.whatwg.org/#terminology-headers)
    — see forbidden header name list (this was implemented in Firefox 43) — it can now be set in a
    Fetch Headers object, or via XHR setRequestHeader().
