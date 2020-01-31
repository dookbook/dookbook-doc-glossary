TOPIC: Syntax
       Statement
       Control Flow
       Conditional
       Loop
       Function
       Parameter
       Function Signature
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Jeff; j3485@mozilla.net; mdn:j3485
         Geordanny Ulises Velasquez; geordanny@mozilla.net; mdn:geordanny
         Liao Yazhi; 1594435860@qq.com; github:Liaoyazhi
         Li Yun; leven.cn@gmail.com; github:leven-cn

# Syntax: Statement, Control Flow and Function

**Syntax** specifies the **required combination and sequence of characters** making up *correctly structured
code*. Syntax varies from language to language (e.g., syntax is different in [[HTML]] and [[JavaScript]]).
Syntax applies both to *programming languages* (commands to the computer) and *markup
languages* (document structure information).

Syntax only governs **ordering** and **structure**; the instructions must also be meaningful,
which is the province of semantics.

Code must have correct syntax in order to compile correctly, otherwise a *syntax error* occurs.
Even small errors, like a missing parenthesis, can keep source code from compiling.

Frameworks are said to have a "**clean**" syntax if they produce simple, readable, concise results.
If a codebase uses "a lot of syntax", it requires more characters to achieve the same functionality.

## Statement

In a computer programming language, a **statement** is a line of code commanding a task.
Every program consists of a sequence of statements.

## Control Flow

The **control flow** is the **order** in which the computer executes *statements* in a programming language.

Code is run in order from the first line in the file to the last line, unless the computer runs
across the (extremely frequent) structures that change the control flow.

A typical programming language includes many control structures, including
**conditionals**, **loops** and **functions**.
Parts of a programming language may also be set to execute when
**events** occur.

### Conditional

A **condition** is a set of rules that can interrupt normal code execution or change it, depending
on whether the condition is completed or not.

An instruction or a set of instructions is executed, if a specific condition is fulfilled. Otherwise,
another instruction is executed. It is also possible to repeat the execution of an instruction,
or set of instructions, while a condition is not yet fulfilled.

### Loop

A **loop** is a sequence of instructions that is **continually repeated** until a certain condition
is met in computer programming.
An example would be the process of getting an item of data and changing it,
and then making sure some condition is checked such as, if a counter has reached a prescribed number.

## Function

A **function** is a *code snippet* that can be called by other code or by itself, or a variable that
refers to the function. When a function is called, *arguments* are passed to the function as input,
and the function can optionally return an output. A function in [[JavaScript]] is also an [object](/en/webfrontend/object).

A function name is an *[[identifier]]* declared as part of a *function declaration* or *function expression*.
The function name's *[[scope]]* depends on whether the function name is a declaration or expression.

### Types of Functions

#### Anonymous Function

An **anonymous function** is a function **without a function name**:

```javascript
function () {};

// or using the ECMAScript 2015 arrow notation
() => {};
```

#### Named Function

A **named function** is a function **with a function name**:

```javascript
function foo() {};

// or using the ECMAScript 2015 arrow notation
const foo = () => {};
```

#### Inner / Outer Function

An **inner function** is a function **inside another function** (`square` in this case).
An **outer function** is a function **containing a function** (`addSquares` in this case):

```javascript
function addSquares(a,b) {
   function square(x) {
      return x * x;
   }
   return square(a) + square(b);
};

//Using ECMAScript 2015 arrow notation
const addSquares = (a,b) => {
   const square = x => x*x;
   return square(a) + square(b);
};
```

#### Recursive Function

A **recursive function** is a function **that calls itself**. See [[recursion]].

```javascript
function loop(x) {
   if (x >= 10)
      return;
   loop(x + 1);
};

//Using ECMAScript 2015 arrow notation
const loop = x => {
   if (x >= 10)
      return;
   loop(x + 1);
};
```

#### Immediately Invoked Function Expressions (IIFE)

An **Immediately Invoked Function Expressions** (**IIFE**) is a function that is called directly after
the function is loaded into the browser’s compiler. The way to identify an IIFE is by locating the
extra left and right parenthesis at the end of the function’s declaration.

```javascript
// Error (https://en.wikipedia.org/wiki/Immediately-invoked_function_expression)
/*
​function foo() {
    console.log('Hello Foo');
}();
*/

(function foo() {
    console.log("Hello Foo");
}());

(function food() {
    console.log("Hello Food");
})();
```

If you'd like to know more about IIFEs, check out the following page on Wikipedia:
[Immediately Invoked Function Expression](https://en.wikipedia.org/wiki/Immediately-invoked_function_expression)

### Parameter

A **parameter** is a named variable passed into a *function*. Parameter variables are used to
import arguments into functions.

Note the difference between *parameters* and *arguments*:

- Function parameters are the names listed in the function's definition.
- Function arguments are the real values passed to the function.
- Parameters are initialized to the values of the arguments supplied.

Two kinds of parameters:

input parameters
:   the most common kind; they pass values into functions. Depending on programming language
    input parameters can be passed several ways (e.g., call-by-value, call-by-address, call-by-reference).

output/return parameters
:   primarily return multiple values from a function, but not recommended since they cause confusion

### Function Signature

A **function signature** (or **type signature**, or **method signature**) defines input and
output of functions or methods.

A signature can include:

- **parameters** and their types
- a **return value** and type
- **exceptions** that might be thrown or passed back
- information about the **availability** of the method in an *[[object-oriented programming]]* (such
as the keywords `public`, `static`, or `prototype`).

#### Signatures in JavaScript

[[JavaScript]] is a loosely typed or a dynamic language. That means you don't have to
declare the type of a variable ahead of time. The type will get determined automatically
while the program is being processed. A signature in JavaScript can still give you some
information about the method:

```javascript
MyObject.prototype.myFunction(value)
```

- The method is installed on an object called `MyObject`.
- The method is installed on the `prototype` of `MyObject` (thus it is an instance
method) as opposed to being a static method.
- The name of the method is `myFunction`.
- The method accepts one parameter, which is called `value` and is not further defined.

#### Signatures in Java

In [[Java]], signatures are used to identify methods and classes at the level of the virtual
machine code. You have to declare types of variables in your code in order to be able to
run the Java code. Java is strictly typed and will check any parameters at compilation
time if they are correct.

```java
public static void main(String[] args)
```

- The `public` keyword is an access modifier and indicates that this method can be called by any object.
- The `static` keyword indicates that this method is a class method as opposed to being an instance method.
- The `void` keyword indicates that this method has no return value.
- The name of the method is `main`.
- The method accepts one parameter of type String Array. It is named `args`.

## Learn More

- [Syntax (Programming Language) on Wikipedia](https://en.wikipedia.org/wiki/Syntax%20(programming%20language))
- [Syntax Error on Wikipedia](https://en.wikipedia.org/wiki/Syntax%20error)
- [Statement (Computer Science) on Wikipedia](https://en.wikipedia.org/wiki/Statement%20(computer%20science))
- [Control Flow on Wikipedia](https://en.wikipedia.org/wiki/Control%20flow)
- [Condition on Wikipedia](https://en.wikipedia.org/wiki/Exception_handling#Condition_systems)
- [Immediately Invoked Function Expression on Wikipedia](https://en.wikipedia.org/wiki/Immediately-invoked_function_expression)
- [Difference between parameter and argument on Wikipedia](http://en.wikipedia.org/wiki/Parameter_%28computer_programming%29#Parameters_and_arguments)
- [Type Signature on Wikipedia](https://en.wikipedia.org/wiki/Type%20signature)
- [Parameter-Passing Modes](http://pages.cs.wisc.edu/~hasti/cs368/CppTutorial/NOTES/PARAMS.html)
- [JavaScript Function Parameters](http://www.ryerson.ca/JavaScript/lectures/functions/passByValueOrReference.html)
- [Passing Parameter in JavaScript](http://javascript.about.com/library/bltut08.htm)
