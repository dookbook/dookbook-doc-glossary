TOPIC: Flex
AUTHORS: Sanday; Sandaydi@github.com; github:Sandaydi
         ZCDC_Ren; renzw@zzes1314.cn; github:klren0312

# 伸缩性

`flex` 是一个CSS的`display` 属性中新添加一个值。 随着`inline-flex`的使用，它将使它适用的元素成为一个flex container（伸缩容器），
而这个元素的每个子元素将成为 flex item（伸缩项目）。伸缩项目将参与到flex布局中，所有由CSS Flexible Box Layout Module（CSS伸缩盒布局模型）定义的属性都能被它们使用。

`flex` 属性是`flex-grow`, `flex-shrink` 和 `flex-basis` 属性的简写。

此外， `<flex>` 可以作为弹性长度被引用在CSS Grid（栅格）布局中。

## 了解更多

### 属性参考

- [align-content](https://developer.mozilla.org/zh-CN/docs/Web/CSS/align-content) 堆栈伸缩行
- [align-items](https://developer.mozilla.org/zh-CN/docs/Web/CSS/align-items) 侧轴上项目对齐方式
- [align-self](https://developer.mozilla.org/zh-CN/docs/Web/CSS/align-self) 侧轴上单个项目对齐方式
- [flex](https://developer.mozilla.org/zh-CN/docs/Web/CSS/flex) 伸缩性
- [flex-basis](https://developer.mozilla.org/zh-CN/docs/Web/CSS/flex-basis) 伸缩-基准值
- [flex-direction](https://developer.mozilla.org/zh-CN/docs/Web/CSS/flex-direction) 伸缩流方向
- [flex-flow](https://developer.mozilla.org/zh-CN/docs/Web/CSS/flex-flow)伸缩流的方向与换行
- [flex-grow](https://developer.mozilla.org/zh-CN/docs/Web/CSS/flex-grow)伸缩-扩展基数
- [flex-shrink](https://developer.mozilla.org/zh-CN/docs/Web/CSS/flex-shrink) 伸缩-收缩比率
- [flex-wrap](https://developer.mozilla.org/zh-CN/docs/Web/CSS/flex-wrap) 伸缩-换行
- [justify-content](https://developer.mozilla.org/zh-CN/docs/Web/CSS/justify-content) 主轴对齐
- [order](https://developer.mozilla.org/zh-CN/docs/Web/CSS/order) 伸缩-顺序

### 延伸阅读

- [CSS Flexible Box Layout Module Level 1 Specification](https://www.w3.org/TR/css-flexbox-1/)（CSS 盒布局模型一级规范）
- CSS Flexbox Guide（CSS 伸缩盒子指南）: [Basic Concepts of Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)（伸缩）
- CSS Flexbox Guide（CSS 伸缩盒子指南）: [Relationship of flexbox to other layout methods](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Relationship_of_Flexbox_to_Other_Layout_Methods)（伸缩盒子与其他布局方法的关系）
- CSS Flexbox Guide（CSS 伸缩盒子指南）: [Aligning items in a flex container](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Aligning_Items_in_a_Flex_Container)（伸缩容器中项的对齐）
- CSS Flexbox Guide（CSS 伸缩盒子指南）: [Ordering flex items](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Ordering_Flex_Items)（伸缩项的顺序）
- CSS Flexbox Guide（CSS 伸缩盒子指南）: [Controlling Ratios of flex items along the main axis](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Controlling_Ratios_of_Flex_Items_Along_the_Main_Ax)（控制主轴上伸缩项的比率）
- CSS Flexbox Guide（CSS 伸缩盒子指南）: [Mastering wrapping of flex items](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Mastering_Wrapping_of_Flex_Items)（掌握如何包装伸缩项）
- CSS Flexbox Guide（CSS 伸缩盒子指南）: [Typical use cases of flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Typical_Use_Cases_of_Flexbox)（伸缩盒子的典型用例）
