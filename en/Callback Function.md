TOPIC: Callback Function
AUTHORS: Vito Traino; avtraino@github.com; github:avtraino
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Aijaz Bin Qasim; aijaz.ali@hotmail.com; github:aijazbinqasim
         Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Keith Rosenberg; netpoetica@mozilla.net; mdn:netpoetica
         Pushpita Dey; PushpitaPikuDey@mozilla.net; mdn:PushpitaPikuDey

# Callback Function

A callback function is a function passed into another function as an argument, which is then invoked
inside the outer function to complete some kind of routine or action.

Here is a quick example:

```javascript
function greeting(name) {
  alert('Hello ' + name);
}

function processUserInput(callback) {
  var name = prompt('Please enter your name.');
  callback(name);
}

processUserInput(greeting);
```

The above example is a synchronous callback, as it is executed immediately.

Note, however, that callbacks are often used to continue code execution after an asynchronous
operation has completed — these are called asynchronous callbacks. A good example is the callback
functions executed inside a `.then()` block chained onto the end of a promise after that promise
fulfills or rejects. This structure is used in many modern web APIs, such as `fetch()`.

## Learn More

### General Knowledge

- [callback](https://en.wikipedia.org/wiki/Callback_(computer_programming)) on Wikipedia
