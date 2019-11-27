TOPICS: HyperText Transfer Protocol

# 超文本传输协议 (HTTP)

**超文本传输协议**（**HTTP**）是用来在[Web](/zh-hans/glossary/World_Wide_Web)上传输超媒体文档的基础协议，
最典型的是在[浏览器](/zh-hans/glossary/Web_browser)和服务器之间传递以至于上网人员可以浏览他们。
目前HTTP最新版本是*HTTP/2*。

作为[[URI]]的一部分，`“http://”`被称为*模式* (*schema*)，通常位于地址的开头，例如“[https://dookbook.info](https://dookbook.info/)”，
就是指[浏览器](/zh-hans/glossary/Web_browser)利用*HTTP协议*请求文档。`https`在这个例子中指的是HTTP协议的*安全版本*，被称为*SSL*，或者*TLS*。

HTTP是**基于文本** (所有的通信都是以纯文本的形式进行) 以及**无状态的** (当前通信不会发现以前的通信状态)。
这个特点对在[Web](/zh-hans/glossary/World_Wide_Web)上访问网页的人是很理想的。但是，HTTP也可以用作*REST* Web服务的基础或*[[AJAX]]*请求，以使其更具动态性。

HTTP使用的默认端口为`80` (HTTPS默认使用`443`)。

## HTTPS

**HTTPS**（全称：*Hyper Text Transfer Protocol over SecureSocket Layer*），是HTTP协议的*加密*版本，通常使用**SSL**或**TLS**加密客户端和服务器之间的所有通信。
这个安全连接允许客户端安全地与服务器交换敏感数据，例如银行业务活动或在线购物。

## HTTP/2

**HTTP/2**是HTTP网络协议的主要版本。它的主要目标是通过**启用请求/响应多路复用**来*减少延迟*，通过**有效压缩HTTP头部字段**来*最小化协议大小*，
并增加对**请求的优先级**的支持和**服务器推送 (Server Push)**。

HTTP/2不会以任何方式修改HTTP的应用程序语义。在*HTTP 1.1*中找到的所有核心概念，例如HTTP方法，状态码，[[URI]]和HTTP头部字段，都保留在原位。
取而代之的是，HTTP/2修改了数据在客户端和服务器之间的格式化（*framed*）和*传输*方式，这两者通过在新的二进制帧层控制整个过程以及隐藏其复杂性。
因此，所有现有的应用程序都可以不经修改地交付运行。

## 更多

- [HTTP - 维基百科](https://en.wikipedia.org/wiki/Hypertext%20Transfer%20Protocol)
- [HTTPS - 维基百科](https://en.wikipedia.org/wiki/HTTPS)
- [RFC 2616 - HTTP/1.1](https://tools.ietf.org/html/rfc2616 "Hypertext Transfer Protocol -- HTTP/1.1")
