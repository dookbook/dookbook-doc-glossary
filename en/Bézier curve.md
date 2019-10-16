TOPIC: Bézier curve
AUTHORS: Dustin Younse; milsyobtaf@github.com; github:milsyobtaf

# Bézier curve

A **Bézier** curve (pronounced bezje) is a mathematically described curve used in computer graphics
and animation. In vector images, they are used to model smooth curves that can be scaled indefinitely.

The curve is defined by a set of control points with a minimum of two. Web related graphics and
animations use Cubic Béziers, which are curves with four control points P0, P1, P2, and P3.

To draw the curve, two imaginary lines are drawn, one from P0 to P1 and the other from P1 to P2.
The end points of the lines are then steadily moved to the next point. A third imaginary line is
drawn with its starting point moving steadily on the first helper line and the end point on the
second helper line. On this imaginary line a point is drawn from its starting point moving steadily
to its end point. The curve this point describes is the Bézier curve. Hereʼs an animated
illustration demonstrating the creation of the curve:

![A9zier_3_big](https://upload.wikimedia.org/wikipedia/commons/d/db/B%C3%A9zier_3_big.gif)

## Learn more

### Genreal knowledge

- [Bézier curve on Wikipedia](https://en.wikipedia.org/wiki/B%C3%A9zier_curve)

### Learn about it

- [Cubic Bézier timing functions in CSS](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/timing-function#The_cubic-bezier()_class_of_timing_functions)
- [`keySplines`](https://wiki.developer.mozilla.org/en-US/docs/Web/SVG/Attribute/keySplines) SVG attribute
- [Cubic Bézier Generator](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Tools/Cubic_Bezier_Generator)
