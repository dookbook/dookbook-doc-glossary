TOPIC: Primitive

# Primitive

In JavaScript, a **primitive** (primitive value, primitive data type) is data that is
not an object and has no methods. There are 7 primitive data types: string, number,
bigint, boolean, null, undefined, symbol (new in ECMAScript 2016).

Most of the time, a primitive value is represented directly at the lowest level of the language implementation.

All primitives are **immutable**, i.e., they cannot be altered. It is important not to
confuse a primitive itself with a variable assigned a primitive value. The variable may
be reassigned a new value, but the existing value can not be changed in the ways that
objects, arrays, and functions can be altered.

## Example

This example would help you understand the fact that primitive values are **immutable**.

JavaScript

```javascript
// Using a string method doesn't mutate the string
var bar = "baz";
console.log(bar);               // baz
bar.toUpperCase();
console.log(bar);               // baz

// Using an array method mutates the array
var foo = [];
console.log(foo);               // []
foo.push("plugh");
console.log(foo);               // ["plugh"]

// Assignment gives the primitive a new (not a mutated) value
bar = bar.toUpperCase();       // BAZ
```

A primitive can be replaced, but it can't be directly altered.

## Another Example [ Step-by-step ]

The following example will help you going through how JavaScript deal with Primitives.

JavaScript

```javascript
// The Primitive
let foo = 5;

// Defining a function that should change the Primitive value
function addTwo(num) {
   num += 2;
}
// Another function trying to do the same thing
function addTwo_v2(foo) {
   foo += 2;
}

// Calling our first function while passing our Primitive as an argument
addTwo(foo);
// Getting the current Primitive value
console.log(foo);   // 5

// Trying again with our second function...
addTwo_v2(foo);
console.log(foo);   // 5
```

Did you expect it to be `7` instead of `5`? If so, read how this code runs:

- For both the `addTwo` and `addTwo_v2` functions calls, JavaScript looks up the value
for the identifier `foo`. It correctly finds our variable instantiated with our first statement
- After finding it, JavaScript passes that argument to the functions as a parameter
- Before executing the statements inside the functions' bodies,
**JavaScript takes acopy of the original passed argument** (which is a primitive) and
creates a local copy. These copies, existing only inside the functions' scopes, are
accessible via the identifiers we specified in the functions' definitions (`num` for
`addTwo`, `foo` for `addTwo_v2`)
- Then, the functions' statements are executed:
    - In the first function, a local `num` variable had been created. We are increasing
    its value by 2, not the original `foo`'s value!
    - In the second function, a local `foo` variable had been created. We are increasing
    its value by 2, not the original (external) `foo`'s value! Also, in this situation,
    the external `foo` variable cannot be accessed in any way. This is because of
    JavaScript's lexical scoping and the resulting variable shadowing. The local `foo`
    hides the external `foo`. For more information, see Closures.
- In conclusion, any changes inside our functions **won't** affect the ORIGINAL `foo` at
all, as we are working on our **copies** of it

That's why Primitives are immutable - instead of working on them directly, we're working
on a copy, without affecting the original.

## Primitive Wrapper Objects In JavaScript

Except for `null` and `undefined`, all primitive values have object equivalents that
wrap around the primitive values:

- `String` for the string primitive.
- `Number` for the number primitive.
- `BigInt` for the bigint primitive.
- `Boolean` for the boolean primitive.
- `Symbol` for the symbol primitive.

The wrapper's `valueOf()` method returns the primitive value.

## Learn More

### General Knowledge

- [Introduction to JavaScript data types](https://wiki.developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures)
- [Primitive data type](https://en.wikipedia.org/wiki/Primitive%20data%20type) on Wikipedia
