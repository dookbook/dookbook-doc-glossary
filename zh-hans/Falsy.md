TOPIC: Falsy
AUTHORS: San; 1962511805@qq.com; github:Pedestrian93
         sub/dance; subdance@github.com; github:subdance
         Kid; kidonng@gmail.com; github:kidonng
         Re Tian; 745752067@qq.com; github:stephentian
         heqimagic; iheqi@github.com; github:iheqi
         庄引; zhuangyin8@gmail.com; github:zhuangyin8
         AlenQi; alenqimail@gmail.com; github:AlenQi

# Falsy

falsy 值 (虚值) 是在 Boolean 上下文中认定为 false 的值。

JavaScript 在需要用到布尔类型值的上下文中使用强制类型转换(Type Conversion )将值转换为布尔值，例如条件语句和循环语句。

!!! note
    在 JavaScript 中只有 6 个 falsy 值。
    这意味着当 JavaScript 期望一个布尔值，并被给与下面值中的一个时，它总是会被当做 false。
| | | |
| - | - | - |
| false | false | 关键字 |
| 0 | 数值 | zero<br>当 BigInt 作为布尔值使用时, 遵从其作为数值的规则. 0n 是 falsy 值.|
| "", '', `` | 这是一个空字符串 (字符串的长度为零). JavaScript 中的字符串可用双引号 "", 单引号 '', 或 模板字面量 `` 定义。|
| null | null - 缺少值 |
| undefined | undefined - 原始值 |
| NaN | NaN - 非数值 |

## 例子

JavaScript中falsy值的例子 (通过 if 代码段将falsy值转换为false):

```javascript
if (false)
if (null)
if (undefined)
if (0)
if (0n)
if (NaN)
if ('')
if ("")
if (``)
if (document.all)
```

### 逻辑与操作符 &&

如果第一个对象（译注：原文如此）是 falsy 值，则返回那个对象：

```javascript
let pet = false && "dog";

// ↪ false
```

!!! note
    `document.all` 在过去被用于浏览器检测，是[HTML规范在此定义了](url)故意与ECMAScript标准相违背的（译者注：`document.all`虽然是一个对象，
    但其转换为`boolean`类型是`false`），以保持与历史代码的兼容性  (`if (document.all) { // Internet Explorer code here }`
    或使用 `document.all` 而不先检查它的存在: `document.all.foo`).

falsy有时写作falsey，即使在英语中，通常将一个单词转换成形容词时，会去掉末尾的字母e，添加字母y。(比如：noise => noisy, ice => icy, shine => shiny)
