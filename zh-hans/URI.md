TOPICS: Uniform Resource Identifier
        Uniform Resource Locator
        Uniform Resource Name

# 统一资源标识符 (Uniform Resource Identifier, URI)

**URI**（统一资源标识符）是一个指向资源的字符串。最通常用在*URL*上来指定Web上资源文件的具体位置。
相比之下，*URN*是在给定的命名空间用名字指向具体的资源，如：书本的*ISBN*。

## 统一资源定位器 (Uniform Resource Locator, URL)

**URL**是*URI*的一个子集。

**统一资源定位器**（*URL*）是指定在[[Internet]]上可以找到资源的位置的文本字符串。

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

**统一资源名称**（*URN*）是统一资源标识（*URI*）的历史名字，它使用`urn:`作为URI scheme。

1997年的[RFC 2141](https://tools.ietf.org/html/rfc2141 "URN Syntax")于中定义了*URN*，
期望为资源提供持久的、位置无关的标识方式，并允许简单地将多个命名空间映射到单个URN命名空间。
这样一个URI的存在并不意味着被标识的资源一定是可用的，但它仍然需要保持全局唯一和持久，即使资源已经不存在了或变得不可用。

自从2005年[RFC 3986](https://tools.ietf.org/html/rfc3986)发布，这一术语的使用已被限制更少的**URI**取代。
这是[W3C](/zh-hans/glossary/World_Wide_Web_Consortium)和
[IETF](/zh-hans/glossary/Internet_Engineering_Task_Force)联合组成的工作组所提议的。
**URN**和**URL**都已经是URI的一种，而且特定情况下URL可能同时拥有名字（URN）和位置（URL）。

在1990年，URN作为一个元数据框架，原本被期望和URL、URC（统一资源特征）一起组成一个第三方互联网信息架构。
然而URC一直停留在理论阶段，随之更晚出现的其他技术（例如资源描述框架）取代了它们。

## 了解更多

- [URI维基百科](https://en.wikipedia.org/wiki/URI)
- [URL维基百科](https://zh.wikipedia.org/wiki/URL)
- [URN维基百科](https://en.wikipedia.org/wiki/URN)
- [RFC 3986 关于URI](https://tools.ietf.org/html/rfc3986 "Uniform Resource Identifier (URI): Generic Syntax")
- [RFC 3305 关于URIs, URLs, URNs](https://tools.ietf.org/html/rfc3305 "URIs, URLs, URNs")
- [RFC 8141 关于URN](https://tools.ietf.org/html/rfc8141 "Uniform Resource Names (URNs)")
- [URL最新标准](https://url.spec.whatwg.org/)
