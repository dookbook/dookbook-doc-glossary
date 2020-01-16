TOPIC: Scope

# Scope

**The current context of execution**. The context in which *values* and *expressions* are
*"visible"*, or can be *referenced*. If a *variable* or other *expression* is not "in the
current scope," then it is unavailable for use. **Scopes** can also be layered in a
hierarchy, so that *child scopes* have access to *parent scopes*, but not vice versa.

## Example in JavaScript

A **function** serves as a *closure* in [[JavaScript]], and thus creates a scope, so that
(for example) a variable defined exclusively within the function cannot be accessed from
outside the function or within other functions. For instance, the following is **invalid**:

```javascript
function exampleFunction() {
    var x = "declared inside function";  // x can only be used in exampleFunction
    console.log("Inside function");
    console.log(x);
}

console.log(x);  // Causes error
```

However, the following code is valid due to the variable being declared outside the
function, making it *global*:

```javascript
var x = "declared outside function";

exampleFunction();

function exampleFunction() {
    console.log("Inside function");
    console.log(x);
}

console.log("Outside function");
console.log(x);
```

## Learn More

- [Scope (Computer Science) on Wikipedia](https://en.wikipedia.org/wiki/Scope%20(computer%20science))
