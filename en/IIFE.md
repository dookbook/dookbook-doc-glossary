TOPIC: IIFE
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Edmund; vssn@mozilla.net; mdn:vssn
         Fotios Tragopoulos; tragopoulos@icloud.com; github:Tragopoulos
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Martin di Martino-Marriott; MartinDM@github.com; github:MartinDM
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Victor van Poppelen; vvanpo@github.com; github:vvanpo
         Irvin Chen; irvinfly@mozilla.net; mdn:irvinfly
         Rolfe Dlugy-Hegwer; rolfedh@github.com; github:rolfedh

# IIFE

An **IIFE** (Immediately Invoked Function Expression) is a JavaScript function that runs
as soon as it is defined.

```javascript
(function () {
    statements
})();
```

It is a design pattern which is also known as a Self-Executing Anonymous Function and contains two
major parts. The first is the anonymous function with lexical scope enclosed within
the `Grouping Operator` `()`. This prevents accessing variables within the IIFE idiom as
well as polluting the global scope.

The second part creates the immediately executing function expression `()` through which the
JavaScript engine will directly interpret the function.

## Examples

The function becomes a function expression which is immediately executed. The variable within the
expression can not be accessed from outside it.

```javascript
(function () {
    var aName = "Barry";
})();
// Variable name is not accessible from the outside scope
aName // throws "Uncaught ReferenceError: aName is not defined"
```

Assigning the IIFE to a variable stores the function's return value, not the function definition itself.

```javascript
var result = (function () {
    var name = "Barry";
    return name;
})();
// Immediately creates the output:
result; // "Barry"
```
