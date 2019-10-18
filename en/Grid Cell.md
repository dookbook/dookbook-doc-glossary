TOPIC: Grid Cell
AUTHORS: Teoli; teoli@mozilla.net; mdn:teoli

# Grid Cell

In a CSS Grid Layout, a **grid cell** is the smallest unit you can have on your CSS grid. It
is the space between four intersecting grid lines and conceptually much like a table cell.

![text](https://mdn.mozillademos.org/files/14767/1_Grid_Cell.png)

If you do not place items using one of the grid placement methods, direct children of the grid
container will be placed one into each individual grid cell by the auto-placement algorithm.
Additional row or column tracks will be created to create enough cells to hold all items.

In the example we have created a three column track grid. The five items are placed into grid cells
working along an initial row of three grid cells, then creating a new row for the remaining two.

```css
.wrapper {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  grid-auto-rows: 100px;
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

## Learn More

### Property Reference

- [`grid-template-columns`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/grid-template-columns)
- [`grid-template-rows`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/grid-template-rows)
- [`grid-auto-rows`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/grid-auto-rows)
- [`grid-auto-columns`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/grid-auto-columns)

### Further Reading

- CSS Grid Layout Guide: [Basic concepts of grid layout](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout)
- [Definition of Grid Cells in the CSS Grid Layout specification](https://drafts.csswg.org/css-grid/#grid-track-concept)
