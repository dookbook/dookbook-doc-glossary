TOPIC: Static Method
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone

# Static Method

A static method (or static function) is a method defined as a member of an object but is accessible
directly from an API object's constructor, rather than from an object instance created via the constructor.

In a Web API, a static method is one which is defined by an interface but can be called
without instantiating an object of that type first.

Methods called on object instances are called instance methods.

## Examples

In the Notifications API, the N`otification.requestPermission()` method is called on
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
