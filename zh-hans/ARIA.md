TOPIC: Accessible Rich Internet Applications

# Accessible Rich Internet Applications (ARIA)

**ARIA** (**Accessible Rich Internet Applications**)是向HTML中添加语义和其他元数据的*[[W3C]]规范*，以满足用户的辅助技术的需要。

例如，你可以将 `role="alert"`添加到`<p>`标签以通知视力有问题的用户该信息是重要的（否则你可能通过文字颜色传达）。

Accessible Rich Internet Applications (ARIA) 是能够让*残障人士*更加便利的访问Web内容和使用Web应用（特别是那些由[[JavaScript]]开发的）的一套机制。

ARIA是对HTML的补充，以便在没有其他机制的情况下，使得应用程序中常用的交互和小部件可以传递给辅助交互技术。例如，ARIA支持HTML4中的可访问导航地标、JavaScript小部件、表单提示和错误消息、实时内容更新等。

!!! warn "注意"
    这些小部件中的许多后来被合并到HTML5中，**开发人员应该更倾向使用对应的语义化HTML元素，而不是使用ARIA**。例如，原生元素具有内置的键盘可访问性、角色和状态。但是如果您选择使用ARIA，您就得负责在脚本中模仿(等效的)浏览器行为。

这是进度条小部件的举例：

```html
<div id="percent-loaded" role="progressbar" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100">
```

由于这个滚动条是用`<div>`写的，没有语义。然而对开发者来说，
在HTML4中又没有更多的语义化的标签，所以我们需要引入ARIA的角色和属性。
它们是通过向元素添加属性来指定的。这个例子中，`role="progressbar"`这个属性告诉浏览器，该元素其实是一个JavaScript实现的进度条组件。`aria-valuemin`和
`aria-valuemax`属性表明了进度条的最小值和最大值，而`aria-valuenow`则描述了当前进度条的状态，因此它得用JavaScript来更新：

```javascript
function updateProgress(percentComplete) {
  progressBar.setAttribute("aria-valuenow", percentComplete);
}
```

!!! info "Note"
    在HTML5中，所有的ARIA属性都是有效的。新的标记元素（`<main>`, `<header>`, `<nav>`等）都已具有了ARIA角色，所以就没必要再标注说明了。
