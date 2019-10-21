TOPIC: Grid
AUTHORS: GHLandy; ghlandy@ghlandy.com; github:GHLandy

# Grid

通过设置 `display: grid;`  可以定义一个 CSS 网格。然后使用 `grid-template-rows` 和
`grid-template-columns` 属性来定义网格的 columns 和 rows。

使用这些属性定义的网格被描述为 显式网格 (explicit grid)。

如果你把内容放在这个explicit grid之外 ，或者如果你依赖auto-placement和grid algorithm需要创建额外的row或者column  tracks 去控制
grid items，那么将在 implicit grid 中创建额外的tracks。由于将内容添加到tracks的定义之外，implicit grid会被自动创建。

（注：在容器div上用 row和column定义的网格总数，等于 行数乘以列数 个。比如一个容器div定义了2行*3列=6个网格，这6个就是显式网格，但是假如里面有8个 子div，多出来那2个就叫做隐式网格。下面例子就是这样的。）

在下面的例子中，我创建了一个有三列两行的explicit grid。由于超过explicit tracks可容纳的六个条目，在网格中的第三行是一个implicit grid row track。

```css
.wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 100px 100px;
}
```

```html
<div class="wrapper">
   <div>One</div>
   <div>Two</div>
   <div>Three</div>
   <div>Four</div>
   <div>Five</div>
   <div>Six</div>
   <div>Seven</div>
   <div>Eight</div>
</div>
```

## 了解更多

### 属性参考

- [`grid-template-columns`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-template-columns)
- [`grid-template-rows`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-template-rows)
- [`grid`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid)
- [`grid-template`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-template)

### 扩展阅读

- CSS Grid Layout Guide: [布局的基本概念](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout)
