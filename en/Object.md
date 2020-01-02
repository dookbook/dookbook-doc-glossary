TOPIC: Object-Oriented Programming

# Object-Oriented Programming

**Object-Oriented Programming** (**OOP**) is *an approach in programming* in which data is encapsulated
within objects and the **object** itself is operated on, rather than its component parts.

## Object

**Object** refers to a **data structure** containing data and instructions for working with the data.
Objects sometimes refer to real-world things, for example a car or map object in a racing game.
[[JavaScript]], [[Java]], C++, and [[Python]] are examples of object-oriented programming languages.

## Class

In object-oriented programming, a **class** defines an object's **characteristics**. Class is *a template
definition of an object's properties and methods*, the "blueprint" from which other more
specific instances of the object are drawn.

## Constructor

A **constructor** belongs to a particular class object that is instantiated. The constructor
initializes this object and can provide access to its private information. The concept of a
constructor can be applied to most object-oriented programming languages. Essentially,
a constructor in [[JavaScript]] is usually declared at the instance of a class.

### Constructor in JavaScript

```javascript
// This is a generic default constructor class Default
function Default() {
}

// This is an overloaded constructor class Overloaded
// with parameter arguments
function Overloaded(arg1, arg2, ...,argN){
}
```

To call the constructor of the class in [[JavaScript]], use a `new` operator to assign a new object
reference to a variable.

```javascript
function Default() {
}

// A new reference of a Default object assigned to a
// local variable defaultReference
var defaultReference = new Default();
```

## Instance

An object created by a constructor is an instance of that constructor.

## Static Method

A **static method** (or **static function**) is a method defined as a member of an object but is accessible
directly from an API object's constructor, rather than from an object instance created via the constructor.

In a Web API, a static method is one which is defined by an interface but can be called
without instantiating an object of that type first.

Methods called on object instances are called *instance methods*.

For example, in the Notifications API, the `Notification.requestPermission()` method is called on
the actual `Notification` constructor itself — it is a static method:

```javascript
let promise = Notification.requestPermission();
```

The `Notification.close()` method on the other hand, is an instance method — it is called on
an specific notification object instance to close the system notification it represents:

```javascript
let myNotification = new Notification('This is my notification');

myNotification.close();
```

## Learn More

- [Object-oriented programming on Wikipedia](https://en.wikipedia.org/wiki/Object-oriented%20programming)
- [Class-Based Programming on Wikipedia](https://en.wikipedia.org/wiki/Class-based_programming)
- [Constructor for OOP on Wikipedia](https://en.wikipedia.org/wiki/Constructor_%28object-oriented_programming%29)
- [Instance on Wikipedia](https://en.wikipedia.org/wiki/Instance%20(computer%20science))
