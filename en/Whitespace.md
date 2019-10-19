TOPIC: Whitespace
AUTHORS: Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Maxwell Anderson; maxwell.brayden.anderson@gmail.com; github:Maxgy
         Hiten; hnk23@protonmail.com; github:hiten3
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09

# Whitespace

**Whitespace** is a set of characters used to show horizontal or vertical spaces between other
characters. They are often used to separate tokens in HTML, CSS, JavaScript, and other computer languages.

## In HTML

[HTML Living Standard](https://html.spec.whatwg.org/) specifies 5 characters as the ASCII whitespace:
U+0009 TAB, U+000A LF,
U+000C FF, U+000D CR, and U+0020 SPACE. In text contents, they are treated as normal space characters
and sequential whitespaces are collapsed as a single space in many case (and this behavior can be
changed by `white-space` CSS property. They are also used as a separator of an element name
and attributes in a element, of class names, etc.
