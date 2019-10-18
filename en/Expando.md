TOPIC: Expando
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer

# Expando

Expando properties are properties added to DOM nodes with JavaScript, where those properties are not
part of the object's DOM specification:

```javascript
window.document.foo = 5; // foo is an expando
```

The term may also be applied to properties added to objects without respecting the object's original
intent, such as non-numeric named properties added to an Array.
