[Media Query](http://www.w3schools.com/css/css_rwd_mediaqueries.asp)

媒体查询是在CSS3中引入的一项技术。使用`@media`规则来包含一个css规则块，如果满足某个条件的话。

[例子](http://www.w3schools.com/css/tryit.asp?filename=tryresponsive_mediaquery)

[例子](http://www.w3schools.com/css/tryit.asp?filename=tryresponsive_breakpoints)

当屏幕(浏览器窗口)小于768px时，每一列的尺寸都是100%.

```css
/* For desktop: */
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

@media only screen and (max-width: 768px) {
    /* For mobile phones: */
    [class*="col-"] {
        width: 100%;
    }
}
```

### Always Design for Mobile First

这样可以使得在小屏幕页面展示更快。

[例子](http://www.w3schools.com/css/tryit.asp?filename=tryresponsive_mobilefirst)

```css
/* For mobile phones: */
[class*="col-"] {
    width: 100%;
}
@media only screen and (min-width: 768px) {
    /* For desktop: */
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
}
```

### Orientation:Portrait/Landscape

媒体查询也可以被用于根据浏览器的方向来改变页面布局。可以设定一系列CSS属性，当窗口的宽度比高度大时(水平方向)，就应用这些属性。

