TOPICS: Character
        Character Set
        Character Encoding

# Character

A character is either a symbol (letters, numbers, punctuation) or non-printing "control" (e.g.,
carriage return or soft hyphen).

## Character Set

A **character** set is an encoding system to let computer know how to recognize Character,
including letters, numbers, punctuation marks, and whitespace.

In earlier times, countries developed their own character sets due to their different languages used,
such as *Kanji JIS* codes (e.g. *Shift-JIS*, *EUC-JP*, etc.) for Japanese, *Big5* for traditional Chinese,
and *KOI8-R* for Russian. However, [[Unicode]] gradually become most acceptable
character set for its universal languages support. [[UTF-8]] is the most common character set and
includes the graphemes of the most popular human languages.

If character set used incorrectly (For example, [[Unicode]] for article encoded in Big5),
you may seen nothing but broken characters, which called [Mojibake](https://en.wikipedia.org/wiki/Mojibake).

## Character Encoding

An **encoding** defines a mapping between **bytes** and **text**. A sequence of bytes allows for
different textual interpretations. By specifying a particular encoding (such as [[UTF-8]]), we
specify how the sequence of bytes is to be interpreted.

For example, in [[HTML]] we normally declare a character encoding of [[UTF-8]], using the following line:

>`<meta charset="utf-8">`
>This ensures that you can use characters from just about any human language in your [[HTML]] document,
and they will display reliably.

## Learn More

- [[ASCII]]
- [[Unicode]]
- [[UTF-8]]

### General Knowledge

- [Character (computing)](https://en.wikipedia.org/wiki/Character%20(computing)) on Wikipedia
- [Character encoding](https://en.wikipedia.org/wiki/Character%20encoding) on Wikipedia
- [ASCII](https://en.wikipedia.org/wiki/ASCII) on Wikipedia
- [UTF-8](https://en.wikipedia.org/wiki/UTF-8) on Wikipedia
- [Unicode](https://en.wikipedia.org/wiki/Unicode) on Wikipedia
