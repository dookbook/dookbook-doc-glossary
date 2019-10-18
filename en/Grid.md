TOPIC: Grid
AUTHORS: Евгений; boxa6@github.com; github:boxa6
         Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         angelo rogerio rubin; angelorubin@mozilla.net; mdn:angelorubin
         Teoli; teoli@mozilla.net; mdn:teoli

# Grid

A CSS grid is defined using the `grid` value of the `display` property; you can define columns and
rows on your grid using the [`grid-template-rows`](url) and [grid-template-columns](url) properties.

The grid that you define using these properties is described as the explicit grid.

If you place content outside of this explicit grid, or if you are relying on auto-placement and the
grid algorithm needs to create additional row or column tracks to hold [grid items](url), then extra
tracks will be created in the implicit grid. The implicit grid is the grid created automatically due
to content being added outside of the tracks defined.

In the example below I have created an explicit grid of three columns and two rows. The third row on
the grid is an implicit grid row track, formed due to their being more than the six items which fill
the explicit tracks.

```css
.wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 100px 100px;
}
```

```html
<div class="wrapper">
   <div>One</div>
   <div>Two</div>
   <div>Three</div>
   <div>Four</div>
   <div>Five</div>
   <div>Six</div>
   <div>Seven</div>
   <div>Eight</div>
</div>
```

## Learn More

### Property Reference

- [`grid-template-columns`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/grid-template-columns)
- [`grid-template-rows`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/grid-template-rows)
- [`grid`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/grid)
- [`grid-template`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/grid-template)

### Further Reading

- CSS Grid Layout Guide: [Basic concepts of grid layout](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout)
