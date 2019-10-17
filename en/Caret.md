TOPIC: Caret
AUTHORS: Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy

# Caret

A **caret** (sometimes called a "text cursor") is an indicator displayed on the screen to indicate
where text input will be inserted. Most user interfaces represent the caret using a thin vertical
line or a character-sized box that flashes, but this can vary. This point in the text is called the
**insertion point**. The word "caret" differentiates the text insertion point from the mouse cursor.

On the web, a caret is used to represent the insertion point in `<input>` and
`<textarea>` elements, as well as any elements whose `contenteditable` attribute is set,
thereby allowing the contents of the element to be edited by the user.

## Learn More

### General Knowledge

- [Caret navigation](https://en.wikipedia.org/wiki/Caret%20navigation) on Wikipedia

### CSS Related To The Caret

You can set the color of the caret for a given element's editable content by setting the element's
CSS [`caret-color`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/caret-color)
property to the appropriate [`<color>`](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/color_value)
value.

### HTML Elements That May Present A Caret

These elements provide text entry fields or boxes and therefore make use of the caret.

- [`<input type="text">`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/input/text)

- [`<input type="password">`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/input/password)

- [`<input type="search">`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/input/search)

- [`<input type="date">`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/input/date),
[`<input type="time">`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/input/time),
[`<input type="datetime">`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/input/datetime),
and [`<input type="datetime-local">`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/input/datetime-local)

- [`<input type="number">`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/input/number),
[`<input type="range">`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/input/range)
[`<input type="email">`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/input/email),
[`<input type="tel">`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/input/%3Cinput_type=_tel_%3E),
and [`<input type="url">`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/input/url)

- [`<textarea>`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea)
  
- Any element with its [`contenteditable`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes#attr-contenteditable)
attribute set
