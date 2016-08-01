## [CSS3 Animations](http://www.w3schools.com/css/css3_animations.asp)

CSS3 `animation` 属性能使开发者不适用Javascript 和 Flash 动画大部分属性。

CSS3 Animations 是什么？

* 动画可以让元素逐渐地从一个样式变成另一个样式
* 想改变多少属性改变多少属性，想改变多少次就改变多少次
* 要使用CSS3动画，必须先为动画指定一些`keyframes`。
* `keyframes`保存了特定时间点时元素应该是什么样式

`@keyframes` 规则

当你在`@keyframe`规则中指定CSS样式时，动画将会在特定的时间慢慢地从当前样式改变到新的样式

当然了，要让动画工作的话，你还必须得把动画绑定到要动画的元素上。

```css
/* The animation code */
@keyframes example {
    from {background-color: red;}
    to {background-color: yellow;}
}

/* The element to apply the animation to */
div {
    width: 100px;
    height: 100px;
    background-color: red;
    animation-name: example;
    animation-duration: 4s;
}
```

和`transition`一样，如果没有指定`transition/animation - duration`值的话，就不会有动画效果了。

`keywords`:

* `from` 代表 `0%`
* `to` 代表 `100%`
* 也可以用**百分比**，用百分比的话，你可以添加任意多的样式改变

```css
/* The animation code */
@keyframes example {
    0%   {background-color: red;}
    25%  {background-color: yellow;}
    50%  {background-color: blue;}
    100% {background-color: green;}
}

/* The element to apply the animation to */
div {
    width: 100px;
    height: 100px;
    background-color: red;
    animation-name: example;
    animation-duration: 4s;
}
```

动画多个属性:

```css
/* The animation code */
@keyframes example {
    0%   {background-color: red; left:0px; top:0px;}
    25%  {background-color: yellow; left:200px; top:0px;}
    50%  {background-color: blue; left:200px; top:200px;}
    75%  {background-color: green; left:0px; top:200px;}
    100% {background-color: red; left:0px; top:0px;}
}

/* The element to apply the animation to */
div {
    width: 100px;
    height: 100px;
    position: relative;
    background-color: red;
    animation-name: example;
    animation-duration: 4s;
}
```

延缓动画

`animation-delay`为动画指定了一个延时

```css
div {
    width: 100px;
    height: 100px;
    position: relative;
    background-color: red;
    animation-name: example;
    animation-duration: 4s;
    animation-delay: 2s;
}
```

上面例子在动画开始前，有2s的延时

`animation-iteration-count`属性指定动画的运行次数

```css
div {
    width: 100px;
    height: 100px;
    position: relative;
    background-color: red;
    animation-name: example;
    animation-duration: 4s;
    animation-iteration-count: 3;
}
```

`animation-direction`属性可以指定动画以反方向或者交替形式运行

`animation-timing-function`指定动画的运行速度

* ease
* linear
* ease-in
* ease-out
* ease-in-out
* cubic-bezier(n,n,n,n)

动画的简写记法:

```css
div {
  animation:example 5s linear 2s infinite alternate;
}
```

[定制自己的cubic-bezier](http://cubic-bezier.com/#.17,.67,.83,.67)

