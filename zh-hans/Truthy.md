TOPIC: Truthy
AUTHORS: Crystal-RainSlide; Crystal-RainSlide@github.com; github:Crystal-RainSlide
         庄引; zhuangyin8@gmail.com; github:zhuangyin8
         夏凌晨; xgqfrms@mozilla.net; mdn:xgqfrms
         晓月风尘; Serifx@mozilla.net; mdn:Serifx

# Truthy

在 JavaScript 中，**Truthy** (真值)指的是在 布尔值 上下文中转换后的值为真的值。所有值都是真值，
除非它们被定义为 falsy (即除了 `false`，`0`，`""`，`null`，`undefined` 和 `NaN` 外)。

JavaScript 在布尔值上下文中使用强制类型转换（coercion）。

JavaScript 中的真值示例如下（将被转换为 `true`，`if` 后的代码段将被执行）：

```javascript
if (true)
if ({})
if ([])
if (42)
if ("0")
if (new Date())
if (-42)
if (12n)
if (3.14)
if (-3.14)
if (Infinity)
if (-Infinity)
```
