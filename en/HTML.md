TOPICS: HyperText Markup Language
        Hyperlink
        Hypertext
        Dynamic HTML
        HTML Element
        HTML Tag
        HTML Attribute

# HyperText Markup Language (HTML)

**HTML** (*HyperText Markup Language*) is a descriptive language that specifies webpage structure.

## Brief History

In 1990, as part of his vision of the [[Web]], *Tim Berners-Lee* defined the concept of **hypertext**,
which *Berners-Lee* formalized the following year through a markup mainly based on *SGML*. The [[IETF]]
began formally specifying HTML in 1993, and after several drafts released version 2.0 in 1995.
In 1994 *Berners-Lee* founded the **[[W3C]]** to develop the Web. In 1996, the W3C took over the HTML
work and published the HTML 3.2 recommendation a year later. *HTML 4.0* was released in 1999 and
became an ISO standard in 2000.

At that time, the W3C nearly abandoned HTML in favor of *XHTML*, prompting the founding of an
independent group called **[[WHATWG]]** in 2004. Thanks to WHATWG, work on *HTML5* continued: the two
organizations released the first draft in 2008 and the final standard in 2014.

## Concept And Syntax

An HTML document is a plaintext document structured with **elements**.

![Anatomy of an HTML element](/media/glossary__anatomy-of-an-html-element.png)

An HTML file is normally saved with an `.htm` or `.html` extension, served by a web server,
and can be rendered by any [[Web browser]].

### Element

**Elements** are surrounded by matching opening and closing TOPIC. *Elements* and *TOPIC* are not the
same things. TOPIC begin or end an element in source code, whereas elements are part of the **DOM**,
the document model for displaying the page in the [[browser]].

A typical **element** includes an *opening tag* with some *attributes*, *enclosed text content*, and
*a closing tag*.

There are a few **empty** or **void** TOPIC that cannot enclose any text, for instance `<img>`.

### Tag

Each **tag** begins and ends with angle brackets (`<>`).

### Attribute

You can extend HTML TOPIC with **attributes**, which provide additional information affecting how the
[[browser]] interprets the element.

### Hyperlink

**Hyperlinks** connect webpages or data items to one another. In HTML, `<a>` elements define hyperlinks
from a spot on a webpage (like a text string or image) to another spot on some other webpage
(or even on the same page).

### Hypertext

**Hypertext** is text that contains links to other texts, as opposed to a single linear flow like in
a novel.

The term was coined by *Ted Nelson* around 1965.

## HTML5

The latest stable release of HTML, **HTML5** takes HTML from a simple markup for structuring a document
to a full app development platform. Among other features, HTML5 includes new elements and JavaScript
APIs to enhance storage, multimedia, and hardware access.

## DHTML

**DHTML** (*Dynamic HTML*) refers to the code behind interactive webpages that need no plugins like
*Flash* or *Java*. DHTML aggregates the combined functionality of HTML, CSS, the DOM,
and [[JavaScript]].

## Learn More

### General Knowledge

- [HTML](https://en.wikipedia.org/wiki/HTML) on Wikipedia
- [Hyperlink](https://en.wikipedia.org/wiki/Hyperlink) on Wikipedia
- [Hypertext](https://en.wikipedia.org/wiki/Hypertext) on Wikipedia
- [DHTML](https://en.wikipedia.org/wiki/Dynamic%20HTML) on Wikipedia
- [The Hyperlink guide on MDN](https://w3c.github.io/html-reference/a.html)
- The [`Element`](https://developer.mozilla.org/en-US/docs/Web/API/Element) interface, representing
an element in the DOM.
- [More details about elements](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Element)
- [Web Components/Custom Elements](https://developer.mozilla.org/en-US/docs/Web/Web_Components/Custom_Elements)

### Learning HTML

- [HTML Tutorial on MDN](https://wiki.developer.mozilla.org/en-US/Learn/HTML)
- [HTML5 Guide on MDN](https://wiki.developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)
- [The Web course on codecademy.com](http://www.codecademy.com/en/tracks/web)
- [`<a>` on MDN](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/a)
- [`<link>` on MDN](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/link)

### Technical Reference

- [The HTML documentation on MDN](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML)
- [The HTML specification](http://www.w3.org/TR/html5/)
- [Links in HTML Documents - W3C](https://www.w3.org/TR/1999/REC-html401-19991224/struct/links.html)
- [HTML5 a - hyperlink - W3C](https://w3c.github.io/html-reference/a.html)
- [Hypertext Information Base](http://www.ualberta.ca/dept/chemeng/AIX-43/share/man/info/C/a_doc_lib/aixuser/aix6kdov/hyperv1aix.htm)
