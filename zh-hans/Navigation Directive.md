TOPIC: Navigation Directive

# Navigation directive

**CSP 浏览指令（navigation directives）** 出现于 `Content-Security-Policy` 首部，支配着用户所能浏览的或者提交表单的资源位置。

浏览指令不将 `default-src` 指令作为回退机制。

以下 CSP 指令属于浏览指令：

- [`form-action`](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy/form-action)
- [`frame-ancestors`](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy/frame-ancestors)
- [`navigate-to`](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy/navigation-to)
