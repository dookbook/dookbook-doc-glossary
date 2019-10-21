TOPIC: Simple Header
AUTHORS: huangl7759; huangl7759@github.com; github:huangl7759

# 简单头部

以下的 HTTP headers都可以被认为是简单头部:

- `Accept`,
- `Accept-Language`,
- `Content-Language`,
- `Content-Type` 并且值是 `application/x-www-form-urlencoded`, `multipart/form-data`, 或者 `text/plain`之一的（忽略参数）.

或者以下客户端头部之一的也可以被认为是简单头部：

- `DPR`
- `Downlink`
- `Save-Data`
- `Viewport-Width`
- `Width`

当只包含简单头部时，一个请求则被视为简单请求并且在CORS中不需要发送preflight request。
