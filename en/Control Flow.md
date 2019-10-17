TOPIC: Control Flow
AUTHORS: Julia Buchner; PetiPandaRou@mozilla.net; mdn:PetiPandaRou
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Sue Smith; SueSmith@github.com; github:SueSmith

# Control Flow

The control flow is the order in which the computer executes statements in a script.

Code is run in order from the first line in the file to the last line, unless the computer runs
across the (extremely frequent) structures that change the control flow,
such as conditionals and loops.

For example, imagine a script used to validate user data from a webpage form. The script submits
validated data, but if the user, say, leaves a required field empty, the script prompts them to fill
it in. To do this, the script uses a conditional structure or `if...else`, so that different code
executes depending on whether the form is complete or not:

```javascript
if (field==empty) {
    promptUser();
} else {
    submitForm();
}
```

A typical script in JavaScript or PHP (and the like) includes many control structures, including
conditionals, loops and functions. Parts of a script may also be set to execute when events occur.

For example, the above excerpt might be inside a function that runs when the user clicks the
**Submit** button for the form. The function could also include a loop, which iterates through
all of the fields in the form, checking each one in turn. Looking back at the code in the `if` and
`else` sections, the lines `promptUser` and `submitForm` could also be calls to other functions in
the script. As you can see, control structures can dictate complex flows of processing even with
only a few lines of code.

Control flow means that when you read a script, you must not only read from start to finish but also
look at program structure and how it affects order of execution.

## Learn More

### General Knowledge

- [Control Flow](https://en.wikipedia.org/wiki/Control%20flow) on Wikipedia

### Technical Reference

- [JavaScript Reference - Control flow](https://wiki.developer.mozilla.org/en-US/docs/Web/JavaScript/Reference#Control_flow)
on MDN

### Learn About It

- [Statements (Control flow)](https://wiki.developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Statements)
on MDN
