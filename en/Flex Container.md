TOPIC: Flex Container
AUTHORS: Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills

# Flex Container

A flexbox layout is defined using the flex or `inline-flex` values of the `display` property on the
parent item. This element then becomes a **flex container**,
and each one of its children becomes a flex item.

A value of `flex` causes the element to become a block level flex container, and `inline-fle`x an
inline level flex container. These values create a **flex formatting context** for the element,
which is similar to a block formatting context in that floats will not intrude into the container,
and the margins on the container will not collapse with those of the items.

## Learn More

### Property Reference

- [`align-content`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/align-content)
- [`align-items`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/align-items)
- [`flex`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/flex)
- [`flex-direction`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/flex-direction)
- [`flex-flow`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/flex-flow)
- [`flex-wrap`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/flex-wrap)
- [`justify-content`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/justify-content)

### Further Reading

- CSS Flexbox Guide: [Basic Concepts of Flexbox](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)
- CSS Flexbox Guide: [Aligning items in a flex container](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Aligning_Items_in_a_Flex_Container)
- CSS Flexbox Guide: [Mastering wrapping of flex items](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Mastering_Wrapping_of_Flex_Items)
