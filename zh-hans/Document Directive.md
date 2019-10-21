TOPIC: Document Directive

# Document directive

**CSP 文档指令（document directives**） 出现于 `Content-Security-Policy` 首部，支配着应用安全策略的文档的属性或者
worker 运行环境的特征。

文档指令不将 `default-src` 指令作为回退机制。

以下 CSP 指令属于文档指令：

- [`base-uri`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/base-uri)
- [`plugin-types`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/plugin-types)
- [`sandbox`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/sandbox)
- [`disown-opener`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/disown-opener)
