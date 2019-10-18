TOPIC: Mutable
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Wojciech Jedynak; wjzz@github.com; github:wjzz
         Mayank Gupta; Mayankgupta688@mozilla.net; mdn:Mayankgupta688
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz

# Mutable

Mutable is a type of variable that can be changed. In JavaScript, only objects and arrays are mutable,
not primitive values.

(You can make a variable name point to a new value, but the previous value is still held in memory.
Hence the need for garbage collection.)

A **mutable object** is an object whose state can be modified after it is created.

**Immutables** are the objects whose state cannot be changed once the object is created.

**String and Numbers** are **Immutable**. Lets understand this with an example:

```javascript
var immutableString = "Hello";

// In the above code, a new object with string value is created.

immutableString = immutableString + "World";

// We are now appending "World" to the existing value.
```

On appending the "immutableString" with a string value, following events occur:

1. Existing value of "immutableString" is retrieved
1. "World" is appended to the existing value of "immutableString"
1. he resultant value is then allocated to a new block of memory
1. "immutableString" object now points to the newly created memory space
1. Previously created memory space is now available for garbage collection.

## Learn More

### General Knowledge

- [Immutable Object](https://en.wikipedia.org/wiki/Immutable%20object) on Wikipedia
