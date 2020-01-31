TOPIC: Syntax
       Statement
       Control Flow
       Conditional
       Loop
       Function
AUTHORS: San; 1962511805@qq.com; github:Pedestrian93
         Crystal-RainSlide; Crystal-RainSlide@github.com; github:Crystal-RainSlide
         xgqfrms; xgqfrms@github.com; github:xgqfrms
         Liao Yazhi; 1594435860@qq.com; github:Liaoyazhi
         Li Yun; leven.cn@gmail.com; github:leven-cn

# 语法: 语句，控制流 和 函数

**语法**指定组成正确*结构化代码*的**所需字符组合和顺序**。语法因语言而异（例如，[[HTML]]和[[JavaScript]]中的语法不同）。语法适用于*编程语言*（计算机命令）和*标记语言*（文档结构信息）。

语法仅控制**顺序**和**结构**。指令也必须有意义，这是语义的限制。

代码必须具有正确的语法才能正确编译，否则会发生*语法错误*。即使是很小的错误，例如缺少括号，也可以阻止源代码的编译。

如果框架产生简单、可读、简洁的结果，则据说它们具有“**干净**”的语法。如果代码库使用“很多语法”，则它需要更多字符才能实现相同的功能。

## 语句 (Statement)

在计算机编程语言中，**语句**是一行任务指令的代码。每个程序都包含若干语句。

## 控制流 (Control Flow)

**控制流**是计算机编程语言中执行*语句*的**顺序**。

一般情况下，代码从文件的第一行到最后一行按顺序执行，除非计算机运行在不同的控制结构下。

典型的编程语言包括许多控制结构：**条件**，**循环**和**函数**。还有一些编程语言也可以设置在**事件**触发时执行。

### 条件 (Conditional)

**条件**是一组规则，可以根据条件是否完成而中断正常的代码执行或对其进行更改。

如果满足特定条件，则执行一条指令或一组指令。否则，将执行另一条指令。在条件尚未满足的情况下，也可以重复执行一条指令或一组指令。

### 循环 (Loop)

**循环**是指一系列指令被**连续重复**执行直到在计算机编程中满足特定条件为止。一个示例是获取数据项并对其进行更改，然后确保检查某些条件（例如，计数器是否达到规定数量）的过程。

## 函数 (Function)

**函数**，是一个可以被其他代码或其自身调用的*代码片段*，或者是一个指向该函数的变量。当函数被调用时，*参数*被作为输入传递给函数，
并且函数可以返回输出。在 [[JavaScript]] 中，函数也是一个[对象](/zh-hans/webfrontend/object)。

函数名是作为*函数声明*或*函数表达式*的一部分声明的 *[标识符](/zh-hans/glossary/identifier)*。函数的 *[作用域](/zh-hans/glossary/scope)*取决于函数名是一个声明还是表达式。

### 函数类型

#### 匿名函数

**匿名函数**是一个**没有函数名的函数**：

```javascript
function () {};

// or using the ECMAScript 2015 arrow notation
() => {};
```

#### 命名函数

**命名函数**是**具有函数名称的函数**：

```javascript
function foo() {};

// or using the ECMAScript 2015 arrow notation
const foo = () => {};
```

#### 内部函数

**内部函数**是另一个函数内的函数（下面例子中的`square`）。外部函数是包含一个函数的函数（下面例子中的`addSquares`）：

```javascript
function addSquares(a,b) {
   function square(x) {
      return x * x;
   }
   return square(a) + square(b);
};

//Using ECMAScript 2015 arrow notation
const addSquares = (a,b) => {
   const square = x => x*x;
   return square(a) + square(b);
};
```

#### 递归函数

**递归函数**是**调用自身的函数**。可参考[递归](/zh-hans/glossary/Recursion)。

```javascript
function loop(x) {
   if (x >= 10)
      return;
   loop(x + 1);
};

//Using ECMAScript 2015 arrow notation
const loop = x => {
   if (x >= 10)
      return;
   loop(x + 1);
};
```

#### 立即调用函数表达式 (IIFE)

**立即调用函数表达式**（**IIFE**）是一种被加载到浏览器的编译器之后直接调用的函数。识别IIFE的方法是通过在函数声明的末尾定位额外的左和右括号。

```javascript
// Error (https://en.wikipedia.org/wiki/Immediately-invoked_function_expression)
/*
​function foo() {
    console.log('Hello Foo');
}();
*/

(function foo() {
    console.log("Hello Foo");
}());

(function food() {
    console.log("Hello Food");
})();
```

如果你想进一步了解 IIFE, 可参考维基百科：[Immediately Invoked Function Expression](https://en.wikipedia.org/wiki/Immediately-invoked_function_expression)

## 更多

- [语法 (编程语言) - 维基百科](https://en.wikipedia.org/wiki/Syntax%20(programming%20language))
- [Syntax Error - 维基百科](https://en.wikipedia.org/wiki/Syntax%20error)
- [语句 (计算机科学) - 维基百科](https://en.wikipedia.org/wiki/Statement%20(computer%20science))
- [控制流 - 维基百科](https://en.wikipedia.org/wiki/Control%20flow)
- [条件 - 维基百科](https://en.wikipedia.org/wiki/Exception_handling#Condition_systems)
- [立即调用函数表达式 - 维基百科](https://en.wikipedia.org/wiki/Immediately-invoked_function_expression)
