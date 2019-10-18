TOPIC: Main Axis
AUTHORS: Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Daniel Palumbi; danpaltor@mozilla.net; mdn:danpaltor
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills

# Main Axis

The main axis in flexbox is defined by the direction set by the `flex-direction` property.
There are four possible values for `flex-direction`. These are:

- `row`
- `row-reverse`
- `column`
- `column-reverse`

Should you choose `row` or `row-reverse` then your main axis will run along the row in the inline direction.

![text](https://mdn.mozillademos.org/files/15708/Basics1.png)

Choose `column` or `column-reverse` and your main axis will run top to bottom of the page in the
block direction.

![text](https://mdn.mozillademos.org/files/15709/Basics2.png)

On the main axis you can control the sizing of flex items by adding any available space to the
items themselves, by way of `flex` properties on the items. Or, you can control the space between
and around items by using the `justify-content` property.

## Learn More

### Property Reference

- [`flex-basis`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/flex-basis)
- [`flex-direction`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/flex-direction)
- [`flex-grow`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/flex-grow)
- [`flex-shrink`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/flex-shrink)
- [`justify-content`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/justify-content)
- [`flex`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/flex)

### Further Reading

- CSS Flexbox Guide: [Basic Concepts of Flexbox](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)
- CSS Flexbox Guide: [Aligning items in a flex container](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Aligning_Items_in_a_Flex_Container)
- CSS Flexbox Guide: [Controlling Ratios of flex items along the main axis](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Controlling_Ratios_of_Flex_Items_Along_the_Main_Ax)
