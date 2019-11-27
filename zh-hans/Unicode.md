TOPIC: Unicode

# Unicode

**Unicode**是标准的 **[[字符集]]**，它对世界上不同的语言，书写系统和符号中的字符进行编号和定义。通过为每个字符分配一个数字，
程序员可以创建[字符编码](/zh-hans/glossary/Character_encoding)，以使计算机可以在同一文件或程序中存储，处理和传输语言的任意组合。

在使用Unicode之前，在同一数据中混合语言既困难又容易出错。例如，一个字符集将存储日语字符，另一字符集将存储阿拉伯字母。如果没有清楚地标记数据的哪些部分位于哪个字符集中，
则其他程序和计算机将错误地显示文本，或在处理过程中损坏文本。如果您曾经见过用诸如“Ã”，“££”之类的乱七八糟的字符代替大括号（`“”`）的字符的文本，
那么您就已经看到了称为*乱码*。

网络上最常见的Unicode字符编码是 **[[UTF-8]]**。 还存在其他编码，例如UTF-16或过时的UCS-2，但*推荐使用UTF-8*。

## 更多

- [Unicode标准: 技术性介绍](http://www.unicode.org/standard/principles.html)
- [Unicode - 维基百科](https://en.wikipedia.org/wiki/Unicode)
