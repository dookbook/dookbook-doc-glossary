TOPIC: Cascading Style Sheets

# Cascading Style Sheets (CSS)

**CSS** (**Cascading Style Sheets**) is a *declarative language* that controls how webpages look in the
browser. The browser applies CSS style declarations to selected elements to display them properly.
**CSS** is one of the three core *[Web](/en/glossary/World_Wide_Web) technologies*, along with **[[HTML]]**
and **[[JavaScript]]**. CSS usually styles *HTML elements*, but can be also used with other markup
languages like *[[SVG]]* or *[[XML]]*.

## CSS Rule

A **CSS rule** is a set of **declarations** associated with a **selector**.
A **style declaration** contains the **properties** and their **values**.

![CSS Rule](/media/glossary__css-rule.png)

Note the syntax:

- Each rule set (apart from the selector) must be wrapped in **curly braces** (**`{}`**).
- Within each declaration, you must use a **colon** (**`:`**) to separate the property from its values.
- Within each rule set, you must use a **semicolon** (**`;`**) to separate each
declaration from the next one.

"*Cascading*" refers to the *rules* that govern how selectors are **prioritized** to change a page's
appearance. This is a very important feature, since a complex website can have thousands of CSS rules.

## CSS Selector

A **CSS selector** is the part of a CSS rule that describes what elements in a document
the rule will match.

### Types of CSS Selectors

| Selector name | What does it select | Example |
| :-- | :-- | :-- |
| **Type selector** (or **element selector**) | All HTML element(s) of the specified type. | `p` to select `<p>` |
| **Class selector** | The element(s) on the page with the specified `class`. | `p.class-name` to select `<p class="class-name">` |
| **ID selector** | The element on the page with the specified ID `id`. | `#id-name` to select `<p id="id-name">` |
| **Attribute selector** | The element(s) on the page with the specified attribute. | `img[src=img.png]` to select `<img src="img.png">` |
| **Pseudo class selector** | The specified element(s), but only when in the specified state. | `a:hover` to select `<a>`, but only when the mouse pointer is hovering over the link. |
| **Pseudo element selector** | The specific part of the selected element(s). | `p::first-line` to select the first line of every `<p>` element. |

- Basic selectors
    - [Universal selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Universal_selectors)
    `* ns|* *|*`
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

## CSS Property

A **CSS property** is a characteristic (like `color`) whose associated value defines one
aspect of how the browser should display the element.

## Learn More

- [CSS on Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [The CSS Working Group current work](http://www.w3.org/Style/CSS/current-work)
- [CSS Selectors Level 3 - W3C CSS Work Group](https://drafts.csswg.org/selectors-3/ "CSS Selector Level 3")
- [MDN CSS文档](https://developer.mozilla.org/en-US/docs/Web/CSS "MDN CSS文档")
