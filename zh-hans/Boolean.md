TOPIC: Boolean

# Boolean

在计算机科学中，**布尔值**是一种取值仅能为 真 或 假 的数据类型，它赋予了编程语言在逻辑上表达真 或 假 的能力。如果没有这种能力，很多功能将无法被实现。举个例子，JavaScript中的 if
语句 需要一些判断条件来决定接下来的代码会否被执行，而这些条件，本质上会被解释成一个布尔值。又如JavaScript中的 for 循环，如果没有一个能够解释成布尔值的判断条件，循环将无法知道自己什么时候该结束。

```javascript
/* JavaScript if statement */
if (boolean conditional) {
   // code to execute if the conditional is true
}

if (boolean conditional) {
  console.log("boolean conditional resolved to true");
} else {
  console.log("boolean conditional resolved to false");
}


/* JavaScript for loop */
for (control variable; boolean conditional; counter) {
  // code to execute repeatedly if the conditional is true
}

for (var i=0; i < 4; i++) {
  console.log("I print only when the boolean conditional is true");
}
```
