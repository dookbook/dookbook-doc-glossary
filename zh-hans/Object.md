TOPIC: Object-Oriented Programming

# 面向对象编程 (OOP)

**面向对象编程** (**OOP**)是一种*编程方法*，其中数据封装在**对象**中，对象本身在其上运行，而不是其组成部分。

## 对象 (Object)

**对象**指包含数据和用于处理数据的指令的**数据结构**。对象有时也指现实世界中的一些事, 例如在赛车游戏当中一辆车或者一幅地图都可以是一个对象。
[[JavaScript]], [[Java]], C++, 还有[[Python]]，都是面向对象的程序设计语言。

## 类 (Class)

在面向对象的程序设计中，“类”定义对象的“特性”。 类是*对象属性和方法的模板定义*，是绘制对象的特定实例的“蓝图”。

## 构造函数 (Constructor)

**构造函数**属于被实例化的特定类对象。构造函数初始化这个对象，并提供可以访问其私有信息的方法。构造函数的概念可以应用于大多数面向对象的编程语言。本质上，[[JavaScript]]中的构造函数通常在类的实例中声明。

### JavaScript中的构造函数

```javascript
// 这是一个通用的默认构造函数类 Default
function Default() {
}

// 这是一个带参数声明的重载构造函数类 Overloaded
function Overloaded(arg1, arg2, ...,argN){
}
```

要调用[[JavaScript]]中类的构造函数，请使用`new`操作符将新的对象引用分配给一个变量。

```javascript
function Default() {
}

// 分配给局部变量 defaultReference 的一个新的 Default 对象引用
var defaultReference = new Default();
```

## 实例 (Instance)

构造函数创建的对象是该构造函数的实例。

## 静态方法 (Static Method)

**静态方法**（或**静态函数**）是定义为对象的方法，但可以直接从对象API的构造函数或类访问，而不是通过构造函数创建的对象实例访问。

在Web API中，静态方法是一种由接口定义的方法，但是可以在不首先实例化该类型的对象的情况下调用它。

在对象实例上调用的方法称为“*实例方法*”。

例如，在Notifications API中，在实际的Notification构造函数本身上调用了`Notification.requestPermission()`方法 - 这是一个静态方法：

```javascript
let promise = Notification.requestPermission();
```

另一方面，`Notification.close()`方法是一个实例方法 - 在特定的通知对象实例上调用以关闭其表示的系统通知：

```javascript
let myNotification = new Notification('This is my notification');

myNotification.close();
```

## 了解更多

- [OOP - 维基百科](https://en.wikipedia.org/wiki/Object-oriented%20programming)
- [Class-Based Programming - 维基百科](https://en.wikipedia.org/wiki/Class-based_programming)
- [Constructor for OOP - 维基百科](https://en.wikipedia.org/wiki/Constructor_%28object-oriented_programming%29)
- [Instance - 维基百科](https://en.wikipedia.org/wiki/Instance%20(computer%20science))
