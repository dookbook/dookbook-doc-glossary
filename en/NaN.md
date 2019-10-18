TOPIC: NaN
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Ajinkya Patil; ajinkya_p@mozilla.net; mdn:ajinkya_p
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Jongryul Yang; urty5656@gmail.com; github:alattalatta
         Rick Waldron; waldron.rick@gmail.com; github:rwaldron
         Schalk Neethling; schalkneethling@mozilla.net; mdn:schalkneethling
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Teoli; teoli@mozilla.net; mdn:teoli
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Keiichi; ethertank@mozilla.net; mdn:ethertank
         Janet Swisher; jmswisher@github.com; github:jmswisher
         David Bruant; bruant.d@gmail.com; github:DavidBruant
         Tom Schuster; evilpie@github.com; github:evilpie
         Nickolay Ponomarev; asqueella@gmail.com; github:nickolay
         Marek Stępień; marcoos@github.com; github:marcoos

# NaN

NaN (Not a Number) is a numeric data type that means an undefined value or value that cannot be
represented, especially results of floating-point calculations.

For example, NaNs can represent infinity, result of division by zero, missing value, or the square
root of a negative (which is imaginary, whereas a floating-point number is real).

Practically speaking, if I divide two variables in a JavaScript program, the result may be NaN,
which is predefined in JavaScript as "undefined". Hence this division may break the program. Now,
if this computation was a small part of a much larger algorithm, it would be really painful to figure
out where the error actually occurs. Fortunately, since the result will be NaN and I know my divisor
may turn out to be 0, I can set up testing conditions that prevent any such computations in the first
place or notify me of where they happen.

The global **`NaN`** property is a value representing Not-A-Number.

| **Property attributes of `NaN`** | |
| - | - |
| Writable | no
| Enumerable | no
| Configurable | no

## Description

`NaN` is a property of the global object.

The initial value of `NaN` is Not-A-Number — the same as the value of `Number.NaN`. In modern browsers,
`NaN` is a non-configurable, non-writable property. Even when this is not the case,
avoid overriding it.

It is rather rare to use `NaN` in a program. It is the returned value when `Math` functions fail
(`Math.sqrt(-1)`) or when a function trying to parse a number fails (`parseInt("blabla")`).

### Testing Against `NaN`

`NaN` compares unequal (via `==`, `!=`, `===`, and `!==`) to any other value -- including to another
NaN value. Use `Number.isNaN()` or `isNaN()` to most clearly determine whether a value is NaN.
Or perform a self-comparison: NaN, and only NaN, will compare unequal to itself.

```javascript
NaN === NaN;        // false
Number.NaN === NaN; // false
isNaN(NaN);         // true
isNaN(Number.NaN);  // true

function valueIsNaN(v) { return v !== v; }
valueIsNaN(1);          // false
valueIsNaN(NaN);        // true
valueIsNaN(Number.NaN); // true
```

However, do note the difference between `isNaN()` and `Number.isNaN()`: the former will return `true`
if the value is currently `NaN`, or if it is going to be `NaN` after it is coerced to a number,
while the latter will return `true` only if the value is currently `NaN`:

```javascript
isNaN('hello world');        // true
Number.isNaN('hello world'); // false
```

## Learn More

### General Knowledge

- [NaN](https://en.wikipedia.org/wiki/NaN) on Wikipedia
