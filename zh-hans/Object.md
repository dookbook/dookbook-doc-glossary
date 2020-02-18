TOPIC: Object-Oriented Programming

# 面向对象编程 (OOP)

**面向对象编程** (**OOP**)是一种*编程方法*，其中数据封装在**对象**中，对象本身在其上运行，而不是其组成部分。

## 对象 (Object)

**对象**指包含数据和用于处理数据的指令的**数据结构**。对象有时也指现实世界中的一些事, 例如在赛车游戏当中一辆车或者一幅地图都可以是一个对象。
[[JavaScript]], [[Java]], C++, 还有[[Python]]，都是面向对象的程序设计语言。

## 属性 (Property)

**属性**是对象的特征，通常描述与数据结构相关的属性。

有两种类型的属性：

- **实例属性**保存特定于给定对象实例的数据。
- **静态属性**保存所有对象实例之间共享的数据。

属性具有*名称*（字符串）和*值*（原型类型，方法或对象引用）。
注意，当我们说“一个属性是一个对象”时，它是“一个属性持有一个对象引用”的简写。这种区别很重要，因为当您更改属性的值时，原始引用的对象保持不变。

## 方法 (Method)

**方法**是一种函数，它是对象的属性。方法有两种：*实例方法*是由对象实例执行的内置任务，而*静态方法*是直接在对象构造函数上调用的任务。

!!! info
    在[[JavaScript]]中，函数本身就是对象，因此，在这种情况下，方法实际上是对函数的对象引用。

### 静态方法 (Static Method)

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

## 继承 (Inheritance)

**继承**是*面向对象编程*的主要功能。**数据[抽象](/zh-hans/glossary/abstraction)**可以携带多个层级，也就是说，类可以具有**父类**（**超类**）和**子类**。

作为应用程序开发人员，您可以选择保留并添加您自己的超类的属性和方法，从而使类定义非常灵活。 有些语言允许一类从多个父类继承（**多重继承**）。

## 对象引用 (Object Reference)

指向**对象**的链接。

**对象引用**的概念，即当将同一对象分配给多个**属性**时，则每个属性都拥有链接到同一对象的对象引用，而不是持有该对象的副本。因此，当对象更改时，引用该对象的所有属性都会同时更改。

## 了解更多

- [OOP - 维基百科](https://en.wikipedia.org/wiki/Object-oriented%20programming)
- [基于类的编程 - 维基百科](https://en.wikipedia.org/wiki/Class-based_programming)
- [属性 (编程) - 维基百科](https://en.wikipedia.org/wiki/Property%20(programming))
- [方法 (计算机编程) - 维基百科](https://en.wikipedia.org/wiki/Method%20(computer%20programming))
- [OOP的构造函数 - 维基百科](https://en.wikipedia.org/wiki/Constructor_%28object-oriented_programming%29)
- [实例 - 维基百科](https://en.wikipedia.org/wiki/Instance%20(computer%20science))
- [引用 (计算机科学) - 维基百科](https://en.wikipedia.org/wiki/Reference%20(computer%20science))
