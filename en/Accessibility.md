TOPIC: Web Accessibility
       Accessibility Object Model

# Web Accessibility

**Web Accessibility** (*A11Y*) refers to *best practices* for keeping a website usable despite physical
and technical restrictions. Web accessibility is formally defined and discussed at the [[W3C]] through
the *[[Web Accessibility Initiative]]* (*[[WAI]]*).

## Accessibility Object Model (AOM)

The **accessibility tree**, or **accessibility object model (AOM)**,
contains *accessibility-related* information for most HTML elements.

Browsers convert markup into an internal representation called the *DOM tree*.
The DOM tree contains
objects for all the markup’s elements, attributes, and text nodes. Browsers then create an
accessibility tree based on the DOM tree, which is used by platform-specific *Accessibility APIs* for
assistive technologies, such as screen readers.

There are four things in an accessibility tree object:

name
:   How can we refer to this thing? For instance, a link with the text 'Read more' will have
    'Read more' assist name (more on how names are computed in the
    [Accessible Name and Description Computation spec](https://www.w3.org/TR/accname-1.1/)).

description
:   How do we describe this element, if we want to add anything to the name? The description of a table
    could explain what kind of info that table offers.

role
:   What kind of thing is it? For example, is it a button, a nav bar, or a list of items?

state
:   Does it have state? Think checked/unchecked for checkboxes, or collapsed/expanded
    for the `<summary>` element.

Additionally, the accessibility tree often contains information on what can be done with an
element: a link can be followed, a text input can be typed into, etc.

## Learn More

- [Accessibility on MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility)
- [Web accessibility on Wikipedia](https://en.wikipedia.org/wiki/Web%20accessibility)
- [Web Accessibility - ARIA on MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)
- [The Web Accessibility Initiative homepage](http://www.w3.org/WAI/)
- [The WAI-ARIA Recommendation](http://www.w3.org/TR/wai-aria/)
