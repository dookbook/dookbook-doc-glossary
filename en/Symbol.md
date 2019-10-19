TOPIC: Symbol
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         DwijBavisi; Dwijbavisi@gmail.com; github:DwijBavisi
         Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Volodymyr Pantasenko; vpantasenko@github.com; github:vpantasenko
         Chafic Najjar; chafic.najjar@gmail.com; github:chaficnajjar
         Siddhant; supertramp.sid@gmail.com; github:formatkaka
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Raphael Kubo da Costa; rakuco@mozilla.net; mdn:rakuco
         Vani Ananthuni; vaniananthuni@mozilla.net; mdn:vaniananthuni
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Sukant Garg; gargsms@mozilla.net; mdn:gargsms

# Symbol

In JavaScript, Symbol is a primitive value.

A value having the data type "**symbol**" can be referred to as a "symbol value." In the JavaScript
run-time environment, a symbol value is created by invoking the function `Symbol`),
which dynamically produces an anonymous, unique value. A symbol may be used as an object property.

Symbol can have an optional description, but for debugging purposes only.

A **Symbol** value represents a unique identifier. For example,

```javascript
// here are two symbols with the same description,
let Sym1 = Symbol("Sym");
let Sym2 = Symbol("Sym");
  
console.log(Sym1 == Sym2); // returns "false"
// Symbols are guaranteed to be unique.
// Even if we create many symbols with the same description,
// they are different values.
```

Note: If you are familiar with Ruby or another language that also has some sort of “symbols” –
please don’t be misguided. JavaScript symbols are different.

Symbol type is a new feature in ECMAScript 2015 and there is no ECMAScript 5 equivalent for symbol.
In some programming languages the symbol data type is referred to as an "atom."

## Symbols Don't Auto-Convert To "strings"

Most values in JavaScript support implicit conversion to a string. For instance, we can `alert`
almost any value, and it will work. Symbols are special. They don’t auto-convert.

For example,

```javascript
let Sym = Symbol("Sym");

alert(Sym); // TypeError: Cannot convert a Symbol value to a string
```

That’s a “language guard” against messing up, because strings and symbols are fundamentally different
and should not occasionally convert one into another.

If we really want to show a symbol, we need to call `.toString()` on it, for example,

```javascript
let Sym = Symbol("Sym");

alert(Sym.toString()); // Symbol(Sym), now it works
```

Or we can use get `symbol.description` property to get the description on it, for example,

```javascript
let _Sym = Symbol("Sym");

alert(_Sym.description); // Sym
```

## Well-known Symbols

The `Symbol` class has constants for so-called well-known symbols. These symbols let you
configure how JS treats an object, by using them as property keys. Examples of well-known symbols
are: `Symbol.iterator` for array-like objects, or `Symbol.search` for string objects.

They are listed in the specification in the [Well-known symbols](https://tc39.github.io/ecma262/#sec-well-known-symbols)
table:

- `Symbol.hasInstance`
- `Symbol.isConcatSpreadable`
- `Symbol.iterator`
- `Symbol.toPrimitive`
- …and so on.

## Global Symbol Registry

The methods that access the global symbol registry are `Symbol.for()` and
`Symbol.keyFor()`; these mediate between the global symbol table (or "registry") and the
run-time environment. The symbol registry is mostly built by JavaScript's compiler infrastructure,
and the symbol registry's content is not available to JavaScript's run-time infrastructure,
except through these reflective methods. The method `Symbol.for("tokenString")` returns a symbol
value from the registry, and `Symbol.keyFor(symbolValue)` returns a token string from the registry;
each is the other's inverse, so the following is true:

```javascript
Symbol.keyFor(Symbol.for("tokenString")) == "tokenString"; // true
```

## Learn More

### General Knowledge

- [Symbol (programming)](https://en.wikipedia.org/wiki/Symbol%20(programming)) on Wikipedia
- [JavaScript data types and data structures](https://wiki.developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures)
- [Symbols in ECMAScript 6](http://2ality.com/2014/12/es6-symbols.html)
- [`Symbol`](https://wiki.developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol)
in the MDN JS reference
- [`Object.getOwnPropertySymbols()`](https://wiki.developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/getOwnPropertySymbols)
