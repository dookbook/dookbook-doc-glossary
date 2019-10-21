TOPIC: Fetch Directive

# Fetch 指令

**CSP fetch** 指令用在`Content-Security-Policy` 头部中，可以用来控制某些具体类型的资源可以从哪些来源被加载。比如说，
`script-src` 使得开发者可以允许可信任来源的脚本在页面上执行， `font-src` 可以控制字体的来源。

所有的指令的值都会回落到 default-src。也就是说，如果某个fetch指令在CSP头部中未定义， 那么用户代理就会寻找default-src 指令的值来替代。

这些 CSP 指令属于fetch指令:

- [`child-src`](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy/child-src)
- [`connect-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/connect-src)
- [`default-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/default-src)
- [`font-src`](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy/font-src)
- [`frame-src`](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy/frame-src)
- [`img-src`](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy/img-src)
- [`manifest-src`](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy/manifest-src)
- [`media-src`](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy/media-src)
- [`object-src`](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy/object-src)
- [`script-src`](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy/script-src)
- [`style-src`](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy/style-src)
- [`worker-src`](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy/worker-src)
