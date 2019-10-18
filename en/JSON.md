TOPIC: JSON
AUTHORS: Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Jongryul Yang; urty5656@gmail.com; github:alattalatta
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Fuqiao Xue; xfq@mozilla.net; mdn:xfq
         April King; april@pokeinthe.io; github:april
         Utkarsh Bhatt; utkarshbhatt12@github.com; github:utkarshbhatt12
         Dekus Lam; DekusDenial@mozilla.net; mdn:DekusDenial
         Rahmat Subekti; bekti@mozilla.net; mdn:bekti
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Janet Swisher; jmswisher@github.com; github:jmswisher
         Keiichi; ethertank@mozilla.net; mdn:ethertank
         紫云飞; ziyunfei@mozilla.net; mdn:ziyunfei
         Rob Wu; rob@robwu.nl; github:Rob--W
         Tom Schuster; evilpie@github.com; github:evilpie
         Trevor Hobson; trevorhobson@github.com; github:trevorhobson
         Amanda Dillon; agdillon@github.com; github:agdillon
         Code PAI; codepai@github.com; github:codepai
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Teoli; teoli@mozilla.net; mdn:teoli
         Timo Tijhof; krinklemail@gmail.com; github:Krinkle
         紫云飞; ziyunfei@mozilla.net; mdn:ziyunfei
         Paul Irish; paul.irish@mozilla.net; mdn:paul.irish
         Eli Grey; Sephr@mozilla.net; mdn:Sephr
         Andreas Wagner; One@mozilla.net; mdn:One
         Wladimir Palant; Wladimir_Palant@mozilla.net; mdn:Wladimir_Palant
         Nickolay Ponomarev; asqueella@gmail.com; github:nickolay

# JSON

JavaScript Object Notation (**JSON**) is a data-interchange format.  Although not a strict subset,
JSON closely resembles a subset of JavaScript syntax. Though many programming languages support JSON,
JSON is especially useful for JavaScript-based apps, including websites and browser extensions.

JSON can represent numbers, booleans, strings, `null`, arrays (ordered sequences of values), and
objects (string-value mappings) made up of these values (or of other arrays and objects).
JSON does not natively represent more complex data types like functions, regular expressions, dates,
and so on.  (Date objects by default serialize to a string containing the date in ISO format, so the
information isn't completely lost.) If you need JSON to represent additional data types, transform
values as they are serialized or before they are deserialized.

Much like XML, JSON has the ability to store hierarchical data unlike the more traditional CSV format.
Many tools provide translation between these formats such as this online [JSON to CSV Converter](https://json-csv.com/)
or this alternative [JSON to CSV Converter](https://jsontoexcel.com/).

The JSON object contains methods for parsing JavaScript Object Notation (JSON) and converting values
to JSON. It can't be called or constructed, and aside from its two method properties, it has no
interesting functionality of its own.

## JavaScript And JSON Differences

JSON is a syntax for serializing objects, arrays, numbers, strings, booleans, and `null`. It is based
upon JavaScript syntax but is distinct from it: some JavaScript is not JSON.

**Objects and Arrays**: Property names must be double-quoted strings; trailing commas are forbidden.

**Numbers**: Leading zeros are prohibited; a decimal point must be followed by at least one digit.
NaN and Infinity are unsupported.

**Any JSON text is a valid JavaScript expression** – but only in JavaScript engines that have
implemented the [proposal to make all JSON text valid ECMA-262](https://github.com/tc39/proposal-json-superset).
In engines that haven't implemented the proposal, U+2028 LINE SEPARATOR and U+2029 PARAGRAPH SEPARATOR
are allowed in string literals and property keys in JSON; but their use in these features in JavaScript
string literals is a `SyntaxError`.

Consider this example where `JSON.parse()` parses the string as JSON and `eval` executes the string
as JavaScript:

```javascript
var code = '"\u2028\u2029"';
JSON.parse(code); // evaluates to "\u2028\u2029" in all engines
eval(code); // throws a SyntaxError in old engines
```

Other differences include allowing only double-quoted strings and having no provisions for `undefined`
or comments. For those who wish to use a more human-friendly configuration format based on JSON,
there is [JSON5](https://json5.org/), used by the Babel compiler, and the more commonly used [YAML](https://en.wikipedia.org/wiki/YAML).

## Full JSON Syntax

The full JSON syntax is as follows:

```javascript
JSON = null
    or true or false
    or JSONNumber
    or JSONString
    or JSONObject
    or JSONArray

JSONNumber = - PositiveNumber
          or PositiveNumber
PositiveNumber = DecimalNumber
              or DecimalNumber . Digits
              or DecimalNumber . Digits ExponentPart
              or DecimalNumber ExponentPart
DecimalNumber = 0
             or OneToNine Digits
ExponentPart = e Exponent
            or E Exponent
Exponent = Digits
        or + Digits
        or - Digits
Digits = Digit
      or Digits Digit
Digit = 0 through 9
OneToNine = 1 through 9

JSONString = ""
          or " StringCharacters "
StringCharacters = StringCharacter
                or StringCharacters StringCharacter
StringCharacter = any character
                  except " or \ or U+0000 through U+001F
               or EscapeSequence
EscapeSequence = \" or \/ or \\ or \b or \f or \n or \r or \t
              or \u HexDigit HexDigit HexDigit HexDigit
HexDigit = 0 through 9
        or A through F
        or a through f

JSONObject = { }
          or { Members }
Members = JSONString : JSON
       or Members , JSONString : JSON

JSONArray = [ ]
         or [ ArrayElements ]
ArrayElements = JSON
             or ArrayElements , JSON
```

Insignificant whitespace may be present anywhere except within a JSONNumber
(numbers must contain no whitespace) or JSONString (where it is interpreted as the corresponding
character in the string, or would cause an error). The tab character ([U+0009](http://unicode-table.com/en/0009/)),
carriage return ([U+000D](http://unicode-table.com/en/000D/)), line feed
([U+000A](http://unicode-table.com/en/000A/)), and space ([U+0020](http://unicode-table.com/en/0020/))
characters are the only valid whitespace characters.

## Methods

`JSON.parse()`

Parse a string as JSON, optionally transform the produced value and its properties, and return the
value. Any violations of the JSON syntax, including those pertaining to the differences between
JavaScript and JSON, cause a `SyntaxError` to be thrown. The `reviver` option allows for interpreting
what the `replacer` has used to stand in for other datatypes.

`JSON.stringify()`

Return a JSON string corresponding to the specified value, optionally including only certain
properties or replacing property values in a user-defined manner. By default, all instances of
`undefined` is replaced with `null`, and other unsupported native data types are censored. The `replacer`
option allows for specifying other behavior.

## See Also

## Tools

- [JSON Diff](http://jsoncompare.org/) checker.
- [JSON Beautifier/editor](http://jsonbeautifier.org/).
- [JSON Parser](http://jsonparser.org/)
- [JSON Validator](https://tools.learningcontainer.com/json-validator/).

## Learn More

### General Knowledge

- [JSON](https://en.wikipedia.org/wiki/JSON) on Wikipedia
