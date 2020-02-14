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

## Learn More

- [CSS on Wikipedia](https://en.wikipedia.org/wiki/CSS)
