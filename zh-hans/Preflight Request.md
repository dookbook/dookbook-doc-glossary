TOPIC: Preflight Request
AUTHORS: Xinye Dai; me@daixinye.com; github:daixinye

# Preflight Request

一个 CORS 预检请求是用于检查服务器是否支持 CORS 即跨域资源共享。

它一般是用了以下几个 HTTP 请求首部的 `OPTIONS` 请求：`Access-Control-Request-Method` 和
`Access-Control-Request-Headers`，以及一个 `Origin` 首部。

当有必要的时候，浏览器会自动发出一个预检请求；所以在正常情况下，前端开发者不需要自己去发这样的请求。

举个例子，一个客户端可能会在实际发送一个 `DELETE` 请求之前，先向服务器发起一个预检请求，用于询问是否可以向服务器发起一个 `DELETE` 请求：

```http
OPTIONS /resource/foo
Access-Control-Request-Method: DELETE
Access-Control-Request-Headers: origin, x-requested-with
Origin: https://foo.bar.org
```

如果服务器允许，那么服务器就会响应这个预检请求。并且其响应首部 `Access-Control-Allow-Methods` 会将 `DELETE` 包含在其中：

```http
HTTP/1.1 204 No Content
Connection: keep-alive
Access-Control-Allow-Origin: https://foo.bar.org
Access-Control-Allow-Methods: POST, GET, OPTIONS, DELETE
Access-Control-Max-Age: 86400
```
