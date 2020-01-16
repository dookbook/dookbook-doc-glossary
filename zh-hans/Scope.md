TOPIC: Scope

# 作用域

即**当前的执行上下文**。上下文中的“*值*”和“*表达式*”为“*可见*”或可以引用。如果*变量*或其他*表达式*不在“当前作用域”中，则无法使用它。**作用域**也可以分层次，以便*子作用域*可以访问*父作用域*，反之亦然。

## 全局作用域

在编程环境中，**全局作用域**是包含所有其他范围并在所有其他范围中可见的范围。

在客户端[[JavaScript]]中，**全局作用域**通常是在其中执行所有代码的网页。

## 局部作用域

**局部作用域**是使变量成为局部变量的特征（即变量名仅在非*全局作用域*的作用域内绑定到其值）。

## 全局变量

**全局变量**是在*全局作用域*中声明的变量，也就是说，在所有其他作用域内可见的变量。

在[[JavaScript]]中，它是全局对象的属性。

## 局部变量

名称仅在*本地作用域*内绑定到其值的变量。

```javascript
var global = 5;  // 全局变量

function fun(){
  var local = 10;  // 局部变量
}
```

## JavaScript示例

**函数**在[[JavaScript]]中用作 *闭包*，因此可以创建作用域，所以（例如）不能从函数外部或其他内部访问仅在函数内部定义的变量。 例如，以下是**错误**的：

```javascript
function exampleFunction() {
    var x = "declared inside function";  // x can only be used in exampleFunction
    console.log("Inside function");
    console.log(x);
}

console.log(x);  // 抛出异常
```

但是，由于变量是在函数外部声明的，因此以下代码有效，使其成为*全局变量*：

```javascript
var x = "declared outside function";

exampleFunction();

function exampleFunction() {
    console.log("Inside function");
    console.log(x);
}

console.log("Outside function");
console.log(x);
```

## 更多

- [Scope (计算机科学) - 维基百科](https://en.wikipedia.org/wiki/Scope%20(computer%20science))
- [Global Variable - 维基百科](https://en.wikipedia.org/wiki/Global%20variable)
- [Local Variable - 维基百科](https://en.wikipedia.org/wiki/Local%20variable)
