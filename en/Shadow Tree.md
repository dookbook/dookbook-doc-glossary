TOPIC: Shadow Tree
AUTHORS: Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Venugopal Shivashankar; venugopalms@gmail.com; github:venugopalms
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy

# Shadow Tree

A **shadow tree** is a tree of DOM nodes whose topmost node is a **shadow root**; that is,
the topmost node within a **shadow DOM**. A shadow tree is a hidden set of standard DOM nodes which
is attached to a standard DOM node that serves as a host. The hidden nodes are not directly
visible using regular DOM functionality, but require the use of a special Shadow DOM API to access.

Nodes within the shadow tree are not affected by anything applied outside the shadow tree,
and vice versa. This provides a way to encapsulate implementation details, which is especially useful
for custom elements and other advanced design paradigms.

## Learn More

### General Knowledge

- [Using shadow DOM](https://wiki.developer.mozilla.org/en-US/docs/Web/Web_Components/Using_shadow_DOM)

### Technical information

- [`Element.shadowRoot`](https://wiki.developer.mozilla.org/en-US/docs/Web/API/Element/shadowRoot)
and [`Element.attachShadow()`](https://wiki.developer.mozilla.org/en-US/docs/Web/API/Element/attachShadow)
- [`ShadowRoot`](https://wiki.developer.mozilla.org/en-US/docs/Web/API/ShadowRoot)
- [`<slot>`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/slot)
