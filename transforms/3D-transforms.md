[CSS3 3D Transform](http://www.w3schools.com/css/css3_3dtransforms.asp)

* `rotateX()`
* `rotateY()`
* `rotateZ()`

CSS3 Transform Properties

下表列出了所有的 3D 变换属性

| 属性                  | 描述                                       |
| ------------------- | ---------------------------------------- |
| transform           | 为元素应用2D或3D变换                             |
| transform-origin    | 改变变换元素的位置                                |
| transform-style     | 指定嵌套元素在3D空间如何渲染。`flat`\|`preserve-3d`\|`initial`\|`inherit` `flat`: 子元素将不会保持它的 3D 位置，默认值。 `preserve-3d`:子元素将会保持 3D 位置。 `initial`:降属性设置为初始值。`inherit`:从父元素继承该属性值。[preserve 3D效果](http://www.w3schools.com/cssref/trycss3_transform-style_inuse.htm) |
| perspective         | 指定3D渲染元素的视角                              |
| perspective-origin  | 指定3D元素的底部位置                              |
| backface-visibility | 当元素不正对着屏幕时，指定元素是否可见                      |

3D Transform Methods

| Function                                 | Description       |
| ---------------------------------------- | ----------------- |
| matrix3d(n,n,n,n,n,n,n,n,n,n,n,n,n,n,n,n) | 定义一个3D变换，使用4*4的矩阵 |
| translate3d(x,y,z)                       | 定义3D平移            |
| translateX(x)                            |                   |
| translateY(y)                            |                   |
| translateZ(z)                            |                   |
| scale3d(x,y,z)                           | 定义3d缩放            |
| scaleX(x)                                |                   |
| scaleY(y)                                |                   |
| scaleZ(z)                                |                   |
| rotate3d(x,y,z,angle)                    | 定义3D旋转            |
| rotateX(angle)                           |                   |
| rotateY(angle)                           |                   |
| rotateZ(angle)                           |                   |
| perspective(n)                           | 定义3D变换的视角         |