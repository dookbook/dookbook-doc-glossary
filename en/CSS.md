TOPIC: Cascading Style Sheets
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Ali; alispivak@mozilla.net; mdn:alispivak
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Nickolay Ponomarev; asqueella@gmail.com; github:nickolay
         Rolfe Dlugy-Hegwer; rolfedh@github.com; github:rolfedh
         Julia Buchner; PetiPandaRou@mozilla.net; mdn:PetiPandaRou
         Liao Yazhi; 1594435860@qq.com; github:liaoyazhi

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

## CSS Property

A **CSS property** is a characteristic (like `color`) whose associated value defines one
aspect of how the browser should display the element.

## Learn More

- [CSS on Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [The CSS Working Group current work](http://www.w3.org/Style/CSS/current-work)
- [MDN CSS文档](https://developer.mozilla.org/en-US/docs/Web/CSS "MDN CSS文档")
