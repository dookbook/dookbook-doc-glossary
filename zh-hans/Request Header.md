TOPIC: Request Header
AUTHORS: 张可携; kexiezhang@gmail.com; github:C1erman
         huangl7759; huangl7759@github.com; github:huangl7759

# 请求头

**请求头**可以被定义为：被用于HTTP请求中并且和请求主体无关的那一类HTTP header。某些请求头如`Accept`, `Accept-*`,
`If-*`允许执行条件请求。某些请求头如：`Cookie`, `User-Agent` 和`Referer`描述了请求本身以确保服务端能返回正确的响应。

并非所有出现在请求中的HTTP首部都属于请求头，例如在 `POST`请求中经常出现的`Content-Length`实际上是一个代表请求主体大小的entity header，虽然你也可以把它叫做请求头。

此外，CORS定义了一个叫做 simple headers的集合，它是请求头集合的一个子集。如果某次请求是只包含simple headers的话，则被认为是简单请求，不会触发请求预检（preflight）。

下面是一个HTTP请求的请求头：

```http
GET /home.html HTTP/1.1
Host: developer.mozilla.org
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.9; rv:50.0) Gecko/20100101 Firefox/50.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br
Referer: https://developer.mozilla.org/testpage.html
Connection: keep-alive
Upgrade-Insecure-Requests: 1
If-Modified-Since: Mon, 18 Jul 2016 02:36:04 GMT
If-None-Match: "c561c68d0ba92bbeb8b0fff2a9199f722e3a621a"
Cache-Control: max-age=0
```

严格来说在这个例子中的`Content-Length`不是一个请求头，而是一个实体头（entity header）：

```http
POST /myform.html HTTP/1.1
Host: developer.mozilla.org
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.9; rv:50.0) Gecko/20100101 Firefox/50.0
Content-Length: 128
```
