TOPIC: Object
       Object-Oriented Programming
AUTHORS: Julia Buchner; PetiPandaRou@mozilla.net; mdn:PetiPandaRou
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Prashant Bhende; pbmj5233@mozilla.net; mdn:pbmj5233
         Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Li Yun; leven.cn@gmail.com; github:leven-cn

# Object

**Object** refers to a **data structure** containing data and instructions for working with the data.
Objects sometimes refer to real-world things, for example a car or map object in a racing game.
[[JavaScript]], [[Java]], C++, [[Python]], and Ruby are examples of object-oriented programming languages.

## Object-Oriented Programming

**Object-Oriented Programming** (**OOP**) is *an approach in programming* in which data is encapsulated
within objects and the **object** itself is operated on, rather than its component parts.

### Constructor

A **constructor** belongs to a particular class object that is instantiated. The constructor
initializes this object and can provide access to its private information. The concept of a
constructor can be applied to most object-oriented programming languages. Essentially,
a constructor in [[JavaScript]] is usually declared at the instance of a class.

#### Constructor in JavaScript

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

## Learn More

- [Object-oriented programming on Wikipedia](https://en.wikipedia.org/wiki/Object-oriented%20programming)
- [Constructor for OOP on Wikipedia](https://en.wikipedia.org/wiki/Constructor_%28object-oriented_programming%29)
