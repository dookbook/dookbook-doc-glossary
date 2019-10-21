TOPIC: HSTS

# HSTS

**HTTP严格传输安全** 让网站可以通知浏览器它不应该再使用HTTP加载该网站，而是自动转换该网站的所有的HTTP链接至更安全的HTTPS。
它包含在HTTP的协议头 `Strict-Transport-Security` 中，在服务器返回资源时带上。

换句话说，它告诉浏览器将URL协议从HTTP更改为HTTPS（会更安全），并要求浏览器对每个请求执行此操作。
