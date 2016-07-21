## 元素可视化格式

### [元素的定位方案(Positioning schemes)](https://www.w3.org/TR/CSS21/visuren.html#positioning-scheme)

在CSS2.1中，元素盒子可以有三种*定位方案*:

1. [Normal flow](https://www.w3.org/TR/CSS21/visuren.html#normal-flow).In CSS 2.1, normal flow includes [block formatting](https://www.w3.org/TR/CSS21/visuren.html#block-formatting) of block-level boxes, [inline formatting](https://www.w3.org/TR/CSS21/visuren.html#inline-formatting) of inline-level boxes, and [relative positioning](https://www.w3.org/TR/CSS21/visuren.html#relative-positioning) of block-level and inline-level boxes.
2. [Floats](https://www.w3.org/TR/CSS21/visuren.html#floats).In the float model, a box is first laid out according to the normal flow, then taken out of the flow and shifted to the left or right as far as possible. Content may flow along the side of a float
3. [Absoulte positioning](https://www.w3.org/TR/CSS21/visuren.html#absolute-positioning). In the absolute positioning model, a box is removed from the normal flow entirely (it has no impact on later siblings) and assigned a position with respect to a containing block


### `position` 取值和描述

用一个表格来描述css中定位属性`position`的值和意义:

| 取值         | 哪种定位方案            | 描述                                       |
| ---------- | ----------------- | ---------------------------------------- |
| "static"   | 1                 | 默认值。元素出现在正常文档流中(忽略 `top`,` bottom`, `left`,` right` 或者 `z-index` 设置) |
| "inherit"  | 根据父元素确定；1/2/3中的一种 | 规定该元素从父元素继承 `position` 属性                |
| "relative" | 1                 | 生成相对定位的元素; 未脱离文档流; 相对于其正常位置进行定位。比如:`left:20` 会让元素向右偏移 20px. 可以使用`top`,` bottom`, `left`,` right` 或者 `z-index`这些属性 |
| "absolute" | 3                 | 生成绝对定位的元素; 完全脱离文档流; 相对于除`static`元素以外的离它最近的父元素进行定位。元素位置通过`top`,` bottom`, `left`,` right`  `z-index` 设置。注意: 如果没有显示指定的非 `static` 父级元素，在会相对文档根元素进行定位，通常是 `document` |
| "fixed"    | 3                 | 生成绝对定位的元素; 完全脱离文档流;相对于浏览器窗口进行定位。元素位置通过`top`,` bottom`, `left`,` right`  `z-index` 设置 |



### [Float](https://www.w3.org/TR/CSS2/visuren.html#floats)

In the float model, a box is first laid out according to the normal flow, then 
**taken out of the flow** and shifted to the left or right as far as possible.

应用`float`的元素会在当前行上向左或向右浮动。`float`最有趣的特性是，该元素后面的内从会沿着它的边流动(可以通过使用`clear`属性来清除浮动带来的这个(副)作用)。元素向左浮动，内容则会沿着右边向右向下浮动，元素向右浮动，内容则会沿着左边向右向下浮动。

浮动盒子会尽可能地向右或向左移动，直到它的外边沿碰触到包裹块的边界或者其它浮动盒子包裹块的边界。如果这里有一个线框，那么浮动盒子最外部的顶部将会和线框盒子的顶部对齐。

如果没有足够的水平空间用于浮动元素，它将会向下移动，直到没有浮动呈现或者浮动盒子找到合适的位置。

> `position:absplute`与`float:left/right`是近亲，出自[position:absolute与float:left是近亲](http://www.zhangxinxu.com/wordpress/2010/12/css-%E7%9B%B8%E5%AF%B9%E7%BB%9D%E5%AF%B9%E5%AE%9A%E4%BD%8D%E7%B3%BB%E5%88%97%EF%BC%88%E4%B8%80%EF%BC%89/)
>
> [absolute的inline-block 化 demo](http://www.zhangxinxu.com/study/201012/position-absolute-inline-block.html)
>
> [absolute 绝对定位的破坏性实例页面](http://www.zhangxinxu.com/study/201012/position-absolute-destroy.html)
>
> [浮动与文档流](http://kabike.iteye.com/blog/1741831)

### [clear](https://www.w3.org/TR/CSS21/visuren.html#propdef-clear)

该属性表明了元素盒子的哪一边不能与之前的浮动元素相邻。



### [display](https://www.w3.org/TR/CSS21/visuren.html#propdef-display)



### `display`,`position` 和 `float` 之间的关系

这三个影响到元素盒子生成和布局的属性，相互之间的制约关系如下:

1. 如果 `display`的值是`none`,`position`和 `float` 属性无法应用。此时，元素不会生成盒子模型。
2. 否则，如果 `position` 的值是 `absolute` 或 `fixed`, 元素盒子则处于绝对定位状态。`float`的计算值将是`none`,`display`的值将会根据下表给出。元素盒子的位置将由`top`,`bottom`,`left`,`right`四个属性和该元素所在的元素盒子(containing box)确定。
3. 否则，如果`float`的值是非`none`,元素盒子将会浮动，`display`的值根据下表确定。
4. 否则，如果该元素是根元素，`display`根据下表确定，
5. 否则，`display`其他的属性则会被指明。

| 指定的值(Specified value)                    | 计算出的值(Computed value) |
| ---------------------------------------- | --------------------- |
| inline-table                             | table                 |
| inline, table-row-group, table-column, table-column-group, table-header-group, table-footer-group, table-row, table-cell, table-caption, inline-block | block                 |
| others                                   | same as specified     |



[了解更多:Visual formatting model](https://www.w3.org/TR/CSS21/visuren.html#absolute-positioning)