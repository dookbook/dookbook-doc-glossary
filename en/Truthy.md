TOPIC: Truthy
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Gacel Perfinian; gacelperfinian@mozilla.net; mdn:gacelperfinian
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz

# Truthy

In JavaScript, a **truthy** value is a value that is considered  `true` when encountered in a
Boolean context. All values are truthy unless they are defined as falsy (i.e., except for `false`,
`0`, `""`, `null`, `undefined`, and `NaN`).

JavaScript uses type coercion in Boolean contexts.

Examples of truthy values in JavaScript (which will be coerced to true in boolean contexts,
and thus execute the `if` block):

```javascript
if (true)
if ({})
if ([])
if (42)
if ("0")
if (new Date())
if (-42)
if (12n)
if (3.14)
if (-3.14)
if (Infinity)
if (-Infinity)
```

## See Also

- Falsy
- Coercion
- Boolean
