TOPIC: Hoisting
AUTHORS: YunHyeok Kwak; rev1c0sm0s@gmail.com; github:arin-kwak
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Neville Lee; nevillealee@gmail.com; github:Nevillealee
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Rick Waldron; waldron.rick@gmail.com; github:rwaldron
         Subham Tripathi; subham.bca@gmail.com; github:gitsubham
         Vani Ananthuni; vaniananthuni@mozilla.net; mdn:vaniananthuni
         RAJKISHOR SAHU; rajkishor09@mozilla.net; mdn:rajkishor09
         Julie Myers; SnoopyRules@mozilla.net; mdn:SnoopyRules
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone

# Hoisting

Hoisting is a term you will not find used in any normative specification prose prior to
[ECMAScript® 2015 Language Specification](http://www.ecma-international.org/ecma-262/6.0/index.html).
Hoisting was thought up as a general way of thinking
about how execution contexts (specifically the creation and execution phases) work in JavaScript.
However, the concept can be a little confusing at first.

Conceptually, for example, a strict definition of hoisting suggests that variable and function
declarations are physically moved to the top of your code, but this is not in fact what happens.
Instead, the variable and function declarations are put into memory during the compile phase,
but stay exactly where you typed them in your code.

## Learn More

### Technical example

One of the advantages of JavaScript putting function declarations into memory before it executes any
code segment is that it allows you to use a function before you declare it in your code. For example:

```javascript
function catName(name) {
  console.log("My cat's name is " + name);
}

catName("Tigger");

/*
The result of the code above is: "My cat's name is Tigger"
*/
```

The above code snippet is how you would expect to write the code for it to work. Now, let's see what
happens when we call the function before we write it:

```javascript
catName("Chloe");

function catName(name) {
  console.log("My cat's name is " + name);
}
/*
The result of the code above is: "My cat's name is Chloe"
*/
```

Even though we call the function in our code first, before the function is written, the code still works.
This is because of how context execution works in JavaScript.

Hoisting works well with other data types and variables. The variables can be initialized and used
before they are declared.

### Only Declarations Are Hoisted

JavaScript only hoists declarations, not initializations. If a variable is declared and initialized
after using it, the value will be undefined. For example:

```javascript
console.log(num); // Returns undefined
var num;
num = 6;
If you declare the variable after it is used, but initialize it beforehand, it will return the value:

num = 6;
console.log(num); // returns 6
var num;
Below are more examples demonstrating hoisting.

//Example 1 - Does not hoist
var x = 1; // Initialize x
console.log(x + " " + y); // '1 undefined'
var y = 2; // Initialize y
//This will not work as JavaScript only hoists declarations

//Example 2 - Hoists
var num1 = 3; //Declare and initialize num1
num2 = 4; //Initialize num2
console.log(num1 + " " + num2); //'3 4'
var num2; //Declare num2 for hoisting

//Example 3 - Hoists
a = 'Cran'; //Initialize a
b = 'berry'; //Initialize b
console.log(a + "" + b); // 'Cranberry'
var a, b; //Declare both a & b for hoisting
```

### Technical Reference

- [JavaScript: Understanding the Weird Parts](https://www.udemy.com/understand-javascript/) —
Udemy.com Course
- [var statement](https://wiki.developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var)
— MDN
- [function statement](https://wiki.developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)
— MDN
