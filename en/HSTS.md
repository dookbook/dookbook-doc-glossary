TOPIC: HSTS
AUTHORS: Teoli; teoli@mozilla.net; mdn:teoli
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz

# HSTS

**HTTP Strict Transport Security** lets a web site inform the browser that it should never load the
site using HTTP and should automatically convert all attempts to access the site using HTTP to HTTPS
requests instead. It consists in one HTTP header, `Strict-Transport-Security`, sent back by
the server with the resource.

In other words, it tells the browser that just changing the protocol from HTTP to HTTPS in an url
will work (and be more secure) and ask the browser to do it for every request.

## Learn More

- [`Strict-Transport-Security`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security)
- OWASP Article: [HTTP Strict Transport Security](https://www.owasp.org/index.php/HTTP_Strict_Transport_Security)
- Wikipedia: [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP%20Strict%20Transport%20Security)
