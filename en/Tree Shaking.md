TOPIC: Tree Shaking
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Max R; Damnful@github.com; github:Damnful
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Andrea Law; andrealaw@mozilla.net; mdn:andrealaw

# Tree Shaking

**Tree shaking** is a term commonly used within a JavaScript
context to describe the removal of dead code.

It relies on the import and export statements in ES2015 to detect if code modules are
exported and imported for use between JavaScript files.

In modern JavaScript applications, we use module bundlers (e.g., [webpack](https://webpack.js.org/)
or [Rollup](https://github.com/rollup/rollup))
to automatically remove dead code when bundling multiple JavaScript files into single files.
This is important for preparing code that is production ready,
for example with clean structures and minimal file size.

## Learn More

### General Knowledge

- ["Benefits of dead code elimination during bundling"](http://exploringjs.com/es6/ch_modules.html#_benefit-dead-code-elimination-during-bundling)
in Axel Rauschmayer's book: "Exploring JS: Modules"

### Technical Reference

- [tree shaking implementation with webpack](https://webpack.js.org/guides/tree-shaking/)
