TOPIC: Origin
AUTHORS: xgqfrms; xgqfrms@github.com; github:xgqfrms

# Origin

Web内容的源由用于访问它的URL 的方案(协议)，主机(域名)和端口定义。只有当方案，主机和端口都匹配时，两个对象具有相同的起源。

某些操作仅限于同源内容，而可以使用 CORS 解除这个限制。

## 同源的例子

|  |  |
| -- | -- |
| `http://example.com/app1/index.html`<br>`http://example.com/app2/index.html` | same origin because same scheme (`http`) and host (`example.com`) |
| `http://Example.com:80`<br>`http://example.com` | same origin because a server delivers HTTP content through port 80 by default |

## 不同源的例子

|  |  |
| -- | -- |
| `http://example.com/app1`<br>`https://example.com/app2` | different schemes |
| `https://example.com/app2`<br>`http://www.example.com`<br>`http://myapp.example.com` | different hosts |
| `http://example.com`<br>`http://example.com:8080` | different ports |

## Specifications

| Specification | Status | Comment |
| -- | -- | -- |
| HTML Living Standard The definition of 'origin' in that specification. | Living Standard |  |
