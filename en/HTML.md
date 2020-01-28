TOPICS: HyperText Markup Language

# HyperText Markup Language (HTML)

**HTML** (*HyperText Markup Language*) is a *descriptive*, *[markup]* language that specifies
webpage **structure**.

An HTML file is normally saved with an **`.htm`** or **`.html`** extension, served by a web server,
and can be rendered by any *[[Web browser]]*.

## Brief History

In 1990, as part of his vision of the [Web](/en/glossary/World_Wide_Web), *Tim Berners-Lee* defined
the concept of **[[hypertext]]**,
which *Berners-Lee* formalized the following year through a markup mainly based on **[[SGML]]**.
The **[[IETF]]** began formally specifying HTML in 1993, and after several drafts released version 2.0
in 1995. In 1994 *Berners-Lee* founded the **[[W3C]]** to develop the Web. In 1996, the W3C took
over the HTML work and published the *HTML 3.2 recommendation* a year later. *HTML 4.0* was released
in 1999 and became an [[ISO]] standard in 2000.

At that time, the W3C nearly abandoned HTML in favor of *[[XHTML]]*, prompting the founding of an
independent group called **[[WHATWG]]** in 2004. Thanks to WHATWG, work on *HTML5* continued: the
two organizations released the first draft in 2008 and the final standard in 2014.

## Doctype

The **doctype** is the required "**`<!DOCTYPE html>`**" preamble found at the top of all documents.
Its sole purpose is to prevent a browser from switching into so-called "*quirks mode*" when
rendering a document; that is, the "`<!DOCTYPE html>`" doctype ensures that the browser makes a
best-effort attempt at following the relevant specifications, rather than using a different rendering
mode that is incompatible with some specifications.

## Element

An HTML document is a *plaintext* document structured with **elements**.

![Anatomy of an HTML element](/media/glossary__anatomy-of-an-html-element.png)

**Elements** are surrounded by matching opening and closing **tag**. *Elements* and *tags* are not the
same things. Tags begin or end an element in source code, whereas elements are part of the **[[DOM]]**,
the document model for displaying the page in the [browser](/en/glossary/Web_browser).

A typical element includes an **opening tag** with some **attributes**, **enclosed text content**, and
**a closing tag**.

### Empty Elements (Void Elements)

There are a few **empty elements** (**void elements**) that cannot enclose any text, for instance `<img>`.

### Block and Inline Elements

There are two important categories of elements in HTML which you should know about.
They are **block-level elements** and **inline elements**.

- **Block-level elements** form a visible block on a page — they will appear on a new line from
  whatever content went before it, and any content that goes after it will also appear on a new line.
  Block-level elements tend to be structural elements on the page that represent, for example,
  paragraphs (`<p>`), lists (`<ul>`, `<ol>`), navigation menus (`<nav>`), footers (`<footer>`),
  and so on. A block-level element wouldn't be nested inside an inline element, but it might be
  nested inside another block-level element.
- **Inline elements** are those that are contained within block-level elements and surround only
  small parts of the document’s content, not entire paragraphs and groupings of content. An inline
  element will not cause a new line to appear in the document; they would normally appear inside a
  paragraph of text, for example an `<a>` element (hyperlink) or emphasis elements such as
  `<em>` or `<strong>`.

## Tag

In HTML a **tag** is used for creating an *element*.  The *name* of an HTML element is the name
used in **angle brackets** such as `<p>` for paragraph.  Note that the end tag's name is preceded by
a **slash character**, "`</p>`", and that in *empty elements* the end tag is neither required nor allowed.
If *attributes* are not mentioned, default values are used in each case.

!!! warn "Note"
    Tags in HTML are **case-insensitive**, i.e. they can be written in uppercase or lowercase.
    For example, a `<title>` tag could be written as `<title>`, `<TITLE>`, `<Title>`, `<TiTlE>`, etc.,
    and it will work fine. Best practice, however, is **to write all tags in lowercase** for consistency,
    readability, and other reasons.

Each **tag** begins and ends with **angle brackets** (**`<>`**).

## Attribute

You can extend HTML tag with **attributes**, which provide additional information affecting how the
[browser](/en/glossary/Web_browser) interprets the element, such as changing its behavior or
providing metadata.

An attribute always has
the form **`name="value"`** (the attribute's identifier followed by its associated value).

### Multiple Attributes

A **space** between it and the element name (or the previous attribute, if the element already has one
or more attributes).

### Boolean Attributes

You'll sometimes see attributes written *without values* — this is perfectly allowed.
These are called **Boolean attributes**, and they can only have one value, which is generally the
same as the attribute name. As an example, take the `disabled` attribute, which you can assign to
form input elements, if you want them to be disabled (greyed out) so the user can't enter any
data in them.

```html
<!-- using the disabled attribute prevents the end user from entering text into the input box -->
<input type="text" disabled>

<!-- The user can enter text into the follow input, as it doesn't contain the disabled attribute -->
<input type="text">  
```

## Hyperlink

**Hyperlinks** connect webpages or data items to one another. In HTML, [`<a>`](/en/webfrontend/<a>)
elements define hyperlinks from a spot on a webpage (like a text string or image) to another spot on
some other webpage (or even on the same page).

## Hypertext

**[[Hypertext]]** is text that contains links to other texts, as opposed to a single linear flow
like in a novel.

The term was coined by *Ted Nelson* around 1965.

## HTML5

**HTML5** is the *latest* evolution of the standard that defines *HTML*.
The term represents two different concepts.
It is a new version of the language HTML, with new elements, attributes, and behaviors,
and a larger set of technologies that allows the building of more diverse and powerful Web sites and
applications. This set is sometimes called *HTML5 & friends* and often shortened to just *HTML5*.

HTML5 technologies classifies into several groups based on their function:

- **[[Semantics]]**: allowing you to describe more precisely what your content is.
    - new outlining and sectioning elements: [`<section>`](/en/webfrontend/<section>),
    [`<article>`](/en/webfrontend/<article>), [`<nav>`](/en/webfrontend/<nav>), [`<header>`](/en/webfrontend/<header>),
    [`<footer>`](/en/webfrontend/<header>) and [`<aside>`](/en/webfrontend/<aside>).
    - new multimedia content: [`<video>`](/en/webfrontend/<video>),
    [`<audio>`](/en/webfrontend/<audio>) elements
    - forms improvements: forms constraint validation API, several new attributes, new values
    for the [`<input>`](/en/webfrontend/<input>) attribute type and the new
    [`<output>`](/en/webfrontend/<output>) element
    - new semantic elements: [`<mark>`](/en/webfrontend/<mark>), [`<figure>`](/en/webfrontend/<figure>),
    [`<figcaption>`](/en/webfrontend/<figcaption>), [`<data>`](/en/webfrontend/<data>), [`<time>`](/en/webfrontend/<time>),
    [`<output>`](/en/webfrontend/<output>), [`<progress>`](/en/webfrontend/<progress>),
    or [`<meter>`](/en/webfrontend/<meter>) and [`<main>`](/en/webfrontend/<main>), etc.
    - improvement in *[`<iframe>`](/en/webfrontend/<iframe>)*: Using the `sandbox` and `srcdoc`
    attributes, authors can now be precise about the level of security and the wished rendering of an
    [`<iframe>`](/en/webfrontend/<iframe>) element
    - **MathML**: Allows directly embedding mathematical formulas.
- **Connectivity**: allowing you to communicate with the server in new and innovative ways.
    - **[[WebSocket]]**
    - **Server-Sent Event** (**SSE**): Allows a server to push events to a client, rather than the classical
    paradigm where the server could send data only in response to a client's request.
    - **WebRTC**: This technology, where *RTC* stands for *Real-Time Communication*, allows connecting
    to other people and controlling videoconferencing directly in the browser, without the need for
    a plugin or an external application.
- **Offline and Storage**: allowing webpages to store data on the client-side locally and operate
  offline more efficiently.
    - **Application Cache**
    - **Online and Offline Events**: let applications and extensions detect whether or not there's
    an active Internet connection, as well as to detect when the connection goes up and down.
    - **Client-Side Session** and **Persistent Storage** (aka **DOM Storage**):
    allow Web applications to
    store structured data on the client side.
    - **IndexedDB**: IndexedDB is a Web standard for the storage of significant amounts of structured
    data in the browser and for high performance searches on this data using indexes.
    - **File API**: makes it possible for Web applications to access local files selected by the
    user. This includes support for selecting multiple files using the `<input>` of `type=file` HTML
    element's new `multiple` attribute. There also is `FileReader`.
- **Multimedia**: making video and audio first-class citizens in the Open Web.
    - **[`<audio>`](/en/webfrontend/<audio>)** and **[`<video>`](/en/webfrontend/<video>)** elements
    - **WebRTC**
    - **Camera API**
    - **[`<track>`](/en/webfrontend/<track>)** and **WebVTT**
- **2D/3D graphics and effects**: Allows a much more diverse range of presentation options.
    - **[`<canvas>`](/en/webfrontend/<canvas>)** element
    - **Text API** for *[`<canvas>`](/en/webfrontend/<canvas>)* elements
    - **WebGL**: WebGL brings 3D graphics to the Web by introducing an API that closely conforms to
    **OpenGL ES 2.0** that can be used in HTML5 *[`<canvas>`](/en/webfrontend/<canvas>)* elements.
    - **[[SVG]]**: An [[XML]]-based format of vectorial images that can directly be embedded in the HTML.
- **Performance and integration**: providing greater speed optimization and better usage of computer
  hardware.
    - **Web Workers**: Allows delegation of [[JavaScript]] evaluation to background threads, allowing
    these activities to prevent slowing down interactive events.
    - **`XMLHttpRequest`** level 2: Allows fetching *asynchronously* some parts of the page, allowing
    it to display dynamic content, varying according to the time and user actions.
    This is the technology behind **[[Ajax]]**.
    - **JIT**-compiling [[JavaScript]] engine
    - **History API**: Allows the manipulation of the browser history. This is especially useful for
    pages loading interactively new information.
    - **`contentEditable` Attribute**: HTML5 has standardized the contentEditable attribute.
    Transform your website to a wiki!
    - **Drag and Drop API**: Allows support for dragging and dropping items
    within and between Web sites. This also provides a simpler API for use by extensions and applications.
    - **Focus Management**: The new HTML5 `activeElement` and `hasFocus` attributes are supported.
    - **Web-based Protocol Handlers**: You can now register Web applications as protocol handlers
    using the `navigator.registerProtocolHandler()` method.
    - **requestAnimationFrame**: Allows control of animations rendering to obtain optimal performance.
    - **Fullscreen API**: Controls the usage of the whole screen for a Web page or application,
    without the browser UI displayed.
    - **Pointer Lock API**: Allows locking the pointer to the content, so games and similar
    applications don't lose focus when the pointer reaches the window limit.
- **Device access**: allowing for the usage of various input and output devices.
    - **Camera API**
    - **Touch Events**
    - **Geolocation**
    - **Detecting Device Orientation**: Get the information when the device on which the browser runs
    changes orientation. This can be used as an input device (e.g., to make games that react to the
    position of the device) or to adapt the layout of a page to the orientation of the screen
    (portrait or landscape).
    - **Pointer Lock API**: Allows locking the pointer to the content, so games and similar
    applications don't lose focus when the pointer reaches the window limit.

## DHTML

**DHTML** (*Dynamic HTML*) refers to the code behind interactive webpages that need no plugins like
*Flash* or *Java*. DHTML aggregates the combined functionality of HTML, [[CSS]], the [[DOM]], and [[JavaScript]].

## HTML Comment `<!-- -->`

**`<!-- -->`** is a comment tag, which is used to insert comments in the source code. Comments do not
appear in the browser.

You can use comments to explain your code, which will help you edit the code at a later time. This
is especially useful when you write a lot of code.

It is also a good practice to use comment tags to hide scripts that are not supported by the browser
(so that the scripts are not displayed as plain text).

Comment tag*** do not support any standard attributes **. The release tag** does not support any
event attributes **.

**Examples**
HTML :

```HTML
<!-This is a comment. Comments are not displayed in the browser. ->

<p> This is a normal paragraph. </ p>
```

## Learn More

- [HTML on Wikipedia](https://en.wikipedia.org/wiki/HTML)
- [HTML Element on Wikipedia](https://en.wikipedia.org/wiki/HTML%20element)
- [Hyperlink on Wikipedia](https://en.wikipedia.org/wiki/Hyperlink)
- [Hypertext on Wikipedia](https://en.wikipedia.org/wiki/Hypertext)
- [DHTML on Wikipedia](https://en.wikipedia.org/wiki/Dynamic%20HTML)
- [HTML Living Standard / Specification - WHATWG](https://html.spec.whatwg.org/) (Recommended)
- [The HTML 5 Specification - W3C](http://www.w3.org/TR/html5/)
- [W3C HTML Validator](http://validator.w3.org/ "W3C HTML Validator")
- [The `Element` Interface](https://developer.mozilla.org/en-US/docs/Web/API/Element)
- [Web Components/Custom Elements](https://developer.mozilla.org/en-US/docs/Web/Web_Components/Custom_Elements)
