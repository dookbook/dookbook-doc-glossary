TOPIC: Vendor Prefix
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         ExE Boss; ExE-Boss@github.com; github:ExE-Boss
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Darby; darby@mozilla.net; mdn:darby
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Teoli; teoli@mozilla.net; mdn:teoli
         Stephanie Hobson; stephaniehobson@mozilla.net; mdn:stephaniehobson

# Vendor Prefix

Browser vendors sometimes add prefixes to experimental or nonstandard CSS properties and JavaScript
APIs, so developers can experiment with new ideas while—in theory—preventing their experiments
from being relied upon and then breaking web developers' code during the standardization process.
Developers should wait to include the unprefixed property until browser behavior is standardized.

!!! note
    Browser vendors are working to stop using vendor prefixes for experimental features. Web developers
    have been using them on production Web sites, despite their experimental nature. This has made it
    more difficult for browser vendors to ensure compatibility and to work on new features; it's also
    been harmful to smaller browsers who wind up forced to add other browsers' prefixes in order to
    load popular web sites.
    Lately, the trend is to add experimental features behind user-controlled flags or preferences,
    and to create smaller specifications which can reach a stable state much more quickly.

## CSS prefixes

The major browsers use the following prefixes:

- `-webkit-` (Chrome, Safari, newer versions of Opera, almost all iOS browsers (including Firefox
for iOS); basically, any WebKit based browser)
- `-moz-` (Firefox)
- `-o-` (Old, pre-WebKit, versions of Opera)
- `-ms-` (Internet Explorer and Microsoft Edge)

## API prefixes

Historically, vendors have also used prefixes for experimental APIs. If an entire interface is
experimental, then the interface's name is prefixed (but not the properties or methods within).
If an experimental property or method is added to a standardized interface,
then the individual method or property is prefixed.

### Interface prefixes

Prefixes for interface names are upper-cased:

- `WebKit` (Chrome, Safari, newer versions of Opera, almost all iOS browsers
(including Firefox for iOS); basically, any WebKit based browser)
- `Moz` (Firefox)
- `O` (Older, pre-WebKit, versions of Opera)
- `MS` (Internet Explorer and Microsoft Edge)

### Property and method prefixes

The prefixes for properties and methods are lower-case:

- `webkit` (Chrome, Safari, newer versions of Opera, almost all iOS browsers
(including Firefox for iOS); basically, any WebKit based browser)
- `moz` (Firefox)
- `o` (Old, pre-WebKit, versions of Opera)
- `ms` (Internet Explorer and Microsoft Edge)

## Learn More

### General Knowledge

- [Vendor Prefix](https://en.wikipedia.org/wiki/CSS_hack#Browser_prefixes) on Wikipedia
