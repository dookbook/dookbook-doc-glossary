TOPIC: Cascading Style Sheets

# 层叠样式表 (CSS)

**CSS**（**Cascading Style Sheets**，**层叠样式表**）是用来控制网页在浏览器中的显示外观的*声明式语言*。浏览器会根据 CSS 的样式定义将其选定的元素显示为恰当的形式。
一条 CSS 的样式定义包括**属性**和**属性值**，它们共同决定网页的外观。

CSS 与 [[HTML]] 和 [[JavaScript]] 并称 [Web](/zh-hans/glossary/World_Wide_Web) 三大核心技术。
一般用它来定义 HTML 元素 的样式，但它也能用于其他标记语言，如 [[SVG]] 和 XML。

一条 CSS *规则*包含一个 *选择符* 和一组 *属性* 定义。下面这个例子用来将页面中的所有 `<p>` 标签显示为黑色背景和黄色文本：

```css
/* p 选择符用来选择页面中的所有 <p> 标签 */
p {
  /* color 属性用来定义文本颜色，这里为黄色 */
  color: yellow;

  /* background-color 属性用来定义元素的背景色，这里为黑色 */
  background-color: black
}
```

CSS 中的 “*C*” (*Cascading*) 表示 “*层叠的*”，意为多个选择符之间具有特定的**优先级**。这一点非常重要，因为复杂网站可能会有非常多的 CSS 规则，因此必须规定好这些规则的优先级，以免乱套。

## 更多

- [CSS - 维基百科](https://en.wikipedia.org/wiki/CSS)
