TOPIC: Signature
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Julia Buchner; PetiPandaRou@mozilla.net; mdn:PetiPandaRou
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone
         Teoli; teoli@mozilla.net; mdn:teoli
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         April King; april@pokeinthe.io; github:april

# Signature

The term **signature** can have several meanings depending on the context. It may refer to:

## Signature (functions)

A **function signature** (or type signature, or method signature) defines input and
output of functions or methods.

A signature can include:

- parameters and their types
- a return value and type
- exceptions that might be thrown or passed back
- information about the availability of the method in an object-oriented program (such
as the keywords `public`, `static`, or `prototype`).

### In Depth

Signatures in JavaScript

JavaScript is a loosely typed or a dynamic language. That means you don't have to
eclare the type of a variable ahead of time. The type will get determined automatically
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

Signatures in Java

In Java, signatures are used to identify methods and classes at the level of the virtual
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

## Signature (security)

A **signature**, or digital signature, is a protocol showing that a message is authentic.

From the hash of a given message, the **signing process** first generates a digital
signature linked to the signing entity, using the entity's private key.

On receiving the message, the **verification process**

- authenticates the sender - uses the sender's public key to decrypt the signature and
recover the hash, which can only be created with the sender's private key, and
- checks message integrity - compares the hash with a newly calculated one from the
received document (the two hashes will differ if the document has been tampered with)

The system fails if the private key is compromised or the recipient is deceitfully given
the wrong public key.

## Learn More

- [Signature](https://en.wikipedia.org/wiki/Signature_(disambiguation)) on Wikipedia

### General Knowledge

- [Java internal type signatures](https://en.wikipedia.org/wiki/Type%20signature#Java) on Wikipedia
- [Digital signature](https://en.wikipedia.org/wiki/Digital%20signature) on Wikipedia
- See digest, encryption

### Technical Reference

- [Information security tutorial](https://developer.mozilla.org/en-US/Learn/tutorial/Information_Security_Basics)
