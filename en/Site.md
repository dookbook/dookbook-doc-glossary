TOPIC: Site
AUTHORS: Adam Williams; lol768@github.com; github:lol768

# Site

The site of a piece of web content is determined by the registrable domain of the host
within the origin. This is computed by consulting a Public Suffix List to find the
portion of the host which is counted as the public suffix (e.g. com, org or co.uk).

The concept of a site is used in [SameSite cookies](url), as well as a web application's
[Cross-Origin Resource Policy](url).

## Examples of same site

|  |  |
|--|--|
| `https://developer.mozilla.org/en-US/docs/`<br>`https://support.mozilla.org/en-US/` | same site because registrable domain of mozilla.org is the same |
| `http://example.com:8080`<br>`https://example.com` | same site because scheme and port are not relevant |

### Examples of different site

|  |  |
|--|--|
| `https://developer.mozilla.org/en-US/docs/`<br>`https://example.com` | not same site because registrable domain of the two URLs differs |

### Specifications

| Specification | Status | Comment |
|--|--|--|
| [URL](https://url.spec.whatwg.org/#host-same-site) | Living Standard | Initial definition |
