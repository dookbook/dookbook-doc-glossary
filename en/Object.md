TOPIC: Object-Oriented Programming
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Liao Yazhi; 1594435860@qq.com; github:Liaoyazhi
         Li Yun; leven.cn@gmail.com; github:leven-cn

# Object-Oriented Programming

**Object-Oriented Programming** (**OOP**) is *an approach in programming* in which data is encapsulated
within objects and the **object** itself is operated on, rather than its component parts.

## Object

**Object** refers to a **data structure** containing data and instructions for working with the data.
Objects sometimes refer to real-world things, for example a car or map object in a racing game.
[[JavaScript]], [[Java]], C++, and [[Python]] are examples of object-oriented programming languages.

## Property

A **property** is a characteristic of an *object*, often describing attributes
associated with a data structure.

There are two kinds of properties:

- **Instance properties** hold data that are specific to a given object instance.
- **Static properties** hold data that are shared among all object instances.

A property has a *name* (a string) and a *value* (primitive, method, or object reference).
Note that when we say that "a property holds an object", that is shorthand for "a
property holds an object reference".  This distinction matters because the original
referenced object remains unchanged when you change the property's value.

## Method

A **method** is a function which is a property of an object. There are two kind of methods: *Instance
Methods* which are built-in tasks performed by an object instance, or *Static Methods* which are tasks
that are called directly on an object constructor.

!!! info
    In [[JavaScript]] functions themselves are objects, so, in that context, a method is
    actually an object reference to a function.

### Static Method

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

## Class

In object-oriented programming, a **class** defines an object's **characteristics**.
Class is *a template definition of an object's properties and methods*,
the "blueprint" from which other more specific instances of the object are drawn.

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

## Inheritance

**Inheritance** is a major feature of *object-oriented programming*.  **Data [[abstraction]]** can
be carried up several levels, that is, classes can have **superclasses** and **subclasses**.

As an app developer, you can choose which of the superclass's attributes and methods to keep and add
your own, making class definition very flexible. Some languages let a class inherit from more than
one parent (**multiple inheritance**).

## Object Reference

A link to an **object**. Object references can be used exactly like the linked objects.

The concept of **object references** becomes clear when assigning the same object to more than one
**property**. Rather than holding a copy of the object, each assigned property holds object references
that link to the same object, so that when the object changes all properties referring
to the object reflect the change.

## Learn More

- [Object-oriented programming on Wikipedia](https://en.wikipedia.org/wiki/Object-oriented%20programming)
- [Class-Based Programming on Wikipedia](https://en.wikipedia.org/wiki/Class-based_programming)
- [Property (Programming) on Wikipedia](https://en.wikipedia.org/wiki/Property%20(programming))
- [Method (Computer Programming) on Wikipedia](https://en.wikipedia.org/wiki/Method%20(computer%20programming))
- [Constructor for OOP on Wikipedia](https://en.wikipedia.org/wiki/Constructor_%28object-oriented_programming%29)
- [Instance on Wikipedia](https://en.wikipedia.org/wiki/Instance%20(computer%20science))
- [Reference (Computer Science) on Wikipedia](https://en.wikipedia.org/wiki/Reference%20(computer%20science))
