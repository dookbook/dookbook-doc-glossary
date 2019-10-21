TOPIC: Gutters
AUTHORS: San; 1962511805@qq.com; github:Pedestrian93
         sub/dance; subdance@github.com; github:subdance

# Gutters

网格间距是网格轨道之间的间距，可以通过 `grid-column-gap`，`grid-row-gap` 或者 `grid-row-gap` 在Grid布局中创建。

在下面的例子中，由一个三列两行的网格。它的列轨道之间有20px的间距，行轨道之间有20px的间距。

```css
.wrapper {
  display: grid;
  grid-template-columns: repeat(3,1.2fr);
  grid-auto-rows: 45%;
  grid-column-gap: 20px;
  grid-row-gap: 20px;
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

在网格大小上，网格间距参与计算就好像规则的网格轨道一样，但是没有任何东西可以被放置到网格间距上。网格间距也像网格线一样在那个位置会增加额外的大小，因此网格项目会被放置在网格间距末的那条网格线后。

能够导致轨道被间隔开来的，除了网格间距属性，还有margins，padding或者使用盒模型对齐中的空间分布属性。这些方法都会导致可见间距的产生，因此网格间距属性不等价于”间距大小“，除非你没有使用这些能够产生间距的方法。

## 了解更多

### 属性参考

- [`grid-column-gap`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-column-gap)
- [`grid-row-gap`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-row-gap)
- [`grid-gap`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-gap)

### 扩展阅读

- CSS Grid Layout Guide: [Basic concepts of grid layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout)
- [Definition of gutters in the CSS Grid Layout specification](https://drafts.csswg.org/css-grid/#gutters)
