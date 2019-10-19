TOPIC: Quality Values
AUTHORS: Teoli; teoli@mozilla.net; mdn:teoli
         David Ross; bunnybooboo@github.com; github:bunnybooboo
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz

# Quality Values

**Quality values**, or q-values and q-factors, are used to describe the order of
priority of values in a comma-separated list. It is a special syntax allowed in some
HTTP headers and in HTML. The importance of a value is marked by the suffix
'`;q=`' immediately followed by a value between `0` and `1` included, with up to three
decimal digits, the highest value denoting the highest priority. When not present, the
default value is `1`.

## Examples

The following syntax

> text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8

indicates the order of priority:

| Value | Priority |
| -- | -- |
| `text/html` and `application/xhtml+xml` | `1.0` |
| `application/xml` | `0.9` |
| `*/*` | `0.8` |

If there is no priority defined for the first two values, the order in the list is irrelevant.

Nevertheless, with the same quality, more specific values have priority over less specific ones:

> text/html;q=0.8,text/*;q=0.8,*/*;q=0.8

| Value | Priority |
| -- | -- |
| `text/html` | `0.8` (but totally specified) |
| `text/*` | `0.8` (partially specified) |
| `*/*` | `0.8` (not specified) |

Some syntax, like the one of Accept, allow additional specifiers like
`text/html;level=1`. These increase the specificity of the value. Their use is extremely rare.

## Browser-specific Information

### Firefox

Starting with Firefox 18, the quality factor values are clamped to 2 decimal places.
They used to be clamped to only 1 decimal place in earlier versions ([bug 672448](https://bugzilla.mozilla.org/show_bug.cgi?id=672448)).

## More Information

- [HTTP headers](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers) using q-values in
their syntax: [`Accept`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Accept),
[`Accept-Charset`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Accept-Charset),
[`Accept-Language`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Accept-Language),
[`Accept-Encoding`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Accept-Encoding),
[`TE`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/TE).
