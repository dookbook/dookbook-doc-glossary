TOPIC: Intrinsic Size
AUTHORS: Rafey Iqbal Rahman; RafeyIqbalRahman@mozilla.net; mdn:RafeyIqbalRahman
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills

# Intrinsic Size

In CSS, the intrinsic size of an element is the size it would be based on its content, if no
external factors were applied to it.

How intrinsic sizes are calculated is defined in the [CSS Intrinsic and Extrinsic Sizing Specification](https://www.w3.org/TR/css-sizing-3/#intrinsic-sizes).

Intrinsic sizing takes into account the `min-content` and max-content size of an element. For text
the `min-content` size would be if the text wrapped as small as it can in the inline direction without
causing an overflow, doing as much soft-wrapping as possible. For a box containing a string of text,
the `min-content` size would be defined by the longest word. The keyword value of `min-content` for
the `width` property will size an element according to the `min-content` size.

The `max-content` size is the opposite — in the case of text, this would have the text display as
wide as possible, doing no soft-wrapping, even if an overflow was caused. The keyword value
`max-content` exposes this behavior.
