TOPIC: Object
       Object-Oriented Programming
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone
         Li Yun; leven.cn@gmail.com; github:leven-cn

# Object

**Object** refers to a **data structure** containing data and instructions for working with the data.
Objects sometimes refer to real-world things, for example a car or map object in a racing game.
[[JavaScript]], [[Java]], C++, [[Python]], and Ruby are examples of object-oriented programming languages.

## Object-Oriented Programming

**Object-Oriented Programming** (**OOP**) is *an approach in programming* in which data is encapsulated
within objects and the **object** itself is operated on, rather than its component parts.

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
