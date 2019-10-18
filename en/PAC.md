TOPIC: PAC
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Duncan McDonald; duncanmcdonald@mozilla.net; mdn:duncanmcdonald
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy

# PAC

A Proxy Auto-Configuration file (**PAC file**) is a file which contains a function,
`FindProxyForURL()`, which is used by the browser to determine whether requests
(including HTTP, HTTPS, and FTP) should go directly to the destination or if they need
to be forwarded through a web proxy server.

```javascript
function FindProxyForURL(url, host) {
  /* ... */
}

ret = FindProxyForURL(url, host)
```

See Proxy Auto-Configuration (PAC) file for details about how these are used and
how to create new ones.

## Learn More

### General Knowledge

- [PAC](https://en.wikipedia.org/wiki/Proxy_auto-config) on Wikipedia

### Technical Reference

- [Proxy Auto-Configuration file](https://wiki.developer.mozilla.org/en-US/docs/Web/JavaScript/Proxy_Auto-Configuration_%28PAC%29_file)
on MDN
