TOPICS: HyperText Transfer Protocol

# 超文本传输协议 (HyperText Transfer Protocol, HTTP)

**HTTP**(**超文本传输协议**) 是用来在[Web](/zh-hans/glossary/World_Wide_Web)上传输文件的基础协议，
最典型的是在[浏览器](/zh-hans/glossary/Web_browser)和服务器之间传递以至于上网人员可以浏览他们。
目前HTTP最新版本是*HTTP/2*。

作为[[URI]]的一部分，`“http://”`被称为*模式*，通常位于地址的开头，例如“[https://dookbook.info](https://dookbook.info/)”，
就是指[浏览器](/zh-hans/glossary/Web_browser)利用HTTP协议请求文档。**https**在这个例子中指的是HTTP协议的安全版本，被称为**SSL**，或者**TLS**。

HTTP是**基于文本** (所有的通信都是以纯文本的形式进行) 以及**无状态的** (当前通信不会发现以前的通信状态)。
这个特点对在[Web](/zh-hans/glossary/World_Wide_Web)上访问网页的人是很理想的。而且，HTTP也可以让网站更加的灵活多变，利用在*AJAX*上等。

## HTTPS

**HTTPS**（全称：*Hyper Text Transfer Protocol over SecureSocket Layer*），是以安全为目标的HTTP通道，在HTTP的基础上通过传输加密和
身份认证保证了传输过程的安全性。HTTPS在HTTP的基础下加入**SSL**/**TLS**层，作为其安全基础。

HTTPS存在不同于HTTP(`80`)的默认端口`443`及一个加密/身份验证层（在HTTP与TCP之间）。这个系统提供了身份验证与加密通讯方法。
现在它被广泛用于万维网上安全敏感的通讯，例如交易支付等方面。

## HTTP/2

**HTTP/2**更简单,高效,强大.它在传输层解决了以前我们*HTTP1.x*中一直存在的问题.使用它可以优化我们的应用。
HTTP/2的首要目标是通过完全的请求，响应多路复用，头部的压缩头部域来减小头部的体积，添加了请求优先级，服务端推送。
为了支持这些特性,他需要大量的协议增加头部字段来支持，例如新的流量控制，差错处理，升级机制。而这些是每个Web开发者都应该在他们的应用中用到的。

HTTP/2并没有在应用中改变HTTP的语义，而是通过在客户端和服务端传输的数据格式(**frame**)和传输。
它通过在新的二进制帧层控制整个过程以及隐藏复杂性,而这不需要改变原来有的东西就可以实现.

## 更多

- [HTTP维基百科](https://en.wikipedia.org/wiki/Hypertext%20Transfer%20Protocol)
- [HTTPS维基百科](https://en.wikipedia.org/wiki/HTTPS)
- [RFC 2616 关于HTTP/1.1](https://tools.ietf.org/html/rfc2616 "Hypertext Transfer Protocol -- HTTP/1.1")
