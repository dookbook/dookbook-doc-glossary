TOPIC: Web Accessibility
       Accessibility Object Model

# 无障碍网页

**无障碍网页**（**Web Accessibility** ，缩写：**A11Y**）指在物理条件和技术条件限制下，保证网站达到*最佳可用性的实践*。
Web accessibility的正式定义与论述，在[[W3C]]上的[网页无障碍倡议 (Web Accessibility Initiative, WAI)](/zh-hans/glossary/WAI)。

## 可访问性对象模型 (AOM)

**可访问性树**或**可访问性对象模型（AOM）**，包含大多数HTML元素与*可访问性相关*的信息。

浏览器将标记转换为内部表示形式，称为*DOM树*。 DOM树包含所有标记元素，属性和文本节点的对象。然后，浏览器基于DOM树创建一个可访问性树，平台专用的*可访问性API*将其用于辅助技术（例如屏幕阅读器）。

可访问性树对象中包含四件事：

名称
:   如何引用它？ 例如，带有文本“更多”的链接将具有“更多”作为其名称（有关如何在[可访问名称和描述计算规范](https://www.w3.org/TR/accname-1.1/)）。

描述
:   如果要在名称中添加任何内容，我们如何描述该元素？表的描述可以解释该表提供的信息类型。

角色
:   它是什么类型的东西？例如，它是按钮，导航栏还是项目列表？

状态
:   它有状态吗？可以将复选框选中或未选中，或者将`<summary>`元素折叠或展开。

此外，可访问性树通常包含有关元素可以完成的操作的信息：可以跟随链接，可以将文本输入键入等。

## 了解更多

- [Accessibility - MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility)
- [Web Accessibility - 维基百科](https://en.wikipedia.org/wiki/Web%20accessibility)
- [Web Accessibility (ARIA) - MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)
- [Web Accessibility Initiative官网](http://www.w3.org/WAI/)
- [WAI-ARIA推荐规范](http://www.w3.org/TR/wai-aria/)
