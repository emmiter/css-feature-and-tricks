## [CSS Pseudo-classes](http://www.w3schools.com/css/css_pseudo_classes.asp)

**CSS 伪类用于定义元素的特殊状态。**

例如:

1. 当用户鼠标移动到元素上时，为元素添加某些样式
2. 用不同的样式标记超链接是否被用户访问过
3. 元素获得焦点时，为元素加载某些样式

语法:

```css
selector:pseudo-class{
  property:value;
}
```

### 锚点伪类(Anchor Pseudo-classes)

```css
a:link{
  color:#FF0000;
}
/* visited link */
a:visited {
    color: #00FF00;
}

/* mouse over link */
a:hover {
    color: #FF00FF;
}

/* selected link */
a:active {
    color: #0000FF;
}
//注意书写顺序，a:hover卸载a:link 和 a:visited后面，这样比较高效。a:active 必须写在a:hover后面。伪类名字大小写不敏感。
```

