TOPICS: Uniform Resource Identifier
        Uniform Resource Locator
        Uniform Resource Name

# 统一资源标识符 (Uniform Resource Identifier, URI)

**URI**（统一资源标识符）是一个指向资源的字符串。最通常用在*URL*上来指定Web上资源文件的具体位置。
相比之下，*URN*是在给定的命名空间用名字指向具体的资源，如：书本的*ISBN*。

## 统一资源定位器 (Uniform Resource Locator, URL)

**统一资源定位器**（*URL*）是指定在[[Internet]]上可以找到资源的位置的文本字符串。它是*URI*的一个**子集**。

在[[HTTP]]的上下文中，**URL**被叫做”*网络地址*“或“*链接*”。你的[Web浏览器](/zh-hans/glossary/Web_browser)在其地址栏显示URL，
例如 `https://dookbook.info`。

URL也可用于文件传输（**FTP**），电子邮件（**SMTP**）和其他应用。

### 格式

URL的一般格式为(带方括号[]的为可选项)：

```http
protocol://hostname[:port]/path/[;parameters][?query]#fragment
```

URL的格式由三部分组成：

①第一部分是协议(或称为服务方式)。

②第二部分是存有该资源的主机IP地址(有时也包括端口号)。

③第三部分是主机资源的具体地址，如目录和文件名等。

第一部分和第二部分用`://`符号隔开，

第二部分和第三部分用`/`符号隔开。

第一部分和第二部分是不可缺少的，第三部分有时可以省略。

## Uniform Resource Name (URN)

**统一资源名称**（*URN*）是标准格式的*URI*，指的是未指定资源位置或资源是否存在的URI。此示例来自[RFC 3986](https://www.ietf.org/rfc/rfc3986.txt)：

`urn:oasis:names:specification:docbook:dtd:xml:4.1.2`

## 了解更多

- [URI - 维基百科](https://en.wikipedia.org/wiki/URI)
- [URL - 维基百科](https://zh.wikipedia.org/wiki/URL)
- [URN - 维基百科](https://en.wikipedia.org/wiki/URN)
- [RFC 3986 - URI](https://tools.ietf.org/html/rfc3986 "Uniform Resource Identifier (URI): Generic Syntax")
- [RFC 3305 - URIs, URLs, URNs](https://tools.ietf.org/html/rfc3305 "URIs, URLs, URNs")
- [RFC 8141 - URN](https://tools.ietf.org/html/rfc8141 "Uniform Resource Names (URNs)")
- [URL最新标准](https://url.spec.whatwg.org/)
