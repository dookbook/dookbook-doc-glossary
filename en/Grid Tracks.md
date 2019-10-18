TOPIC: Grid Tracks
AUTHORS: Teoli; teoli@mozilla.net; mdn:teoli

# Grid Tracks

A **grid track** is the space between two grid lines. They are defined in the explicit grid by using
the `grid-template-columns` and grid-template-rows properties or the shorthand
`grid` or grid-template properties. Tracks are also created in the implicit grid by
positioning a grid Item outside of the tracks created in the explicit grid.

The image below shows the first row track on a grid.

![text](https://mdn.mozillademos.org/files/14769/1_Grid_Track.png)

## Track Sizing In The Explicit Grid

When defining grid tracks using `grid-template-columns` and `grid-template-rows` you may
use any length unit, and also the flex unit, `fr` which indicates a portion of the available space
in the grid container. The example below demonstrates a grid with three column tracks, one of 200 pixels,
the second of 1fr, the third of 3fr. Once the 200 pixels has been subtracted from the space available
in the grid container, the remaining space is divided by 4.
One part is given to column 2, 3 parts to column 3.

```css
.wrapper {
  display: grid;
  grid-template-columns: 200px 1fr 3fr;
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

## Track Sizing In The Implicit Grid

Tracks created in the implicit grid are auto-sized by default, however you can define a size for these
tracks using the `grid-auto-rows` and `grid-auto-columns` properties.

## Learn More

### Property Reference

- [`grid-template-columns`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/grid-template-columns)
- [`grid-template-rows`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/grid-template-rows)
- [`grid-auto-rows`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/grid-auto-rows)
- [`grid-auto-columns`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/grid-auto-columns)

### Further Reading

- CSS Grid Layout Guide: [Basic concepts of grid layout](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout)
- [Definition of Grid Tracks in the CSS Grid Layout specification](https://drafts.csswg.org/css-grid/#grid-track-concept)
