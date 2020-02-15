TOPIC: Cascading Style Sheets

# Cascading Style Sheets (CSS)

**CSS** (**Cascading Style Sheets**) is a *declarative language* that controls how webpages look in the
browser. The browser applies CSS style declarations to selected elements to display them properly.

**CSS** is one of the three core *[Web](/en/glossary/World_Wide_Web) technologies*, along with **[[HTML]]**
and **[[JavaScript]]**. CSS usually styles *HTML elements*, but can be also used with other markup
languages like *[[SVG]]* or *[[XML]]*.

## CSS Rule

A **CSS rule** is a set of **properties** associated with a **selector**.
A **style declaration** contains the **properties** and their **values**,
which determine how a webpage looks.

```css
selector {
  property: value;
  ...
}
```

![CSS Rule](/media/glossary__css-rule.gif)

Here is an example that makes every
HTML paragraph yellow against a black background:

```css
/* The selector "p" indicate that all paragraphs in the document will be affected by that rule */
p {
  /* The "color" property defines the text color, in this case yellow. */
  color: yellow;

  /* The "background-color" property defines the background color, in this case black. */
  background-color: black
}
```

"*Cascading*" refers to the *rules* that govern how selectors are **prioritized** to change a page's
appearance. This is a very important feature, since a complex website can have thousands of CSS rules.

## CSS Selector

A **CSS selector** is the part of a CSS rule that describes what elements in a document
the rule will match. The matching elements will have the rule's specified style applied to them.

Consider this CSS:

```css
p {
  ...
}

div.warning {
  ...
}

#customized {
  ...
}
```

The selectors here are `"p"` (which applies the style to the text inside any
`<p>` element), `"div.warning"` (which applies the style to all `<div>` element with the
class `"warning"`), and `"#customized"` (which applies the
style to the element with the `id` `"customized"`).

We can then apply this CSS to some HTML, such as:

```html
<p>This is happy text.</p>

<div class="warning">
  Be careful! There are wizards present, and they are quick to anger!
</div>

<div id="customized">
  <p>This is happy text.</p>
  <div class="warning">
    Be careful! There are wizards present, and they are quick to anger!
  </div>
</div>
```

### Types of CSS Selectors

- Basic selectors
    - [Type selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Type_selectors) `element-name`
    - [Class selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Class_selectors) `.class-name`
    - [ID selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/ID_selectors) `#id-name`
    - [Universal selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Universal_selectors)
    `* ns|* *|*`
    - [Attribute selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors)
    `[attr=value]`
    - [State selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)
    `a:active, a:visited`
- Grouping
    - [Grouping selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Grouping_selectors)
  `A, B`
- Combinators
    - [Adjacent sibling selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Adjacent_sibling_selectors)
    `A + B`
    - [General sibling selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/General_sibling_selectors)
    `A ~ B`
    - [Child selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Child_selectors)
    `A > B`
    - [Descendant selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Descendant_selectors)
    `A B`
- Pseudo
    - [Pseudo-classes](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes): **`:`**
    - [Pseudo-elements](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements): **`::`**

## CSS Property

A **CSS property** is a characteristic (like `color`) whose associated value defines one
aspect of how the browser should display the element.

## Learn More

- [CSS on Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [The CSS Working Group current work](http://www.w3.org/Style/CSS/current-work)
- [CSS Selectors Level 3 - W3C CSS Work Group](https://drafts.csswg.org/selectors-3/ "CSS Selector Level 3")
- [MDN CSS文档](https://developer.mozilla.org/en-US/docs/Web/CSS "MDN CSS文档")
