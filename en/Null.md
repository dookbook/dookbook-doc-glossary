TOPIC: Null
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Rafael Trestini; trestini@mozilla.net; mdn:trestini
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone
         Schalk Neethling; schalkneethling@mozilla.net; mdn:schalkneethling
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Viktor Levytskyi; levytskyi@mozilla.net; mdn:levytskyi
         Sphinx; SphinxKnight@github.com; github:SphinxKnight
         Sergei Nizhivenko; snizh@mozilla.net; mdn:snizh
         Vani Ananthuni; vaniananthuni@mozilla.net; mdn:vaniananthuni
         James Kyle; thejameskyle@mozilla.net; mdn:thejameskyle
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         David Bruant; bruant.d@gmail.com; github:DavidBruant
         Teoli; teoli@mozilla.net; mdn:teoli

# Null

In computer science, a **`null`** value represents a reference that points, generally intentionally,
to a nonexistent or invalid object or address. The meaning of a null reference varies
among language implementations.

In JavaScript, null is one of the primitive values.

The value null represents the intentional absence of any object value. It is one of JavaScript's
primitive values.

## Syntax

```javascript
null
```

## Description

he value `null` is written with a literal: `null`. `null` is not an identifier for a property of the
global object, like `undefined` can be. Instead, `null` expresses a lack of identification, indicating
that a variable points to no object. In APIs, `null` is often retrieved in a place where an object
can be expected but no object is relevant.

```javascript
// foo does not exist. It is not defined and has never been initialized:
foo;
"ReferenceError: foo is not defined"

// foo is known to exist now but it has no type or value:
var foo = null;
foo;
"null"
```

### Difference Between `null` And `undefined`

When checking for `null` or `undefined`, beware of the differences between equality (==) and identity
(===) operators, as the former performs type-conversion.

```javascript
typeof null          // "object" (not "null" for legacy reasons)
typeof undefined     // "undefined"
null === undefined   // false
null  == undefined   // true
null === null        // true
null == null         // true
!null                // true
isNaN(1 + null)      // false
isNaN(1 + undefined) // true
```

## Learn More

### General Knowledge

- [Null pointer](https://en.wikipedia.org/wiki/Null%20pointer) on Wikipedia

### Technical Reference

- [JavaScript data types and data structures](https://wiki.developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures)
- The JavaScript global object: [`null`](https://wiki.developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/null)
