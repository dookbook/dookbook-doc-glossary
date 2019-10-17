TOPIC: Canonical Order
AUTHORS: Sebastian Zartner; SebastianZ@github.com; github:SebastianZ
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills

# Canonical Order

In CSS, canonical order is used to refer to the order in which separate values need to be specified
(or parsed) or are to be serialized as part of a CSS property value. It is defined by the formal
syntax of the property and normally refers to the order in which
longhand values should be specified as part of a single shorthand value.

For example, `background` shorthand property values are made up of several `background-*`
longhand properties. The canonical order of those longhand values is defined as

1. `background-image`
1. `background-position`
1. `background-size`
1. `background-repeat`
1. `background-attachment`
1. `background-origin`
1. `background-clip`
1. `background-color`

Furthermore, its syntax defines, that if a value for the `background-size` is given,
it **must** be specified **after** the value for the `background-position`,
separated by a slash. Other values may appear in any order.

## Learn More

### General Knowledge

- [What does “canonical order” mean with respect to CSS properties?](https://stackoverflow.com/questions/28963536/what-does-canonical-order-mean-with-respect-to-css-properties)
on Stack Overflow provides useful further discussion
- The [description of the formal syntax used for CSS values](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Value_definition_syntax)
on MDN
