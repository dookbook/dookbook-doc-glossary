TOPIC: Mixin
AUTHORS: Kamran Tahir; EvilSpark@github.com; github:EvilSpark
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Teoli; teoli@mozilla.net; mdn:teoli
         Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz

# Mixin

A mixin is a class or interface in which some or all of its methods and/or properties are
unimplemented, requiring that another class or interface provide the missing implementations.
The new class or interface then includes both the properties and methods from the mixin as well as
those it defines itself. All of the methods and properties are used exactly the same regardless of
whether they're implemented in the mixin or the interface or class that implements the mixin.

The advantage to mixins is that they can be used to simplify the design of APIs in which multiple
interfaces need to include the same methods and properties.

For example, the `WindowOrWorkerGlobalScope` mixin is used to provide methods and properties
that need to be available on both the `Window` and `WorkerGlobalScope` interfaces.
The mixin is implemented by both of those interfaces.

## Learn More

### General Knowledge

- [Mixin](http://en.wikipedia.org/wiki/Mixin) on Wikipedia
