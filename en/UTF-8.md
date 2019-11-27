TOPIC: Unicode Transformation Format 8

# UTF-8

**UTF-8** (**Unicode Transformation Format 8**) is the [[World Wide Web]]'s most common character
encoding. Each character is represented by *one to four bytes*. UTF-8 is *backward-compatible* with
[[ASCII]] and can represent any standard [[Unicode]] character.

The first 128 UTF-8 characters precisely match the first 128 [[ASCII]] characters (numbered `0`-`127`),
meaning that existing ASCII text is already valid UTF-8. All other characters use two to four bytes.
Each byte has some bits reserved for encoding purposes. Since non-ASCII characters require more than
one byte for storage, they run the risk of being corrupted if the bytes are separated and not recombined.

## Encoding Rules

UTF-8 uses `1`~`4` bytes to encode each character:

- A [[ASCII]] character only needs `1` byte encoding (Unicode range is from `U+0000` ~ `U+007F`)
- Latin, Greek, Cyrillic, Armenian, Hebrew, Arabic, Syrian and other letters with umlauts require `2`
  byte encoding (Unicode range from `U+0080` ~ `U+07FF`)
- Characters in other languages (including Chinese, Japanese, Korean, Southeast Asian, Middle Eastern,
  etc.) contain most of the commonly used characters, using `3` byte encoding
- Other rarely used language characters use `4` byte encoding

UTF-8 encoding rules: if there is only one byte, the most significant bit is `0`; if it is multi-byte,
the first byte starts from the most significant bit, and the number of consecutive binary bits is 1.
The number of bytes it encodes. The remaining bytes begin with `10`.

## Learn More

### General Knowledge

- [UTF-8 on Wikipedia](https://en.wikipedia.org/wiki/UTF-8)
