TOPIC: Constructor

# Constructor

**构造函数**属于被实例化的特定类对象 。构造函数初始化这个对象，并提供可以访问其私有信息的方法。构造函数的概念可以应用于大多数面向对象的编程语言。本质上，JavaScript 中的构造函数通常在类的实例中声明。

## 语法

```javascript
// 这是一个通用的默认构造函数类 Default
function Default() {
}

// 这是一个带参数声明的重载构造函数类 Overloaded
function Overloaded(arg1, arg2, ...,argN){
}
```

要调用 JavaScript 中类的构造函数，请使用 `new` 操作符将新的对象引用分配给一个变量。

```javascript
function Default() {
}

// 分配给局部变量 defaultReference 的一个新的 Default 对象引用
var defaultReference = new Default();
```
