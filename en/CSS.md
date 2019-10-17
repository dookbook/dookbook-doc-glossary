TOPIC: CSS
AUTHORS: Jongryul Yang; urty5656@gmail.com; github:alattalatta
         Takahiro Uemura; Uemmra3@gmail.com; github:Uemmra3
         Красимир Беров; kberov@mozilla.net; mdn:kberov
         Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Ashutosh Chaturvedi; ashutoshchaturvedi@mozilla.net; mdn:ashutoshchaturvedi
         Sergio González Collado; sergiocollado@github.com; github:sergiocollado
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Taylor Hunt; tigt@github.com; github:tigt
         sodan.labs; sodanlabs@github.com; github:sodanlabs
         Federico Culloca; federicoculloca@github.com; github:federicoculloca

# CSS

**CSS** (Cascading Style Sheets) is a declarative language that controls how webpages look in the
browser. The browser applies CSS style declarations to selected elements to display them properly.
A style declaration contains the properties and their values, which determine how a webpage looks.

CSS is one of the three core Web technologies, along with HTML and JavaScript. CSS usually styles
HTML elements, but can be also used with other markup languages like SVG or XML.

A CSS rule is a set of properties associated with a selector. Here is an example that makes every HTML
paragraph yellow against a black background:

```css
/* The selector "p" indicate that all paragraphs in the document will be affected by that rule */
p {
  /* The "color" property defines the text color, in this case yellow. */
  color: yellow;

  /* The "background-color" property defines the background color, in this case black. */
  background-color: black
}
```

"Cascading" refers to the rules that govern how selectors are prioritized to change a page's
appearance. This is a very important feature, since a complex website can have thousands of CSS rules.

## Learn More

### General Knowledge

- [Learn CSS](https://developer.mozilla.org/en-US/Learn/CSS)
- [CSS](https://en.wikipedia.org/wiki/CSS) on Wikipedia

### Technical Reference

- [The CSS documentation on MDN](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS)
- [The CSS Working Group current work](http://www.w3.org/Style/CSS/current-work)
