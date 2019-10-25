TOPIC: Selector (CSS)
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Julie Myers; SnoopyRules@mozilla.net; mdn:SnoopyRules
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Teoli; teoli@mozilla.net; mdn:teoli

# Selector (CSS)

A **CSS selector** is the part of a CSS rule that describes what elements in a document
the rule will match. The matching elements will have the rule's specified style applied to them.

Consider this CSS:

```css
p {
  color: green;
}

div.warning {
  width: 100%;
  border: 2px solid yellow;
  color: white;
  background-color: darkred;
  padding:  0.8em 0.8em 0.6em;
}

#customized {
  font: 16px Lucida Grande, Arial, Helvetica, sans-serif;
}
```

The selectors here are `"p"` (which applies the color green to the text inside any
`<p>` element), `"div.warning"` (which makes any `<div>` element with the
class `"warning`" look like a warning box), and `"#customized"`, which sets the
base font of the element with the ID `"customized"` to 16-pixel tall Lucida Grande or
one of a few fallback fonts.

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

The resulting page content is styled like this:

## Learn More

### General Knowledge

- [Learn More about CSS selectors](https://wiki.developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Selectors)
in our introduction to CSS.
- Basic selectors
    - [Type selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Type_selectors) `elementname`
    - [Class selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Class_selectors) `.classname`
    - [ID selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/ID_selectors) `#idname`
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
    - [Pseudo-classes](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)`:`
    - [Pseudo-elements](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)`::`

## Technical Reference

- [Selectors Level 3](https://drafts.csswg.org/selectors-3/)
