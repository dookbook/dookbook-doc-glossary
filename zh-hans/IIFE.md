TOPIC: IIFE
AUTHORS: Crystal-RainSlide; Crystal-RainSlide@github.com; github:Crystal-RainSlide
         夏凌晨; xgqfrms@mozilla.net; mdn:xgqfrms

# IIFE（立即调用函数表达式）

IIFE（ 立即调用函数表达式）是一个在定义时就会立即执行的  JavaScript 函数。

```javascript
(function () {
    statements
})();
```

这是一个被称为 自执行匿名函数 的设计模式，主要包含两部分。第一部分是包围在 `圆括号运算符` `()` 里的一个匿名函数，这个匿名函数拥有独立的词法作用域。
这不仅避免了外界访问此 IIFE 中的变量，而且又不会污染全局作用域。

第二部分再一次使用 `()` 创建了一个立即执行函数表达式，JavaScript 引擎到此将直接执行函数。

## 示例

当函数变成立即执行的函数表达式时，表达式中的变量不能从外部访问。

```javascript
(function () {
    var aName = "Barry";
})();
// 无法从外部访问变量 name
aName // 抛出错误："Uncaught ReferenceError: aName is not defined"
```

将 IIFE 分配给一个变量，不是存储 IIFE 本身，而是存储 IIFE 执行后返回的结果。

```javascript
var result = (function () {
    var name = "Barry";
    return name;
})();
// IIFE 执行后返回的结果：
result; // "Barry"
```
