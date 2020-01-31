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

Recently, JavaScript's popularity has expanded even further through the successful [**Node.js**](http://nodejs.org/)
platform - the most popular cross-platform JavaScript runtime environment outside the browser.
Node.js allows developers to use JavaScript as a scripting language to automate things on a PC and
build fully functional [[HTTP]] and [[WebSocket]] servers.

## Object-Oriented

JavaScript is heavily **object-oriented**. It follows a **`prototype`**-based model (as opposed to class-based).

### Inheritance and the Prototype Chain

JavaScript is a bit confusing for developers experienced in class-based languages (like Java or C++),
as it is *dynamic* and does not provide a class implementation per se (the `class` keyword is
introduced in *ES2015*, but is *syntactical sugar*, JavaScript remains **`prototype`-based**).

When it comes to **inheritance**, JavaScript only has one construct: *objects*.
Each object has a *private property* which holds a link to another object called its **prototype**.
That prototype object has a prototype of its own, and so on until an object is reached with *`null`*
as its prototype.
By definition, `null` has no prototype, and acts as the final link in this **prototype chain**.

Nearly all objects in JavaScript are instances of **[Object](/en/webfrontend/Object)** which sits on
the **top** of a prototype chain.

While this confusion is often considered to be one of JavaScript's weaknesses, the prototypal
inheritance model itself is, in fact, more powerful than the classic model. It is, for example,
fairly trivial to build a classic model on top of a prototypal model.

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
    - [`number`](/en/webfrontend/Number)
    - [`bigint`](/en/webfrontend/BigInt)
    - [`string`](/en/webfrontend/String)
    - `symbol` (new in ECMAScript 2016)
- and [`Object`](/en/webfrontend/Object).

### Primitive Wrapper Objects In JavaScript

Except for [`null`](/en/webfrontend/null) and [`undefined`](/en/webfrontend/undefined), all
primitive values have object equivalents that wrap around the primitive values:

- [`String`](/en/webfrontend/String) for the `string` primitive.
- [`Number`](/en/webfrontend/Number) for the `number` primitive.
- [`BigInt`](/en/webfrontend/BigInt) for the `bigint` primitive.
- [`Boolean`](/en/webfrontend/Boolean) for the `boolean` primitive.
- `Symbol` for the `symbol` primitive.

The wrapper's `valueOf()` method returns the primitive value.

## `for` Loop

### Syntax of `for` Loop

```javascript
for (statement 1; statement 2; statement 3){
  execute code block
}
```

- `statement 1` is executed once before the code block is run.

- `statement 2` defines the condition needed to execute the code block.

- `statement 3` is executed every time the code block is run.

### Example of `for` Loop

```javascript
for(var i = 0; i < 10; i++){
  console.log(i)
}
//This loop will print numbers 0-9, will stop when condition is met (i = 10)
```

For the above example, the syntax is as follows:

- Statement 1 sets the variable for the loop (`var i = 0`).

- Statement 2 sets the loop condition (`i < 10`).

- Statement 3 increases the value of `i` (`i++`) each time the code block is run.

## `while` Loop

### Syntax of `while` Loop

```javascript
while (condition){
  execute code block
}
```

- The code block will continue to loop as long as the `condition` is `true`.

### Example of `while` Loop

```javascript
var i = 0;
while(i < 5){
  console.log(i)
  i++
}
//This loop  will print number 0-4, will stop when condition becomes false (i >=5)
```

For the above example, the syntax is as follows:

- The code block will continue to run as long as the variable (`i`) is less than `5`.

## Learn More

- [JavaScript on Wikipedia](https://en.wikipedia.org/wiki/JavaScript)
- [ECMAScript (ECMA-262) Standard](http://www.ecma-international.org/publications/standards/Ecma-262.htm)
