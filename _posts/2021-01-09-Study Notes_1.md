---
layout: page
title: 保姆式svg介绍
excerpt_separator: <!--more-->
categories:
     - 学习笔记
---

# 篇一
## title: 保姆式svg介绍

<!--more-->

### SVG主要优势:
（1）SVG可被众多工具读取和修改（比如记事本）。

（2）SVG与JPEG和GIF图像比起来，尺寸更小，且可压缩性更强。

（3）SVG是可伸缩的。

（4）SVG图像可在任何的分辨率下被高质量地打印。

（5）SVG可在图像质量不下降的情况下被放大。

（6）SVG图像中的文本是可选的，同时也是可搜索的（很适合制作地图）。

（7）SVG可以与Java技术一起运行。

（8）SVG是开放的标准。

（9）SVG文件是纯粹的XML。
### SVG代码
* svg的width属性和height属性，指定了 SVG 图像在 HTML 元素中所占据的宽度和高度。除了相对单位%，也可以采用绝对单位（单位：像素）。

```
如果不指定这两个属性，SVG 图像默认大小是300像素（宽） x 150像素（高）。如果只想展示 SVG 图像的一部分，就要指定viewBox属性。
```

#### Viewbox 视区盒子
* Viewbox就是截屏工具选中的那个框框，最终的呈现就是把框框中的截屏内容再次在显示器中全屏显示
![](/assets/https://github.com/RasiLam/lms_web/blob/lms_/assets/SVG1.png?raw=true)
* 参数：viewBox="x, y, width, height" （x:左上角横坐标，y:左上角纵坐标）
 

### 外联SVG
1.使用img标签：最直接的插入SVG图像的方式就是将图像插入到HTML文档中的方式。

2.使用object标签：可以使用object标签引入外部svg文件到当前页面。

3.把SVG作为背景图像插入：SVG可以在CSS中用作一个背景图像，和其他图片格式(PNG、JPG、GIF)一样。

### 内联SVG
* 在 HTML5 中，能够将 SVG 元素直接嵌入 HTML 页面中
![](/assets/https://github.com/RasiLam/lms_web/blob/lms_/assets/SVG2.png?raw=true)

### SVG动画
![](/assets/https://github.com/RasiLam/lms_web/blob/lms_/assets/SVG3.jpg?raw=true)

以下是获取SVG图标链接：

Font Awesome图库(http://www.fontawesome.com.cn/faicons/)

codepen(https://codepen.io)

Iconfont(https://www.iconfont.cn/)




