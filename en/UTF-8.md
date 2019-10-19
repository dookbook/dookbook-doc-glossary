TOPIC: UTF-8
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy

# UTF-8

UTF-8 (UCS Transformation Format 8) is the World Wide Web's most common character encoding. Each
character is represented by one to four bytes. UTF-8 is backward-compatible with ASCII and can
represent any standard Unicode character.

The first 128 UTF-8 characters precisely match the first 128 ASCII characters (numbered 0-127),
meaning that existing ASCII text is already valid UTF-8. All other characters use two to four bytes.
Each byte has some bits reserved for encoding purposes. Since non-ASCII characters require more than
one byte for storage, they run the risk of being corrupted if the bytes are separated and not recombined.

## Learn More

### General Knowledge

- [UTF-8](https://en.wikipedia.org/wiki/UTF-8) on Wikipedia
- [FAQ about UTF-8 on Unicode website](http://www.unicode.org/faq/utf_bom.html#UTF8)
