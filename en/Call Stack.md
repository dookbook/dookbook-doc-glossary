TOPIC: Call Stack
AUTHORS: Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         geoffreyhale; geoffreyhale@github.com; github:geoffreyhale
         Yahya Elharony; yahya@elharony.com; github:elharony
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Andy Prickett; andy@andyprickett.com; github:andyprickett
         Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Sneh Jain; SnehJain@mozilla.net; mdn:SnehJain

# Call Stack

A **call stack** is a mechanism for an interpreter (like the JavaScript interpreter in a web browser)
to keep track of its place in a script that calls multiple functions — what function is currently
being run and what functions are called from within that function, etc.

- When a script calls a function, the interpreter adds it to the call
stack and then starts carrying out the function.

- Any functions that are called by that function are added to the call stack further up,
and run where their calls are reached.

- When the current function is finished, the interpreter takes it off the stack and resumes
execution where it left off in the last code listing.

- If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

## ExampleSection

```javascript
function greeting() {
   // [1] Some codes here
   sayHi();
   // [2] Some codes here
}
function sayHi() {
   return "Hi!";
}

// Invoke the `greeting` function
greeting();

// [3] Some codes here
```

The code above would be executed like this:

1. Ignore all functions, until it reaches the `greeting()` function invocation.

1. Add the `greeting()` function to the call stack list.

   !!! note
      Call stack list:
      -greeting

1. Execute all lines of code inside the `greeting()` function.

1. Get to the `sayHi()` function invocation.

1. Add the `sayHi()` function to the call stack list.

   !!! note
      Call stack list:
      -greeting
      -sayHi

1. Execute all lines of code inside the `sayHi()` function, until reaches its end.

1. Return execution to the line that invoked `sayHi()` and continue
executing the rest of the `greeting()` function.

1. Delete the `sayHi()` function from our call stack list.

   !!! note
      Call stack list:
      -greeting

1. When everything inside the `greeting()` function has been executed, return to its invoking line
to continue executing the rest of the JS code.

1. Delete the `greeting()` function from the call stack list.

   !!! note
      Call stack list:
      EMPTY

We started with an empty Call Stack, and whenever we invoke a function, it is automatically added to
the Call Stack, after executing all of its codes, it is automatically removed from the Call Stack.
At the end, we ended up with an empty stack too.

## Learn More

### General Knowledge

- [call stack](https://en.wikipedia.org/wiki/Call%20stack) on Wikipedia
