TOPIC: JavaScript

# JavaScript编程语言

JavaScript (JS) 是一种编程语言，为通常用于客户端（client-side）的网页动态脚本，不过，也常通过像[Node.js](http://nodejs.org/)这样的包，用于服务器端（server-side）。

不应该把JavaScript和[[Java]]混淆。“Java”和“JavaScript”都是Oracle（甲骨文）公司在美国和其他国家注册的商标，但是这两种编程语言在语法、语义和使用方面都明显不同。

## 历史

*Brendan Eich*（彼时受雇于Netscape（网景）公司）为服务器端构想的语言JavaScript，不久却在1995年9月加入*Netscape Navigator 2.0*项目。
JavaScript很快获得了成功，而Internet Explorer 3.0也在1996年8月引入了对JavaScript的支持，冠以*JScript*之名。

1996年11月，Netscape开始与[[ECMA]]国际化组织合作以使JavaScript成为行业标准。从此以后，标准化的JavaScript就被称为 *[[ECMAScript]]*，并规范于
**ECMA-262**之下。

## 应用场景

JavaScript通常用于*浏览器*，使开发者能通过[[DOM]]来操纵网页内容、或透过[[AJAX]] 与IndexedDB 来操作数据；还可以用它在canvas上面绘图、通过各种APIs与运行浏览器的
各种设备交互等等。由于近年来的发展、以及各浏览器的APIs性能改善，JavaScript成了世界上最常用的编程语言之一。

最近，JavaScript的流行程度 ，由于 **[Node.js](http://nodejs.org/)**平台 —— 这个除浏览器外最流行的跨平台JavaScript运行环境 —— 的成功而大大提升。
Node.js 使开发者可以在PC上使用JavaScript作为脚本语言使用以自动化处理和构建功能完备的 [[HTTP]] 和 [[WebSocket]] 服务器。

## 面向对象

JavaScript是高度**面向对象**的。它遵循基于**原型**（**`prototype`**）的模型（相比于基于类的模型）。

### 继承与原型链

对于使用过基于类的语言 (如 Java 或 C++) 的开发人员来说，JavaScript 有点令人困惑，因为它是*动态*的，并且本身不提供一个 class的实现。（在 *ES2015*/*ES6*
中引入了 `class` 关键字，但那只是*语法糖*，JavaScript仍然是**基于原型**的）。

当谈到**继承**时，JavaScript 只有一种结构：对象。每个实例对象（ object ）都有一个*私有属性*（称之为 *`__proto__`*）指向它的构造函数的**原型对象**（**`prototype`**）。
该原型对象也有一个自己的原型对象( `__proto__` ) ，层层向上直到一个对象的原型对象为 *`null`*。根据定义，`null` 没有原型，并作为这个**原型链**中的最后一个环节。

几乎所有 JavaScript 中的对象都是位于原型链**顶端**的 [Object](/zh-hans/webfrontend/Object) 的实例。

尽管这种原型继承通常被认为是 JavaScript 的弱点之一，但是原型继承模型本身实际上比经典模型更强大。例如，在原型模型的基础上构建经典模型相当简单。

## 动态类型

JavaScript是一种*弱类型*或者说 *[动态语言](/zh-hans/glossary/dynamic_programming_language)*。这意味着你不用提前声明变量的类型，在程序运行过程中，类型会被自动确定。这也意味着你可以使用同一个变量保存不同类型的数据：

```javascript
let foo = 42;    // foo现在是数字
foo     = 'bar'; // foo现在是字符串
foo     = true;  // foo现在是布尔类型
```

## 数据类型

最新的[[ECMAScript]]标准定义了8种数据类型:

- 7种原始类型:
    - [`boolean`](/zh-hans/webfrontend/Boolean)
    - [`null`](/zh-hans/webfrontend/null)
    - [`undefined`](/zh-hans/webfrontend/undefined)
    - [`number`](/zh-hans/webfrontend/Number)
    - [`bigint`](/zh-hans/webfrontend/BigInt)
    - [`string`](/zh-hans/webfrontend/String)
    - `symbol` (ECMAScript 2016新增)
- 和[`Object`](/zh-hans/webfrontend/Object)。

### JavaScript中的基本类型的包装对象

除了[`null`](/zh-hans/webfrontend/null)和[`undefined`](/zh-hans/webfrontend/undefined)之外，所有基本类型都有其对应的包装对象：

- [`String`](/zh-hans/webfrontend/String)为字符串基本类型`string`。
- [`Number`](/zh-hans/webfrontend/Number)为数值基本类型`number`。
- [`BigInt`](/zh-hans/webfrontend/BigInt)为`bigint`基本类型。
- [`Boolean`](/zh-hans/webfrontend/Boolean)为布尔基本类型`boolean`。
- `Symbol`为字面量基本类型。

这个包裹对象的`valueOf()`方法返回基本类型值。

## `for` 循环

### `for` 循环的语法

```javascript
for (statement 1; statement 2; statement 3) {
  execute code block
}
```

- `statement 1` 在代码块执行之前执行一次。

- `statement 2` 定义了代码执行条件的判断。

- `statement 3` 每次在代码块执行后执行一次。

### `for` 循环的示例

```javascript
for (var i = 0; i < 10; i++) {
  console.log(i)
}
// 这个循环会打印数字0到9，然后在条件(i=10)成立时停止循环。
```

以上示例中，语法如下：

- 语句1设置循环变量 (`var i = 0`)。

- 语句2设置循环条件 (`i < 10`)。

- 语句3每次在代码块执行之后递增变量`i` (`i++`)。

## `while` 循环

### `while` 循环的语法

```javascript
// 代码块将一直执行到`condition`为`true`为止
while (condition) {
  execute code block
}
```

### `while` 循环的示例

```javascript
var i = 0;
while (i < 5) {
  console.log(i)
  i++
}

// 这个循环将打印数字0到4，然后当条件为`false` (i>=5) 时停止循环。
```

## 严格模式

JavaScript的**严格模式**是选择加入JavaScript的受限变体的一种方法，从而隐式退出“*草率模式*”。严格模式不仅仅是一个子集：它有意地具有与普通代码不同的语义。

整个脚本的严格模式可通过以下方式调用：在任何其他声明之前声明 **`"use strict";`**。

## 了解更多

- [JavaScript - 维基百科](https://en.wikipedia.org/wiki/JavaScript)
- [ECMAScript (ECMA-262)标准](http://www.ecma-international.org/publications/standards/Ecma-262.htm)
