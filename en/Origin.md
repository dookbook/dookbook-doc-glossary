TOPIC: Origin
AUTHORS: Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Teoli; teoli@mozilla.net; mdn:teoli
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer

# Origin

Web content's **origin** is defined by the scheme (protocol), host (domain), and port of the URL
used to access it. Two objects have the same origin only when the scheme, host, and port all match.

Some operations are restricted to same-origin content, and this restriction can be lifted using CORS.

## Examples Of Same Origin

|  |  |
| -- | -- |
| `http://example.com/app1/index.html`<br>`http://example.com/app2/index.html` | same origin because same scheme (`http`) and host (`example.com`) |
| `http://Example.com:80`<br>`http://example.com` | same origin because a server delivers HTTP content through port 80 by default |

## Examples of Different Origin

|  |  |
| -- | -- |
| `http://example.com/app1`<br>`https://example.com/app2` | different schemes |
| `https://example.com/app2`<br>`http://www.example.com`<br>`http://myapp.example.com` | different hosts |
| `http://example.com`<br>`http://example.com:8080` | different ports |

## Specifications

| Specification | Status | Comment |
| -- | -- | -- |
| [HTML Living Standard The definition of 'origin' in that specification.](https://html.spec.whatwg.org/multipage/#origin) | Living Standard |  |

## Learn More

- See [Same-origin policy](https://wiki.developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy)
for more information.
