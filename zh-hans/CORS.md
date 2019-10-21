TOPIC: CORS
AUTHORS: Wu Yuping; fs523577192@gmail.com; github:fs523577192
         夏凌晨; xgqfrms@mozilla.net; mdn:xgqfrms

# CORS

**CORS** （Cross-Origin Resource Sharing，跨域资源共享）是一个系统，它由一系列传输的HTTP头组成，这些HTTP头决定浏览器是否阻止前端 JavaScript 代码获取跨域请求的响应。

同源安全策略 默认阻止“跨域”获取资源。但是 CORS 给了web服务器这样的权限，即服务器可以选择，允许跨域请求访问到它们的资源。

## 了解更多

### 总体了解

- MDN上的 Cross-Origin Resource Sharing (CORS)
- 维基百科上的 [Cross-origin resource sharing](https://zh.wikipedia.org/wiki/Cross-origin%20resource%20sharing)

### CORS 头

`Access-Control-Allow-Origin`

指示请求的资源能共享给哪些域。

`Access-Control-Allow-Credentials`

指示当请求的凭证标记为 true 时，是否响应该请求。

`Access-Control-Allow-Headers`

用在对预请求的响应中，指示实际的请求中可以使用哪些 HTTP 头。

`Access-Control-Allow-Methods`

指定对预请求的响应中，哪些 HTTP 方法允许访问请求的资源。

`Access-Control-Expose-Headers`

指示哪些 HTTP 头的名称能在响应中列出。

`Access-Control-Max-Age`

指示预请求的结果能被缓存多久。

`Access-Control-Request-Headers`

用于发起一个预请求，告知服务器正式请求会使用那些 HTTP 头。

`Access-Control-Request-Method`

用于发起一个预请求，告知服务器正式请求会使用哪一种 HTTP 请求方法。

`Origin`

指示获取资源的请求是从什么域发起的。

### 技术引用

- [Fetch 规范](https://fetch.spec.whatwg.org/)
