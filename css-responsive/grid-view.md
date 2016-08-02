[Grid View](http://www.w3schools.com/css/css_rwd_grid.asp)

有很多基于网格的页面，也就意味着页面被分为了很多个列:12列。

在响应式设计时，使用`grid-view`是非常有用的。这让在页面上放置元素变得更加容易。

一个响应式网格视图一般会包含12列，这12列的总宽度是100%，当你缩放浏览器窗口的时候，它也会进行相应的缩小或扩张。

响应式网格:

![响应式网格](http://www.w3schools.com/css/tryresponsive_grid.htm)

### 构建响应式网格视图

*首先确保所有的HTML 元素的`box-sizing`属性值被设置为`border-box`*.This makes sure that the padding and border are included in the total width and height of the elements.

```css
* {
    box-sizing: border-box;
}
```

1. [一个使用百分比布局的简单的响应式设计的例子](http://www.w3schools.com/css/tryit.asp?filename=tryresponsive_webpage)

   如果网页仅包含两列的话，上面这个例子是OK的。但是我们想使用12列的网格布局来更好地控制网页。那么第一步就要先算出每一列的宽度: 100% / 12 = 8.33%. 然后给每一列一个类，`class="col-"`，和一个代表该列应该有几个单位的跨度。

   ```css
   .col-1 {width: 8.33%;}
   .col-2 {width: 16.66%;}
   .col-3 {width: 25%;}
   .col-4 {width: 33.33%;}
   .col-5 {width: 41.66%;}
   .col-6 {width: 50%;}
   .col-7 {width: 58.33%;}
   .col-8 {width: 66.66%;}
   .col-9 {width: 75%;}
   .col-10 {width: 83.33%;}
   .col-11 {width: 91.66%;}
   .col-12 {width: 100%;}
   ```

   每一行都要被一个`<div>`包裹。一行中的列数加起来总是12.