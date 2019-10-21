TOPIC: Grid Tracks

# Grid Tracks

**网格轨道** 是两条网格线之间的空间。它们通过使用属性 `grid-template-columns` 和 `grid-template-rows`
或者简写属性 `grid` 和 `grid-template` 在显式网格中定义。网格轨道也可以在隐式网格中创建，通过将一个网格项目定位到显式网格中创建的轨道外面。

下图展示该网格中的第一个行轨道（上色部分的空间）。

![text](https://mdn.mozillademos.org/files/14769/1_Grid_Track.png)

## 显式网格中的轨道大小

当使用 `grid-template-columns` 和 `grid-template-rows` 定义网格轨道时，你可以使用任何长度单位，
也可以使用flex单位 `fr` 来表示网格容器中可用空间的一部分。下面的例子演示了一个三列轨道的网格，第一列200px，第二列1fr，第三列3fr。网格容器中的可用空间减去200px后，剩余空间被分成4份，1份给第二列，3份给第三列。

```css
.wrapper {
  display: grid;
  grid-template-columns: 200px 1fr 3fr;
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

## 隐式网格中的轨道大小

隐式网格中创建的轨道默认为自动大小，但可以通过 `grid-auto-rows` 和 `grid-auto-columns` 属性来定义这些轨道的大小。

## 了解更多

### 属性参考

- [`grid-template-columns`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-template-columns)
- [`grid-template-rows`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-template-rows)
- [`grid-auto-rows`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-auto-rows)
- [`grid-auto-columns`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-auto-columns)

### 扩展阅读

- CSS Grid Layout Guide: [Basic concepts of grid layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout)
- [Definition of Grid Tracks in the CSS Grid Layout specification](https://drafts.csswg.org/css-grid/#grid-track-concept)
