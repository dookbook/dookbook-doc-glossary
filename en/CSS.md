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

| Selector | What does it select | Example |
| :-- | :-- | :-- |
| **Type selector** (or **element selector**) (**`<>`**) | All HTML element(s) of the specified type (or node name, tag name). | `p` selects `<p>` |
| **Class selector** (**`.`**) | The element(s) on the page with the specified `class`. | `p.class-name` { style properties } selects `<p class="class-name">` |
| **ID selector** (**`#`**) | The element on the page with the specified ID `id`. | `#id-name` selects `<p id="id-name">` |
| **Attribute selector** (**`[]`**) | The element(s) on the page with the specified attribute. | `img[src=img.png]` selects `<img src="img.png">` |
| **Pseudo class selector** (**`:`**) | The specified element(s), but only when in the specified state. | `a:hover` selects `<a>`, but only when the mouse pointer is hovering over the link. |
| **Pseudo element selector** (**`::`**) | The specific part of the selected element(s). | `p::first-line` selects the first line of every `<p>` element. |
| **Universal selectors** (**`*`**) | Matches elements of any type. | `*` selects all elements. |

- Basic selectors
    - [](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Universal_selectors)
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

### CSS Attribute Selector

| Syntax | Description | Example |
| :-- | :-- | :-- |
| `[attr]` | Represents elements with an attribute name of `attr`. | `a[title]` selects `<a>` elements with a `title` attribute. |
| `[attr=value]` | Represents elements with an attribute name of `attr` whose value is exactly `value`. | `a[href="https://example.org"]` selects `<a>` elements with an `href` matching `https://example.org`. |
| `[attr~=value]` | Represents elements with an attribute name of `attr` whose value is a *whitespace*-separated list of words, one of which is exactly `value`. | `a[class~="logo"]` selects `<a>` elements whose `class` attribute contains the word `logo`. |
| `[attr|=value]` | Represents elements with an attribute name of `attr` whose value can be exactly `value` or can begin with `value` immediately followed by a **hyphen**, **`-`** (*`U+002D`*). It is often used for *language subcode* matches. | `div[lang|="zh"]` selects all `<div>` elements in Chinese, whether simplified (`zh-CN`) or traditional (`zh-TW`). |
| `[attr^=value]` | Represents elements with an attribute name of `attr` whose value is prefixed (preceded) by `value`. | `a[href^="#"]` selects all `<a>` elements with an `href` beginning with `#`. |
| `[attr$=value]` | Represents elements with an attribute name of `attr` whose value is suffixed (followed) by `value`. | `a[href$=".org"]` selects all `<a>` elements with an `href` ending `.org`. |
| `[attr*=value]` | Represents elements with an attribute name of `attr` whose value contains **at least one occurrence** of `value` within the string. | `a[href*="example"]` selects all `<a>` elements with an `href` containing at least one occurrence of `example`. |
| `[attr operator value i]` (**Selectors Level 4 added**) | Adding an **`i`** (or **`I`**) before the closing bracket causes the `value` to be compared **case-insensitively** (for characters within the ASCII range). | `a[href*="Example" i]` selects all `<a>` elements with an `href` containing `Example` regardless of capitalization. |
| `[attr operator value s]` (**Selectors Level 4 added**, **experimental API**) | Adding an **`s`** (or **`S`**) before the closing bracket causes the `value` to be compared **case-sensitively** (for characters within the ASCII range). | `a[href*="Example" s]` selects all `<a>` elements with an `href` containing `Example` with matching capitalization. |

## CSS Property

A **CSS property** is a characteristic (like `color`) whose associated value defines one
aspect of how the browser should display the element.

## Learn More

- Book: ***Designing With Web Standards*, Third Edition (2009)**
- [CSS on Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [The CSS Working Group current work](http://www.w3.org/Style/CSS/current-work)
- [CSS Selectors Level 3 - W3C CSS Work Group](https://drafts.csswg.org/selectors-3/ "CSS Selector Level 3")
- [MDN CSS文档](https://developer.mozilla.org/en-US/docs/Web/CSS "MDN CSS文档")
- [W3C CSS Validator](http://jigsaw.w3.org/css-validator/ "W3C CSS Validator")
