[CSS 单位](http://www.w3schools.com/cssref/css_units.asp)

1. em
2. ex
3. %
4. px
5. cm
6. mm
7. in
8. pt
9. pc
10. ch
11. rem
12. vh
13. vw
14. vmin
15. vmax

相对长度

| 单位   | 描述                                       |
| ---- | ---------------------------------------- |
| em   | 相对于元素字体(2em 就是当前字体的2倍) [try it](http://www.w3schools.com/cssref/tryit.asp?filename=trycss_unit_em) |
| ex   | 相对于当前字体的`x-height`(极少使用) [try it](http://www.w3schools.com/cssref/tryit.asp?filename=trycss_unit_ex) |
| ch   | 相对于"0"的宽度                                |
| rem  | 相对于根元素的字体大小                              |
| vw   | Relative to 1% of the width of the viewport* [try it](http://www.w3schools.com/cssref/tryit.asp?filename=trycss_unit_vw) |
| vh   | Relative to 1% of the height of the viewport* [try it](http://www.w3schools.com/cssref/tryit.asp?filename=trycss_unit_vh) |
| vmin | Relative to 1% of viewport's* smaller dimension [try it](http://www.w3schools.com/cssref/tryit.asp?filename=trycss_unit_vmin) |
| vmax | Relative to 1% of viewport's* larger dimension [try it](http://www.w3schools.com/cssref/tryit.asp?filename=trycss_unit_vmax) |
| %    |                                          |

绝对长度

| 单位   | 描述                         |
| ---- | -------------------------- |
| cm   | 厘米                         |
| mm   | 毫米                         |
| in   | 1in = 96px = 2.54cm        |
| px * | 像素(1px = 1/ 96th of 1in)   |
| pt   | points (1pt = 1/72 of 1in) |
| pc   | 1pc = 12pt                 |

px是相对于可视设备的。对于 low-dpi 的设备，1px 就是1个显示设备像素(dot)。对于打印机和高分辨率屏幕，1px则意味着多个设备像素。

* Pixels (px) are relative to the viewing device. For low-dpi devices, 1px is one device pixel (dot) of the display. For printers and high resolution screens 1px implies multiple device pixels.

常识性知识点:

1. 浏览器默认字号是 16px
2. 为了方便计算，时常将在`<html>元素中设置  `font-size 值为 62.5%. 相当于在`<html>`中设置`font-size`为10px

参考文章:

1. [rem 与 px 的转换](http://caibaojian.com/rem-and-px.html)
2. [rem 自适应布局 - 移动端自适应必备](http://caibaojian.com/flexible-js.html)

