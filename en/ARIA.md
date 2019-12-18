TOPIC: Accessible Rich Internet Applications

# Accessible Rich Internet Applications (ARIA)

**ARIA** (**Accessible Rich Internet Applications**) is a *[[W3C]] specification* for adding
semantics and other metadata to HTML to cater to users of assistive technology.

For example, you could add the attribute `role="alert"` to a `<p>` tag to notify a
sight-challenged user that the information is important and time-sensitive
(which you might otherwise convey through text color).

Accessible Rich Internet Applications (ARIA) is a set of attributes that define ways to make web
content and web applications (especially those developed with [[JavaScript]]) more accessible to
*people with disabilities*.

It supplements HTML so that interactions and widgets commonly used in applications can be passed to
assistive technologies when there is not otherwise a mechanism. For example,
ARIA enables accessible navigation landmarks in HTML4, JavaScript widgets,
form hints and error messages, live content updates, and more.

!!! warn "Note"
    Many of these widgets were later incorporated into HTML5, and
    **developers should prefer using the correct semantic HTML element over using ARIA**,
    if such an element exists. For instance, native elements have built-in keyboard accessibility,
    roles and states. However, if you choose to use ARIA, you are responsible for
    mimicking (the equivalent) browser behaviour in script.

Here's the markup for a progress bar widget:

```html
<div id="percent-loaded" role="progressbar" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100">
```

This progress bar is built using a `<div>`, which has no meaning. Unfortunately, there isn't a more
semantic tag available to developers in HTML 4, so we need to include ARIA roles and properties.
These are specified by adding attributes to the element. In this example, the `role="progressbar"`
attribute informs the browser that this element is actually a JavaScript-powered progress bar widget.
The `aria-valuemin` and `aria-valuemax` attributes specify the minimum and maximum values for the progress
bar, and the `aria-valuenow` describes the current state of it and therefore must be
kept updated with JavaScript like this:

```javascript
// Create a function that can be called at any time to update
// the value of the progress bar.
function updateProgress(percentComplete) {
  progressBar.setAttribute("aria-valuenow", percentComplete);
}
```

!!! info "Note"
    In HTML5, all ARIA attributes validate. The new landmark elements
    (`<main>`, `<header>`, `<nav>` etc) have built-in ARIA roles, so there is no need to duplicate them.
