TOPIC: Cascading Style Sheets

# 层叠样式表 (CSS)

**CSS**（**Cascading Style Sheets**，**层叠样式表**）是用来控制网页在浏览器中的显示外观的*声明式语言*。浏览器会根据 CSS 的样式定义将其选定的元素显示为恰当的形式。
**CSS** 与 **[[HTML]]** 和 **[[JavaScript]]** 并称 *[Web](/zh-hans/glossary/World_Wide_Web) 三大核心技术*。
一般用它来定义 *HTML 元素* 的样式，但它也能用于其他标记语言，如 *[[SVG]]* 和 *[[XML]]*。

## CSS 规则

一条 CSS **规则**包含一个**选择器** (**selector**)和一组**声明**(**declaration**)定义。
一条 CSS 的**样式声明** (**style declaration**)包括**属性** (**property**)和**属性值**  (**value**)。

![CSS Rule](/media/glossary__css-rule.png)

注意语法特征：

- 每一条CSS规则（不包括选择器）都必须包含在**大括号** (**`{}`**)里。
- 每条CSS样式声明里，都必须包含属性和值，它们被**冒号** (**`:`**)分开。
- 每条CSS样式声名总是以**分号** (**`;`**)结束。

CSS 中的 “**C**” (*Cascading*) 表示 “*层叠的*”，意为多个选择符之间具有特定的**优先级**。这一点非常重要，因为复杂网站可能会有非常多的 CSS 规则，因此必须规定好这些规则的优先级，以免乱套。

## CSS 选择器

**CSS选择器** (**selector**) 是CSS规则的一部分，它描述了该规则将匹配文档中的哪些元素。

### CSS 选择器类型

| 选择器 | 匹配的元素 | 示例 |
| :-- | :-- | :-- |
| **类型选择器** (或**元素选择器**、**标签选择器**) | 同类元素或同标签的元素。| `p`选择所有`<p>`元素 |
| **类选择器** | 包含指定`class`的所有元素。| `p.class-name`选择所有`<p class="class-name">`元素 |
| **ID选择器** | 包含指定`id`的元素。| `#id-name`选择`<p id="id-name">`元素。|
| **属性选择器** | 包含指定属性的元素。| `img[src=img.png]` 选择`<img src="img.png">`元素。|
| **伪类选择器** | 包含指定状态的元素。| `a:hover`选择`<a>`元素，当鼠标划过的时候。|
| **伪元素选择器** | 包含指定元素的部分。 | `p::first-line`选择所有`<p>`元素内容的第一行。|

- 基础选择器
    - [Universal selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Universal_selectors)
    `* ns|* *|*`
- Grouping
    - [Grouping selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Grouping_selectors)
  `A, B`
- Combinators
    - [Adjacent sibling selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Adjacent_sibling_selectors)
    `A + B`
    - [General sibling selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/General_sibling_selectors)
    `A ~ B`
    - [Child selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Child_selectors)
    `A > B`
    - [Descendant selectors](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/Descendant_selectors)
    `A B`

### CSS 属性选择器

| 语法 | 描述 | 示例 |
| :-- | :-- | :-- |
| `[attr]` | 表示带`attr`属性的元素。| `a[title]`，选择带`title`属性的`<a>`元素。|
| `[attr=value]` | 表示`attr`属性值完全等于`value`的元素。| `a[href="https://example.org"]`， 选择`href`属性值为`https://example.org`的元素。|
| `[attr~=value]` | 表示`attr`属性值包含`value`的元素。多个属性值以*空格*隔开。| `a[class~="logo"]`， 选择`class`属性值包含`logo`的元素。|
| `[attr|=value]` | 表示`attr`属性值完全等于`value`或以`value-`为前缀。（**`-`**为**连字符**，Unicode 编码为 *`U+002D`*）。典型的应用场景是用来匹配*语言简写代码*（如 `zh-CN`，`zh-TW` 可以用 `zh` 作为 `value`）。| `div[lang|="zh"]`，选择所有内容为中文的`<div>`元素，不管是简体中文 (`zh-CN`)还是繁体中文 (`zh-TW`)。|
| `[attr^=value]` | 表示`attr`属性值以`value`开头。| `a[href^="#"]`，选择`href`属性值以`#`开头的所有`<a>`元素。|
| `[attr$=value]` | 表示`attr`属性值以`value`结尾。| `a[href$=".org"]`，选择`href`属性值以`.org`结尾的所有`<a>`元素。|
| `[attr*=value]` | 表示`attr`属性值的字符串至少包含一次`value`。| `a[href*="example"]`，选择`href`属性值字符串至少包含一次`example`的所有`<a>`元素。|
| `[attr operator value i]` (**Selectors Level 4 新增**) | 在中括号结束符号之前新增一个 **`i`** (或 **`I`**) 表示匹配是**忽略大小写**的。| `a[href*="Example" i]`，新增`href`属性值包含`Example`（忽略大小写）。|
| `[attr operator value s]` (**Selectors Level 4 新增**, **试验性 API**) | 在中括号结束符号之前新增一个 **`s`** (或 **`S`**) 表示匹配是**区分大小写**的。| `a[href*="Example" s]`，新增`href`属性值包含`Example`（区分大小写）。 |

## CSS 属性

**CSS属性** （**property**）是一种特性（如`color`），其关联的值定义了浏览器应如何显示元素的一个方面。

## 更多

- [CSS - 维基百科](https://en.wikipedia.org/wiki/CSS)
- [MDN CSS文档](https://developer.mozilla.org/en-US/docs/Web/CSS "MDN CSS文档")
