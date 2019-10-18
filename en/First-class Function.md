TOPIC: First-class Function
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Thuy; thuy@thuy.life; github:ThuyNT13
         Emerson Pereira; emerson.mdca@gmail.com; github:emersoonpereiira
         Justin; janstilau@github.com; github:janstilau
         Yahya Elharony; yahya@elharony.com; github:elharony

# First-class Function

A programming language is said to have [First-class functions](url) when functions in that language
are treated like any other variable. For example, in such a language, a function can be passed as an
argument to other functions, can be returned by another function and can be
assigned as a value to a variable.

## Example | Assign a function to a variable

JavaScript

```javascript
const foo = function() {
   console.log("foobar");
}
// Invoke it using the variable
foo();
```

We assigned an `Anonymous Function` in a `Variable`, then we used that variable to invoke the
function by adding parentheses `()` at the end.

!!! note
    **Even if your function was named**, you can use the variable name to invoke it. Naming it will be
    helpful when debugging your code. But it won't affect the way we invoke it.

## Example | Pass a function as an Argument

JavaScript

```javascript
function sayHello() {
   return "Hello, ";
}
function greeting(helloMessage, name) {
  console.log(helloMessage() + name);
}
// Pass `sayHello` as an argument to `greeting` function
greeting(sayHello, "JavaScript!");
```

We are passing our `sayHello()` function as an argument to the `greeting()` function, this explains
how we are treating the function as a `value`.

!!! note
    The function that we pass as an argument to another function, is called a [Callback function](url).
    `sayHello` is a Callback function.

## Example | Return a function

### JavaScript

```javascript
function sayHello() {
   return function() {
      console.log("Hello!");
   }
}
```

In this example; We need to return a function from another function - We can return a function
because we treated function in JavaScript as a `value`.

!!! note
    A function that returns a function is called a **Higher-Order Function**.
    Back to our example; Now, we need to invoke `sayHello`
    function and its returned `Anonymous Function`. To do so, we have two ways:

### 1- Using a variable

```javascript
const sayHello = function() {
   return function() {
      console.log("Hello!");
   }
}
const myFunc = sayHello();
myFunc();
```

This way, it returns the `Hello!` message.

!!! note
    You have to use another variable. If you invoked `sayHello` directly, it would return the function
    itself **without invoking its returned function**.

### 2- Using double parentheses

```javascript
function sayHello() {
   return function() {
      console.log("Hello!");
   }
}
sayHello()();
```

We are using double parentheses `()()` to invoke the returned function as well.

## Learn More

### General Knowledge

- [First-class functions](https://en.wikipedia.org/wiki/First-class_function) on Wikipedia
