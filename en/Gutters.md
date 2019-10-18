TOPIC: Gutters
AUTHORS: Teoli; teoli@mozilla.net; mdn:teoli

# Gutters

**Gutters** or alleys are spacing between content tracks. These can be created in
CSS Grid Layout using the `grid-column-gap`,
`grid-row-gap`, or `grid-gap` properties.

In the example below we have a three-column and two-row track grid, with 20-pixel gaps between column
tracks and `20px`-gaps between row tracks.

```css
.wrapper {
  display: grid;
  grid-template-columns: repeat(3,1.2fr);
  grid-auto-rows: 45%;
  grid-column-gap: 20px;
  grid-row-gap: 20px;
}
```

```html
<div class="wrapper">
   <div>One</div>
   <div>Two</div>
   <div>Three</div>
   <div>Four</div>
   <div>Five</div>
</div>
```

In terms of grid sizing, gaps act as if they were a regular grid track however nothing can be placed
into the gap. The gap acts as if the grid line at that location has gained extra size, so any grid
item placed after that line begins at the end of the gap.

The grid-gap properties are not the only thing that can cause tracks to space out. Margins,
padding or the use of the space distribution properties in Box Alignment can all contribute to
the visible gap – therefore the grid-gap properties should not be seen as equal to “the gutter size”
unless you know that your design has not introduced any additional space with one of these methods.

## Learn More

### Property Reference

- [`grid-column-gap`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/grid-column-gap)
- [`grid-row-gap`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/grid-row-gap)
- [`grid-gap`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/grid-gap)

### Further Reading

- CSS Grid Layout Guide: [Basic concepts of grid layout](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout)
- [Definition of gutters in the CSS Grid Layout specification](https://drafts.csswg.org/css-grid/#gutters)
