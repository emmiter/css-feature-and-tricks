[CSS3-2D-Transforms](http://www.w3schools.com/css/css3_2dtransforms.asp)

## Transform 一般都要和animation和transition一起使用。

CSS3 transform 允许开发者平移(`translate`),缩放(`scale`)以及扭曲(`skew`)元素。**变形(transformation)**指的是改变元素形状(shape),尺寸(size)以及位置(position)的效果。

CSS3支持2D和3D变换。

![CSS中的坐标系，2D和3D](http://sunny90.com/uploads/allimg/150122/1-150122230941952.jpg)

## 2D变形的内容如下

* `translate()`

​        “平移方法”从当前位置移动该元素到指定的位置(就是translate(x,y))x和y的位置 [例子](http://www.w3schools.com/css/tryit.asp?filename=trycss3_transform_translate)

* `rotate()`

  根据给定的角度，顺时针或逆时针旋转元素 [例子](http://www.w3schools.com/css/tryit.asp?filename=trycss3_transform_rotate)。正值代表顺时针，负值代表逆时针

* `scale()`

  增加或减小元素的尺寸(根据宽和高被给定的参数)。scale比较常见的是用在鼠标hover到图片上进行放大。配合`transition`一起使用。

* `skewX()`

  沿着`X`轴，按照给定的弧度扭曲元素。[例子](http://www.w3schools.com/css/tryit.asp?filename=trycss3_transform_skewx)

* `skewY()`

  沿着`Y`轴，按照给定的弧度扭曲元素。[例子](http://www.w3schools.com/css/tryit.asp?filename=trycss3_transform_skewy)

* skew()

  按照给定的弧度，同时沿着`X`轴和`Y`轴扭曲元素。[例子](http://www.w3schools.com/css/tryit.asp?filename=trycss3_transform_skew)

  如果只有一个参数的话，会被当作是绕X轴旋转。

* `matrix()`

  把所有2D变换结合成一个。接收6个参数，包含数学函数，允许你旋转，缩放，平移和扭曲。

  `matrix(scaleX(),skewY(),skewX(),scaleY(),translateX(),translateY());`

  * 沿X轴缩放值
  * 绕Y轴扭曲值
  * 绕X轴扭曲值
  * 沿Y轴缩放值
  * 沿X轴平移值
  * 沿Y轴平移值

  ​

注意，上面的变形都是静态的，就是你一打开页面它就处于变形后的那个状态了。可以配合`animation`和`transition`一起使用，让元素动起来。

