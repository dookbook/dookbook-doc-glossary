TOPIC: Fallback Alignment
AUTHORS: Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills

# Fallback Alignment

In CSS Box Alignment, a fallback alignment is specified in order to deal with cases where the
requested alignment cannot be fullfilled. For example, if you specify `justify-content: space-between`
there must be more than one alignment subject. If there is not, the fallback alignment is used.
This is specified per alignment method, as detailed below.

First baseline
:   `start`

Last baseline
:   `safe end`

Baseline
:   `start`

Space-between
:   `flex-start` (start)

Space-around
:   `center`

Space-evenly
:   `center`

Stretch
:   `flex-start` (start)

## Learn More

- [CSS Box Alignment](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Alignment)
