TOPIC: Scope
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Kobe Davis; Llamaless@mozilla.net; mdn:Llamaless
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Shiladittya; sap@mozilla.net; mdn:sap
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone
         Liao Yazhi; 1594435860@qq.com; github:Liaoyazhi

# Scope

**The current context of execution**. The context in which *values* and *expressions* are
*"visible"*, or can be *referenced*. If a *variable* or other *expression* is not "in the
current scope," then it is unavailable for use. **Scopes** can also be layered in a
hierarchy, so that *child scopes* have access to *parent scopes*, but not vice versa.

## Global Scope

In a programming environment, the **global scope** is the scope that contains, and is visible in,
all other scopes.

In client-side [[JavaScript]], the **global scope** is generally the web page inside
which all the code is being executed.

## Local Scope

**Local scope** is a characteristic of variables that makes them local (i.e., the variable name is only
bound to its value within a scope which is not the *global scope*).

## Local Variable

A variable whose name is bound to its value only within a *local scope*.

```javascript
var global = 5;  // is a global variable

function fun(){
  var local = 10;  // is a local variable  
}
```

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
- [Local Variable on Wikipedia](https://en.wikipedia.org/wiki/Local%20variable)
