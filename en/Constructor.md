TOPIC: Constructor
AUTHORS: Julia Buchner; PetiPandaRou@mozilla.net; mdn:PetiPandaRou
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Prashant Bhende; pbmj5233@mozilla.net; mdn:pbmj5233
         Federico Culloca; federicoculloca@github.com; github:federicoculloca

# Constructor

A **constructor** belongs to a particular class object that is instantiated. The constructor
initializes this object and can provide access to its private information. The concept of a
constructor can be applied to most object-oriented programming languages. Essentially,
a constructor in JavaScript is usually declared at the instance of a class.

## Syntax

```javascript
// This is a generic default constructor class Default
function Default() {
}

// This is an overloaded constructor class Overloaded
// with parameter arguments
function Overloaded(arg1, arg2, ...,argN){
}
```

To call the constructor of the class in JavaScript, use a `new` operator to assign a new object
reference to a variable.

```javascript
function Default() {
}

// A new reference of a Default object assigned to a
// local variable defaultReference
var defaultReference = new Default();
```

## Learn More

### General Knowledge

- [Constructor](https://en.wikipedia.org/wiki/Constructor_%28object-oriented_programming%29) on Wikipedia

### Technical Reference

- [The constructor in object oriented programming for JavaScript](https://wiki.developer.mozilla.org/en-US/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript#The_Constructor)
on MDN
- [New operator in JavaScript](https://wiki.developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/new)
on MDN
