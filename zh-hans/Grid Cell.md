TOPIC: Grid Cell

# Grid Cell

在Grid布局中，**网络单元格**是CSS网格中的最小单元。它是四条网格线之间的空间，概念上非常像表格单元格。

![text](https://mdn.mozillademos.org/files/14767/1_Grid_Cell.png)

如果不使用网格布局提供的方法去放置网格容器的项目，这些项目将通过自动布局算法被放置到每个网格单元格中。将创建额外的行或列轨道以创建足够的单元格来保存所有项目。

在例子中，我们创建了一个三列轨道的网格。五个项目被放置到网格单元格中，它们沿着初始行依次被放置到三个网格单元格中，然后为剩下的两个创建了一个新行。

```css
.wrapper {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  grid-auto-rows: 100px;
}
```

```html
<div class="wrapper">
   <div>One</div>
   <div>Two</div>
   <div>Three</div>
   <div>Four</div>
   <div>Five</div>
</div>
```

## 了解更多

### 属性参考

- [`grid-template-columns`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-template-columns)
- [`grid-template-rows`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-template-rows)
- [`grid-auto-rows`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-auto-rows)
- [`grid-auto-columns`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-auto-columns)

### 扩展阅读

- CSS Grid Layout Guide: [Basic concepts of grid layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout)
- [Definition of Grid Cells in the CSS Grid Layout specification](https://drafts.csswg.org/css-grid/#grid-track-concept)
