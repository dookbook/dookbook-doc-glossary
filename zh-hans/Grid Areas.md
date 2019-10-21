TOPIC: Grid Areas

# Grid Areas

**网格区域**是网格中由一个或者多个网格单元格组成的一个矩形区域。当你使用基于网格线位置放置一个项目或者使用命名的网格区域定义区域时，网格区域被创建。

本质上，网格区域一定是矩形的。例如，不可能创建T形或L形的网格区域。

在下面的例子中，有一个网格容器包含两个网格项目，我用 `grid-area` 属性命名它们，然后用 `grid-template-areas` 把它们放在网格上。这将创建两个网格区域，一个覆盖四个网格单元格，另外一个覆盖两个。

```css
.wrapper {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  grid-template-rows: 100px 100px;
  grid-template-areas:
    "a a b"
    "a a b";
}
.item1 {
  grid-area: a;
}
.item2 {
  grid-area: b;
}
```

```html
<div class="wrapper">
   <div class="item1">Item</div>
   <div class="item2">Item</div>
</div>
```

## 了解更多

### 属性参考

- [`grid-template-columns`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-template-columns)
- [`grid-template-rows`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-template-rows)
- [`grid-auto-rows`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-auto-rows)
- [`grid-auto-columns`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-auto-columns)
- [`grid-template-areas`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-template-areas)
- [`grid-area`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-area)

### 扩展阅读

- CSS Grid Layout Guide: [Basic concepts of grid layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout)
- CSS Grid Layout Guide: [Grid template areas](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Grid_Template_Areas)
- [Definition of Grid Areas in the CSS Grid Layout specification](https://drafts.csswg.org/css-grid/#grid-area-concept)
