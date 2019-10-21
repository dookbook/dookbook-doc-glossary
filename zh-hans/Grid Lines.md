TOPIC: Grid Lines

# Grid Lines

使用Grid布局在显式网格中定义轨道的同时会创建**网格线**。在下面的例子中，有一个三列两行的网格。它给了我们4条列线和3条行线。

```html
<div class="wrapper">
   <div>One</div>
   <div>Two</div>
   <div>Three</div>
   <div>Four</div>
   <div>Five</div>
</div>
```

```css
.wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 100px 100px;
}
```

网格线可以用它们的编号来寻址。在从左到右的语言比如英语中，列线1将位于网格的左侧，行线1将位于其顶部。线编号遵循文档的写入模式，因此在从右到左的语言中，列线1行将位于网格的右侧。下面的图片展示了该网格的线编号，假设语言是从左到右的。

![text](https://mdn.mozillademos.org/files/14763/1_diagram_numbered_grid_lines.png)

当创建隐式轨道去支持显式网格外的内容时，网格线也会在隐式网格中被创建，但是这些网格线不能通过编号来寻址。

## 按网格线编号将项目放置到网格上

创建一个网格后，可以通过网格线编号将项目放置到该网格上。在下面的例子中，项目定位从列线1到列线3，从行线1到行线3。

```html
<div class="wrapper">
   <div class="item">Item</div>
</div>
```

```css
.wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 100px 100px;
}
.item {
  grid-column-start: 1;
  grid-column-end: 3;
  grid-row-start: 1;
  grid-row-end: 3;
}
```

## 命名网格线

在显式网格中创建的网格线可以被命名，在轨道大小信息之前或之后的方括号中命名。当放置一个项目时，你可以使用这些名称代替编号，如下所示。

```html
<div class="wrapper">
   <div class="item">Item</div>
</div>
```

```css
.wrapper {
  display: grid;
  grid-template-columns: [col1-start] 1fr [col2-start] 1fr [col3-start] 1fr [cols-end];
  grid-template-rows: [row1-start] 100px [row2-start] 100px [rows-end];
}
.item {
  grid-column-start: col1-start;
  grid-column-end: col3-start;
  grid-row-start: row1-start;
  grid-row-end: rows-end;
}
```

## 了解更多

### 属性参考

- [`grid-template-columns`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-template-columns)
- [`grid-template-rows`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-template-rows)
- [`grid-column-start`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-column-start)
- [`grid-column-end`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-column-end)
- [`grid-column`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-column)
- [`grid-row-start`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-row-start)
- [`grid-row-end`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-row-end)
- [`grid-row`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-row)

### 扩展阅读

- CSS Grid Layout Guide: [Basic concepts of grid layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout)
- CSS Grid Layout Guide: [Line-based placement with CSS Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid)
- CSS Grid Layout Guide: [Layout using named grid lines](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines)
- CSS Grid Layout Guide: [CSS Grids, Logical Values and Writing Modes](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/CSS_Grid,_Logical_Values_and_Writing_Modes)
- [Definition of Grid Lines in the CSS Grid Layout specification](https://drafts.csswg.org/css-grid/#grid-line-concept)
