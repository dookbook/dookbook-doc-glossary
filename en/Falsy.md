TOPIC: Falsy
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         庄引; zhuangyin8@gmail.com; github:zhuangyin8
         Noel; thenoelman@github.com; github:thenoelman
         Michal Gallovič; gallovicm@gmail.com; github:MichalGallovic
         Nixixi; nilinli1994@gmail.com; github:NiLinli
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer

# Falsy

A **falsy** value is a value that is considered false when encountered in a Boolean context.

JavaScript uses Type Conversion to coerce any value to a Boolean in contexts that require it,
such as conditionals and loops.

!!! note

There are only **6 falsy** values in JavaScript

This means that when JavaScript is expecting a boolean and it is given one of the values below,
it will always evaluate to “falsy”

|  |  |
| -- | -- |
| `false` | The keyword false |
| `0` | The number zero |
| `0n` | BigInt, when used as a boolean, follows the same rule as a Number. 0n is falsy. |
| `""`, `''`, ` `` ` | This is an empty string(the length of the string is zero).Strings in JavaScript can be defined with double quotes `""`, or single quotes `''`, as well as Template literals ` `` ` |
| `null` | null  - the absence of any object value |
| `undefined` | undefined - the primitive value |
| `NaN` | NaN - not a number |

## Examples

Examples of falsy values in JavaScript (which are coerced to false in Boolean contexts, and thus
bypass the `if` block):

```javascript
if (false)
if (null)
if (undefined)
if (0)
if (0n)
if (NaN)
if ('')
if ("")
if (``)
if (document.all)
```

### The logical AND operator, &&

If the first object is falsy, it returns that object

```javascript
let pet = false && "dog";

// ↪ false
```

!!! note
    `document.all` has been used for browser detection in the past and the
    [HTML specification defines a willful violation](http://www.whatwg.org/specs/web-apps/current-work/multipage/obsolete.html#dom-document-all)
    of the ECMAScript standard here to keep compatibility with legacy code
    (`if (document.all) { // Internet Explorer code here(except IE11) }`
    or using `document.all` without checking its presence first: `document.all.foo`).

Sometimes written **falsey**, although in English usually turning a word into an adjective with a -y,
any final e is dropped (noise => noisy, ice => icy, shine => shiny)

## Learn More

- Truthy
- Boolean
