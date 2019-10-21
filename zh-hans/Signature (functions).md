TOPIC: Signature (functions)

# 函数签名

**函数签名**（或者类型签名，抑或方法签名）定义了 函数或方法的输入与输出。

签名可包含以下内容：

- 参数 及参数的 类型
- 一个的返回值及其类型
- 可能会抛出或传回的异常
- 该方法在 面向对象程序中的可用性方面的信息（如`public`、`static`或`prototype`）。

## 深入

### JavaScript中的签名

JavaScript 是一种类型松散或动态语言。这意味着您不必提前声明变量的类型。类型将在程序处理时自动确定。JavaScript中的签名仍然可以为您提供有关该方法的一些信息：

```javascript
MyObject.prototype.myFunction(value)
```

- 该方法是安装在一个名为`MyObject`的 对象上。
- 该方法安装在`MyObject`的原型上（因此它是一个instance method），而不是static method。
- 该方法名为`myFunction`。
- 该方法接受一个参数，该参数被称为`value`，且没有进一步定义。

### Java中的签名

在Java中，签名用于识别虚拟机代码级别的方法和类。你必须在代码中声明变量的类型才能运行Java代码。 Java是强类型的，将在编译时检查任何参数是否正确。

```java
public static void main(String[] args)
```

- `public`关键字是一个访问修饰符，表示该方法可以被任何对象调用。
- `static`关键字表示该方法是一个类方法，而不是一个实例方法。
- `void`关键字表示此方法没有返回值。
- 方法的名称为 `main`。
- 该方法接受一个字符串数组类型的参数。它被命名为`args`。
