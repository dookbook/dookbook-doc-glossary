TOPIC: JavaScript

# JavaScript Programming Language

**JavaScript** (**JS**) is a programming language mostly used to dynamically script webpages on the client
side, but it is also often utilized on the server-side, using packages such as [Node.js](http://nodejs.org/).

JavaScript should not be confused with the [[Java]] programming language.
Both "Java" and
"JavaScript" are trademarks or registered trademarks of Oracle in the U.S. and other countries.
However, the two programming languages are significantly different in their syntax, semantics, and uses.

## History

Conceived as a server-side language by *Brendan Eich* (then employed by the Netscape Corporation),
JavaScript soon came to *Netscape Navigator 2.0* in September 1995. JavaScript enjoyed immediate success
and Internet Explorer 3.0 introduced JavaScript support under the name *JScript* in August 1996.

In November 1996, Netscape began working with *[[ECMA]] International* to make JavaScript an industry
standard. Since then, the standardized JavaScript is called *[[ECMAScript]]* and specified under **ECMA-262**.

## Application Scenarios

JavaScript is mostly used in the *browser*, enabling developers to manipulate webpage content through
the [[DOM]], manipulate data with [[AJAX]] and IndexedDB, draw graphics with canvas, interact with
the device running the browser through various APIs, and so forth. JavaScript is one of the world's most
commonly-used languages, owing to the recent growth and performance
improvement of APIs available in browsers.

Recently, JavaScript's popularity has expanded even further through the successful **[Node.js](http://nodejs.org/)**
platform - the most popular cross-platform JavaScript runtime environment outside the browser.
Node.js allows developers to use JavaScript as a scripting language to automate things on a PC and
build fully functional [[HTTP]] and [[WebSocket]] servers.

## Object-Oriented

JavaScript is heavily **object-oriented**. It follows a **`prototype`**-based model (as opposed to class-based).

## Dynamic Typing

JavaScript is a **loosely typed** or a *[dynamic language](/en/glossary/dynamic_programming_language)*.
Variables in JavaScript are not directly associated with any particular value type, and any variable
can be assigned (and re-assigned) values of all types:

```javascript
let foo = 42;    // foo is now a number
foo     = 'bar'; // foo is now a string
foo     = true;  // foo is now a boolean
```

## Data Type

The latest [[ECMAScript]] standard defines eight data types:

- Seven data types that are primitives:
    - [`boolean`](/en/webfrontend/Boolean)
    - [`null`](/en/webfrontend/null)
    - [`undefined`](/en/webfrontend/undefined)
    - `number`
    - `bigint`
    - `string`
    - `symbol` (new in ECMAScript 2016)
- and `Object`.

### Primitive Wrapper Objects In JavaScript

Except for [`null`](/en/webfrontend/null) and [`undefined`](/en/webfrontend/undefined), all
primitive values have object equivalents that wrap around the primitive values:

- `String` for the `string` primitive.
- `Number` for the `number` primitive.
- `BigInt` for the `bigint` primitive.
- `Boolean` for the `boolean` primitive.
- `Symbol` for the `symbol` primitive.

The wrapper's `valueOf()` method returns the primitive value.

## Learn More

- [JavaScript on Wikipedia](https://en.wikipedia.org/wiki/JavaScript)
- [ECMAScript (ECMA-262) Standard](http://www.ecma-international.org/publications/standards/Ecma-262.htm)
