TOPIC: Cascading Style Sheets

# Cascading Style Sheets (CSS)

**CSS** (**Cascading Style Sheets**) is a *declarative language* that controls how webpages look in the
browser. The browser applies CSS style declarations to selected elements to display them properly.
**CSS** is one of the three core *[Web](/en/glossary/World_Wide_Web) technologies*, along with **[[HTML]]**
and **[[JavaScript]]**. CSS usually styles *HTML elements*, but can be also used with other markup
languages like *[[SVG]]* or *[[XML]]*.

## Apply CSS to HTML Document

There are several ways to introduce CSS, and the priority is from high to low:

1. Inline styles ([**`style` attribute**](/en/webfrontend/style_attribute))
2. Inner stylesheets ([**`<style>`**](/en/webfrontend/<style>) element)
3. **External stylesheets** ([**`<link>`**](/en/webfrontend/<link>) element) (**Recommended**)

```html
<!-- Example: Apply CSS -->

<!-- External stylesheet -->
<head>
  <link href="style.css" ref="stylesheet">
</head>

<!-- Inner stylesheet, priority higher than external stylesheet -->
<style>
  p {
    color: black;
  }
</style>

<!-- Inline styles, highest priority -->
<p style="color: black;">A paragraph.</p>
```

```css
/* style.css */
p {
  color: black;
}
```

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
| **Type selector** (or **element selector**) (**`< >`**) | all HTML element(s) of the specified type (or node name, tag name). | `p` selects `<p>` |
| **Class selector** (**`.`**) | the element(s) on the page with the specified `class`. | `p.class-name` { style properties } selects `<p class="class-name">` |
| **ID selector** (**`#`**) | the element on the page with the specified ID `id`. | `#id-name` selects `<p id="id-name">` |
| **Attribute selector** (**`[ ]`**) | the element(s) on the page with the specified attribute. | `img[src=img.png]` selects `<img src="img.png">` |
| **Pseudo class selector** (**`:`**) | the specified element(s), but only when in the specified state. | `a:hover` selects `<a>`, but only when the mouse pointer is hovering over the link. |
| **Pseudo element selector** (**`::`**) | the specific part of the selected element(s). | `p::first-line` selects the first line of every `<p>` element. |
| **Universal selectors** (**`*`**) | match elements of any type. | `*` selects all elements. |
| **Descendant selectors** (or **descendant combinator**) (**`A B`**) | typically represented by a *single space* character — combines two selectors such that elements matched by the second selector are selected if they have an **ancestor** (parent, parent's parent, parent's parent's parent, etc) element matching the first selector. | `ul.my-things li` lists items that are descendants of the "`my-things`" list. |
| **Child selectors** (or **child combinator**) (**`A > B`**) | match only those elements matched by the second selector that are **the direct children** of elements matched by the first. | `ul.my-things > li` lists items that are children of the "`my-things`" list. |
| **General sibling selectors** (**`A ~ B`**) | match the second element only if it follows the first element (though not necessarily immediately), and both are children of the same parent element. | `img ~ p` matches paragraphs that are siblings of and subsequent to any image. |
| **Adjacent sibling selectors** (**`A + B`**) | match the second element **only** if it immediately follows the first element, and both are children of the same parent element. | `img + p` matches paragraphs that come immediately after any image. |
| **Grouping selectors** (**`A, B`**) | grouping selectors in a single line or a multiple lines using a comma-separated lists. | `h1, h2` selects all `<h1>`, `<h2>` elements. |

### CSS weights

Regarding CSS weights, it is represented by a four-digit number string (CSS2 is three digits). It is
more like four levels, with values from left to right, the largest on the left, a level greater
than one level, and no digits between the levels. No one can surpass.

| Category | Contribution|
| :-- | :-- |
| **Contribution value inherited or `*`** | 0,0,0,0 |
| **Contribution of each element (tag)** | 0,0,0,1 |
| **Contributing value for each class** | 0,0,1,0 |
| **Contribution value for each ID** | 0,1,0,0 |
| **Contribution value for inline style** | 1,0,0,0 |
| **Each `!Important` contribution value** | ∞  infinity. |

**For example:**

`div ul li`  ----  0,0,0,3 (`div`,`ul`,`li`are all elements, so 0，0，0，1+0，0，0，1+0，0，0，1=0，0，0，3)

`.nav ul li` ----  0,0,1,2 (`.nav`belongs to class，so 0，0，1，0+0，0，0，1+0，0，0，1=0，0，1，2)

`a:hover`    ----  0,0,1,1 (`:hover` belongs to pseudo class selector，`a` belongs to elements，so 0，0，0，1+0，0，1，0=0，0，1，1)

`.nav a`     ----  0,0,1,1 (`.nav` belongs to class selector，so 0，0，1，0+0，0，0，1=0,0,1,1)

`#nav p`     ----  0,1,0,1  (`#nav` belongs to ID，`p` belongs to elements，so 0，1，0，0+0，0，0，1=0,0,1,1)

!!! wran "Attention"
    There are no bases between digits. For example: 0,0,0,5 + 0,0,0,5 =0,0,0,10 instead of 0,0, 1, 0，
    so there will not be 10 [`div`](/en/webfrontend/<div>) that can enter a class selector. Happening.

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

## CSS Comment `/* ... */`

**`/* ... */`** is the CSS comment, which is used to insert comments in the source code.
Comments do not appear in the browser.

CSS Example:

```css
/* This is a comment. */
p {
  text-align: center;  /* This is a comment, too */

  /* This is another comment. */
  color: black;
  font-family: arial;
}
```

## Learn More

- Book: ***Designing With Web Standards*, Third Edition (2009)**
- [CSS on Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [The CSS Working Group current work](http://www.w3.org/Style/CSS/current-work)
- [CSS Selectors Level 3 - W3C CSS Work Group](https://drafts.csswg.org/selectors-3/ "CSS Selector Level 3")
- [MDN CSS文档](https://developer.mozilla.org/en-US/docs/Web/CSS "MDN CSS文档")
- [W3C CSS Validator](http://jigsaw.w3.org/css-validator/ "W3C CSS Validator")
