TOPIC: Symbol
AUTHORS: Xu Xinhang; xuxinhang@github.com; github:xuxinhang
         After Amiao Look; kv.ch40@gmail.com; github:4fterlook
         庄引; zhuangyin8@gmail.com; github:zhuangyin8

# Symbol

这个技术术语页面同时描述了一种称为 “**symbol**” 的数据类型，还有一个像类的函数 “`Symbol()`”，用来创建 **symbol** 数据类型实例。

数据类型 “**symbol**” 是一种原始数据类型，该类型的性质在于这个类型的值可以用来创建匿名的对象属性。该数据类型通常被用作一个对象属性的键值——当你想让它是私有的时候。
例如，**symbol** 类型的键存在于各种内置的 JavaScript 对象中。同样，自定义类也可以这样创建私有成员。**symbol** 数据类型具有非常明确的目的，并且因为其功能性单一的优点而突出；
一个 **symbol** 实例可以被赋值到一个左值变量，还可以通过标识符检查类型，这就是它的全部特性。不能对该类型实例使用其他操作符（将“**Symbol**”类型的实例与 “**Number**”
类型的实例对比，例如整数 42，该实例就具有将值与其他类型的值进行比较或组合的运算符）。

一个具有数据类型 “**symbol**” 的值可以被称为 “符号类型值”。在 JavaScript 运行时环境中，一个符号类型值可以通过调用函数 `Symbol()` 创建，这个函数动态地生成了一个匿名，
唯一的值。Symbol类型唯一合理的用法是用变量存储 symbol的值，然后使用存储的值创建对象属性。以下示例使用"var"创建一个变量来保存 symbol。

```javascript
var  myPrivateMethod  = Symbol();
this[myPrivateMethod] = function() {...};
```

当一个 symbol 类型的值在属性赋值语句中被用作标识符，该属性（像这个 symbol 一样）是匿名的；并且是不可枚举的。因为这个属性是不可枚举的，它不会在循环结构 “`for( ... in ...)`”
中作为成员出现，也因为这个属性是匿名的，它同样不会出现在 “`Object.getOwnPropertyNames()`” 的返回数组里。这个属性可以通过创建时的原始 symbol 值访问到，
或者通过遍历 “`Object.getOwnPropertySymbols()`” 返回的数组。在之前的代码示例中，通过保存在变量 `myPrivateMethod`的值可以访问到对象属性。

内置函数 “`Symbol()`” 是一个不完整的类，当作为函数调用时会返回一个 symbol 值，试图通过语法 “`new Symbol()`” 作为构造函数调用时会抛出一个错误。
它有一些静态方法来访问 JavaScript 全局 symbol 表，还有一些静态属性用来保存已存在通用对象里的特定 symbol 地址。通过 `Symbol()` 函数创建 symbol 值已在上面解释过。
理解试图将 `Symbol()`作为构造函数使用会抛出错误可以提前预防意外（当作构造函数使用）创建对象导致的混乱。访问全局 symbol 注册表的方法是 `Symbol.for()`和
`Symbol.keyFor()`；它们斡旋在全局 symbol 表（或注册表）与运行时环境之间。symbol 注册表通常构建在 JavaScript 编译器基础设施，所以 symbol 注册表的
内容不会出现 JavaScript 运行时环境，除了通过它们的反射方法。`Symbol.for("tokenString")` 方法从注册表返回一个 symbol 值，
`Symbol.keyFor(symbolValue)` 方法从注册表返回 token 字符串；正好相反，所以下面为 true：

```javascript
Symbol.keyFor(Symbol.for("tokenString"))=="tokenString";  // true
```

**Symbol** 类具有一些静态属性，对于匿名命名来说，这带有一点讽刺意味。这类属性只有几个; 它们是所谓的“众所周知”的 symbol。 它们是在某些内置对象中找到的某些特定方法属性的 symbol。
暴露出这些 symbol 使得可以直接访问这些行为；这样的访问可能是有用的，例如在定义自定义类的时候。 普遍的 symbol 的例子有：“`Symbol.iterator`”用于类似数组的对象，“`Symbol.search`”用于字符串对象。

`Symbol()`函数及其创建的 symbol 值可能对设计自定义类的编程人员有用。 symbol 值提供了一种自定义类可以创建私有成员的方式，并维护一个仅适用于该类的 symbol 注册表。
自定义类可以使用 symbol 值来创建“自有”属性，这些属性避免了不必要的被偶然发现带来的影响。 在类定义中，动态创建的 symbol 值将保存到作用域变量中，该变量只能在类定义中私有地使用。
没有 token 字符串; 作用域变量起到 token 的等同作用。

Symbol 是 JavaScript 的 原始数据类型 ，`Symbol`实例是唯一且不可改变的.  

在一些编程语言中 symbol也被称为原子(atoms).

在JavaScript中，Symbol 是 基本数据类型 的一种，Symbol 对象是 Symbol原始值的封装 。

Symbol 的描述是可选的，但仅用于调试目的。

Symbol 类型是 ECMAScript 2015 中新添加的特性，在ECMAScript 5中没有对应的类型。

```javascript
Symbol("foo") !== Symbol("foo")
const foo = Symbol()
const bar = Symbol()
typeof foo === "symbol"
typeof bar === "symbol"
let obj = {}
obj[foo] = "foo"
obj[bar] = "bar"
JSON.stringify(obj) // {}
Object.keys(obj) // []
Object.getOwnPropertyNames(obj) // []
Object.getOwnPropertySymbols(obj) // [ foo, bar ]
```
