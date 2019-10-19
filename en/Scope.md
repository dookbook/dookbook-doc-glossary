TOPIC: Scope
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Nkosilathi Sibanda; kosi53@hotmail.co.uk; github:thekosiguy
         Mohamed Al-Fahim; MohamedAlFahim@mozilla.net; mdn:MohamedAlFahim
         Irene Smith; ismith@mozilla.com; github:irenesmith
         Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         whitman; welm@mozilla.net; mdn:welm
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone

# Scope

The current context of execution. The context in which values and **expressions** are
"visible," or can be referenced. If a **variable** or other expression is not "in the
current scope," then it is unavailable for use. Scopes can also be layered in a
hierarchy, so that child scopes have access to parent scopes, but not vice versa.

A **function** serves as a **closure** in JavaScript, and thus creates a scope, so that
(for example) a variable defined exclusively within the function cannot be accessed from
outside the function or within other functions. For instance, the following is invalid:

```javascript
function exampleFunction() {
    var x = "declared inside function";  // x can only be used in exampleFunction
    console.log("Inside function");
    console.log(x);
}

console.log(x);  // Causes error
```

However, the following code is valid due to the variable being declared outside the
function, making it global:

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

### General Knowledge

- [Scope (computer science)](https://en.wikipedia.org/wiki/Scope%20(computer%20science)) on Wikipedia
