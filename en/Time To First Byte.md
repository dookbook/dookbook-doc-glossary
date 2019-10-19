TOPIC: Time To First Byte

# Time To First Byte

**Time to First Byte** (TTFB) refers to the time between the browser requesting a page and when it
receives the first byte of information from the server. This time includes DNS
lookup and establishing the connection using a TCP handshake and SSL handshake if
the request is made over https.

TTFB is the time it takes between the start of the request and the start of the response, in milliseconds:

```javascript
TTFB = responseStart - requestStart
```

## See Also

- [A typical HTTP session](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Session)
- [PerformanceResourceTiming](https://wiki.developer.mozilla.org/en-US/docs/Web/API/PerformanceResourceTiming)
- [PerformanceTiming](https://wiki.developer.mozilla.org/en-US/docs/Web/API/PerformanceTiming)
