TOPICS: 统一资源标识符
        Uniform Resource Identifier
        统一资源定位器
        Uniform Resource Locator

# 统一资源标识符 (Uniform Resource Identifier, URI)

**URI**（统一资源标识符）是一个指向资源的字符串。最通常用在*URL*上来指定Web上资源文件的具体位置。
相比之下，*URN*是在给定的命名空间用名字指向具体的资源，如：书本的*ISBN*。

## 统一资源定位器 (Uniform Resource Locator, URL)

**URL**是*URI*的一个子集。

**统一资源定位器**（*URL*）是指定在[[Internet]]上可以找到资源的位置的文本字符串。

在[[HTTP]]的上下文中，**URL**被叫做”*网络地址*“或“*链接*”。你的[[Web浏览器]]在其地址栏显示URL，
例如 `https://developer.mozilla.org`。

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

## 了解更多

- [URI维基百科](https://en.wikipedia.org/wiki/URI)
- [RFC 3986 on URI](http://tools.ietf.org/html/rfc3986)
- [URL维基百科](https://zh.wikipedia.org/wiki/URL)
- [URL最新标准](https://url.spec.whatwg.org/)
