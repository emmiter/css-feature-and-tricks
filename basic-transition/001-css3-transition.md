## CSS3 Transitions

参考资料：

1.[w3schools.com/css/css3_transitions](http://www.w3schools.com/css/css3_transitions.asp)

CSS3 transitions 允许将某个属性的值，在给定时间内，平滑地从当前值过渡到新指定的值。
对于鼠标`hover`这种情况，当鼠标移出该元素盒子时，它会逐渐恢复(从改变后所处状态->改变前的状态)初始状态。

### 如何使用 CSS3 Transitions?

要创建一个过渡效果，必须指定两件事情：

1. 指定属性(***可以同时指定若干个可过渡的属性***): 过渡要改变的属性
2. 过渡效果所持续的时间

***注意：必须指定持续时间，若未指定，可以理解为持续时间为0，则不会产生过渡效果***

举一个🌰

```css
div {
  width:100px;
  height:100px;
  background:red;
  -webkit-transition:width 2s;
  transition:width 2s;
}
```

```
div:hover {
  width:300px;
}
```

上面的例子中，当鼠标`hover`到该`div`上后，`width`的值被重新设定成了`300px`。而过渡开始的条件是***当指定的CSS属性(这里是`width`值改变的时候，就会触发过渡效果)***。所以，鼠标`hover`上去后，会看到该`div`的宽度逐渐变宽到`300px`,用时2s。

### 改变多个属性值

```css
div{
  -webkit-transition:width 2s,height 4s;/*Safari*/
  transition:width 2s,height 2s;
}
```

### 指定过渡的速度曲线

`transition-timing-function`属性指定了过渡效果的速度曲线

该属性可以取如下值:

1. `ease` - slow start,then fast,then end slowly(default)
2. `linear` - keep the same speed from start to end
3. `ease-in` - with a slow start
4. `ease-out` - with a slow end
5. `ease-in-out` - with a slow start and end
6. `cubic-bezier(n,n,n,n)` - lets you define your own values in a cubic-bezier function

[6种速度曲线的视觉效果看这里](http://www.w3schools.com/css/tryit.asp?filename=trycss3_transition_speed)

### 延迟过渡效果

`transition-delay`属性可以为过渡效果指定一个延迟时间(以秒为单位)

```css
//指定了1s的过渡开始延迟
div {
  -webkit-transition-delay:1s;/*Safari*/
  transition-delay:1s;
}
```

### 过渡+变换(Transition+Transformation)

The following example also adds a transformation to the transition effect:

[这里查看效果](http://www.w3schools.com/css/tryit.asp?filename=trycss3_transition_transform)

```css
div {
  width:100px;
  height:100px;
  background:red;
  -webkit-transition:width 2s,height 2s,-webkit-transform 2s;/* Safari*/
  transition:width 2s,height 2s,transform 2s;
}

div:hover {
  width:300px;
  height:300px;
  -webkit-transform:rotate(180deg); /* Safari */
  transform:rotate(180deg);
}
```

### CSS3 过渡属性(CSS3 Transition Properties)

下表列出了所有的`transition`属性

| 属性(Property)                 | 描述(Description)                    |
| ---------------------------- | ---------------------------------- |
| `transition`                 | 四个过渡属性的简写。                         |
| `transition-delay`           | 指定过渡效果的延迟时间(in seconds)            |
| `transition-duration`        | 指定过渡效果的持续时间(seconds/milliseconds)  |
| `transition-property`        | 指定过渡属性的名字，如果一次要过渡多个属性的话，属性值之间以逗号分隔 |
| `transition-timing-function` | 指定过渡的速度曲线                          |