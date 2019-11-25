TOPICS: User Agent
        Web Browser

# 用户代理 (User Agent)

**用户代理**是代表一个人的计算机程序。

除了浏览器之外，用户代理可以是抓取网页的机器人、下载管理器或可以访问Web的其他应用程序。

垃圾邮件机器人、下载管理器和一些浏览器通常会发送一个*假*UA字符串来宣称自己是不同的客户端。这被称为*用户代理欺骗*。

## Web浏览器 (Web Browser)

最常见的用户代理是Web浏览器。网页浏览器是一种从[Web](/zh-hans/glossary/World_Wide_Web)获取和显示页面的程序，并且让用户通过**超链接**访问更多页面。

随着向服务器发送的每个请求，浏览器包含一个可表明身份的`User-Agent`[HTTP](/zh-hans/glossary/HyperText_Transfer_Protocol)的协议头，
叫作**用户代理**（**UA**，**User Agent**）字符串。此字符串通常标识浏览器、及其版本号及其主机操作系统。

用户代理的字符串可以被[[JavaScript]]在客户端中使用`navigator.userAgent`获取。

典型的用户代理字符串如下所示： `"Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:35.0) Gecko/20100101 Firefox/35.0"`。

### 常见浏览器

- [谷歌浏览器 (Google Chrome)](/zh-hans/glossary/Google_Chrome_Browser)
- [[Apple Safari]]
- [火狐 (Mozilla Firefox)](/zh-hans/glossary/Mozilla_Firefox)
- [Microsoft Edge](https://www.microsoft.com/windows/microsoft-edge)
- [欧朋浏览器 (Opera Browser)](http://www.opera.com/)

## 了解更多

- [User Agent维基百科](https://en.wikipedia.org/wiki/User%20agent)
- [RFC 2616: 14.43](https://tools.ietf.org/html/rfc2616): The `User-Agent` header
