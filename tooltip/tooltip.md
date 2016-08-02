[CSS tooltips](http://www.w3schools.com/css/css_tooltip.asp)

tooltips 经常被用于指定额外的信息，当用户把鼠标悬停在元素上时。

[basic tooltips](http://www.w3schools.com/css/tryit.asp?filename=trycss_tooltip)

[tooltip Arrows](http://www.w3schools.com/css/tryit.asp?filename=trycss_tooltip_arrow_bottom)

```css
.tooltip .tooltiptext::after {
    content: " ";
    position: absolute;
    top: 100%; /* At the bottom of the tooltip */
    left: 50%;
    margin-left: -5px;
    border-width: 5px;
    border-style: solid;
    border-color: black transparent transparent transparent;
}
```

