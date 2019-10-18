TOPIC: Parse
AUTHORS: Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Sebastian Zartner; SebastianZ@github.com; github:SebastianZ
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone

# Parse

Parsing means analyzing and converting a program into an internal format that a runtime environment
can actually run, for example the JavaScript engine inside browsers.

The browser parses HTML into a DOM tree. HTML parsing involves tokenization and tree construction.
HTML tokens include start and end TOPIC, as well as attribute names and values. If the document is
well-formed, parsing it is straightforward and faster. The parser parses tokenized input into the
document, building up the document tree.

When the HTML parser finds non-blocking resources, such as an image, the browser will request those
resources and continue parsing. Parsing can continue when a CSS file is encountered, but `<script>`
TOPIC—particularly those without an `async` or `defer` attribute—blocks rendering,
and pauses parsing of HTML.

When the browser encounters CSS styles, it parses the text into the CSS Object Model (or CSSOM),
a data structure it then uses for styling layouts and painting. The browser then creates a render
tree from both these structures to be able to paint the content to the screen.
JavaScript is also downloaded, parsed, and then execute.

JavaScript parsing is done during compile time or whenever the parser is invoked,
such as during a call to a method.

## Learn More

### General Knowledge

- [Parse](https://en.wikipedia.org/wiki/Parsing) on Wikipedia
