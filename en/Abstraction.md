TOPIC: Abstraction
AUTHORS: Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie

# Abstraction

Abstraction in computer programming is a way to reduce complexity and allow efficient design and
implementation in complex software systems.
It hides the technical complexity of systems behind simpler APIs.

## Advantages of Data Abstraction

- Helps the user to avoid writing low level code.
- Avoids code duplication and increases reusability.
- Can change internal implementation of class independently without affecting the user.
- Helps to increase security of an application or
program as only important details are provided to the user.

## Example

```javascript
class ImplementAbstraction {
  // method to set values of internal members
  set(x, y) {
    this.a = x;
    this.b = y;
  }

  display() {
    console.log('a = ' + this.a);
    console.log('b = ' + this.b);
  }
}

const obj = new ImplementAbstraction();
obj.set(10, 20);
obj.display();
// a = 10
// b = 20
```

## Learn more

### General knowledge

- [abstraction](https://en.wikipedia.org/wiki/Abstraction%20(computer%20science)) on Wikipedia
