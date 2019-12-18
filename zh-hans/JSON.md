TOPIC: JavaScript Object Notation

# JavaScript Object Notation (JSON)

**JavaScript Object Notation** (**JSON**) 是一种**数据交换**格式。尽管不是严格意义上的子集，JSON非常接近[[JavaScript]]语法的子集。

JSON可以表示*数字*、*布尔值*、*字符串*、*`null`*、*数组*（值的有序序列），以及*对象*（字符串与值的映射）。JSON并非原生支持更复杂的数据类型（如函数、正则表达式、日期等）。
（日期对象默认会序列化为ISO格式的日期的字符串，因此信息不会完全丢失。）如果你需要使用 JSON 来表示额外的数据类型，请在它们*序列化*时或*反序列化*之前转换值。

与[[XML]]非常相似，JSON能存储传统的CSV格式所不能存储的*层级数据*。
有许多工具能帮助你在这些格式之间转换。

## JSON语法

完整的JSON语法如下：

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

除`JSONNumber`（数字中不得包含空格）或`JSONString`（其中将其解释为字符串中的相应字符，否则会导致错误）之外的任何地方都可以使用无意义的空格。制表符([`U+0009`](http://unicode-table.com/en/0009/))，
回车符([`U+000D`](http://unicode-table.com/en/000D/))，换行符([`U+000A`](http://unicode-table.com/en/000A/))
和空格([`U+0020`](http://unicode-table.com/en/0020/))字符是唯一有效的空白字符。

## JSON 方法

### `JSON.parse()`

将字符串解析为JSON，可以选择转换生成的值及其属性，然后返回该值。 任何违反JSON语法的行为，包括那些与[[JavaScript]]和JSON之间的区别有关的行为，都将引发`SyntaxError`。
`reviver`选项允许解释`replacer`代表其他数据类型的含义。

### `JSON.stringify()`

返回与指定值相对应的JSON字符串，可以选择仅包含某些属性或以用户定义的方式替换属性值。默认情况下，所有`undefined`实例都将替换为`null`，并检查其他不受支持的本机数据类型。`replacer`选项允许指定其他行为。

## JavaScript和JSON的区别

JSON是用于序列化对象，数组，数字，字符串，布尔值和`null`的语法。它基于JavaScript语法，但与JavaScript语法不同：某些JavaScript不是JSON。

**对象和数组**：属性名称必须为**双引号字符串**；禁止尾随逗号。

**数字**：禁止前导零；小数点后必须至少有一位数字。不支持`NaN`和`Infinity`。

**任何JSON文本都是有效的JavaScript表达式** – 但仅在实现了[建议使所有JSON文本均有效ECMA-262的提案](https://github.com/tc39/proposal-json-superset)的JavaScript引擎中。
在尚未实施该建议的引擎中，字符串常量和JSON中的属性键均允许使用`U+2028` (LINE SEPARATOR)和`U+2029` (PARAGRAPH SEPARATOR)；
但是它们在JavaScript字符串文字中的这些功能中的使用是`SyntaxError`。

考虑以下示例，其中`JSON.parse()`将字符串解析为JSON，而`eval()`将字符串执行为JavaScript：

```javascript
var code = '"\u2028\u2029"';
JSON.parse(code); // 在所有JS引擎中按"\u2028\u2029"执行
eval(code); // 在老的JS引擎中会抛出SyntaxError异常
```

其他区别包括只允许使用双引号引起来的字符串，并且不提供`undefined`或注释的规定。对于那些希望使用基于JSON的更人性化的配置格式的人，
Babel编译器使用了[JSON5](https://json5.org/)，更常用的是[YAML](https://en.wikipedia.org/wiki/YAML)。

## 了解更多

- [JSON - 维基百科](https://en.wikipedia.org/wiki/JSON)
