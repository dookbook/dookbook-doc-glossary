TOPIC: Cross Axis
AUTHORS: Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills

# Cross Axis

The cross axis in flexbox runs perpendicular to the main axis, therefore if your
`flex-direction` is either `row` or `row-reverse` then the cross axis runs down the columns.

![Alt Text](https://mdn.mozillademos.org/files/15710/Basics3.png)

If your main axis is `column` or `column-reverse` then the cross axis runs along the rows.

![Alt Text](https://mdn.mozillademos.org/files/15711/Basics4.png)

Alignment of items on the cross axis is achieved with the `align-items` property on the flex
container or `align-self` property on individual items. In the case of a multi-line flex container,
with additional space on the cross axis, you can use `align-content` to control the spacing of the rows.

## Learn More

### Property Reference

- [`align-content`](https://developer.mozilla.org/en-US/docs/Web/CSS/align-content)
- [`align-items`](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items)
- [`align-self`](https://developer.mozilla.org/en-US/docs/Web/CSS/align-self)
- [`flex-wrap`](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-wrap)
- [`flex-direction`](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-direction)
- [`flex`](https://developer.mozilla.org/en-US/docs/Web/CSS/flex)

### Further Reading

- CSS Flexbox Guide: [Basic Concepts of Flexbox](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)
- CSS Flexbox Guide: [Aligning items in a flex container](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Aligning_Items_in_a_Flex_Container)
- CSS Flexbox Guide: [Mastering wrapping of flex items](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Mastering_Wrapping_of_Flex_Items)
