TOPIC: Global Object
AUTHORS: brian; bminard@flatfoot.ca; github:bminard
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Yahya Elharony; yahya@elharony.com; github:elharony
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie

# Global Object

A global object is an object that always exists in the global scope.

In JavaScript, there's always a global object defined. In a web browser, when scripts create global
variables, they're created as members of the global object. (In Node.js this is not the case.)
The global object's interface depends on the execution context in which the script is running.
For example:

- In a web browser, any code which the script doesn't specifically start up as a background task has
a `Window` as its global object. This is the vast majority of JavaScript code on the Web.
  
- Code running in a `Worker` has a `WorkerGlobalScope` object as its global object.
  
- Scripts running under Node.js have an object called `global` as their global object.

## `window` Object In The Browser

The `window` object is the Global Object in the Browser. Any Global Variables or Functions can be
accessed as properties of the `window` object.

### Access Global Variables

```javascript
var foo = "foobar";
foo === window.foo; // Returns: true
```

After defining a Global Variable `foo`, we can access its value directly from the `window` object,
by using the variable name `foo` as a property name of the Global Object `window.foo`.

Explanation

The global variable `foo` was stored in the `window` object, like this:

```javascript
foo: "foobar"
```

### Access Global Functions

```javascript
function greeting() {
   console.log("Hi!");
}

window.greeting(); // It is the same as the normal invoking: greeting();
```

The example above explain how Global Functions are stored as properties in the `window` object.
We created a Global Function `greeting`, then invoke it using the `window` object.

Explanation

The global function `greeting` was stored in the `window` object, like this:

```javascript
greeting: function greeting() {
   console.log("Hi!");
}
```
