TOPIC: Object
       Object-Oriented Programming

# 对象 Object

**对象**指包含数据和用于处理数据的指令的**数据结构**。对象有时也指现实世界中的一些事, 例如在赛车游戏当中一辆车或者一幅地图都可以是一个对象。
[[JavaScript]], [[Java]], C++, [[Python]], 还有Ruby，都是面向对象的程序设计语言。

## 面向对象编程 (OOP)

**面向对象编程** (**OOP**)是一种*编程方法*，其中数据封装在**对象**中，对象本身在其上运行，而不是其组成部分。

### 静态方法

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
