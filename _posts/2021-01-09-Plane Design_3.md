---
layout: page
title: 页面设计之灰阶打印，假如回到70年代，网页是怎样的？
excerpt_separator: "<!--more-->"
categories:
     - 平面设计
---

# 篇三
## title: 页面设计之灰阶打印，假如回到70年代，网页是怎样的？
#### 学习了如何用衬线字体和非衬线字体进行可读性的提高，相信大家也明白了标题用非衬线字体与内文用衬线字体在平面设计中的作用接下来让我们来了解一下如何用灰阶打印，让整个网页回归70年代黑白照片的质感。
<!--more-->
### 什么是灰阶打印
利用`filter`进行灰阶打印
- `filter`CSS属性将模糊或颜色偏移等图形效果应用于元素。滤镜通常用于调整图像，背景和边框的渲染。
-  CSS标准里包含了一些已实现预定义效果的函数。你也可以参考一个SVG滤镜，通过一个URL链接到SVG滤镜元素(SVG filter element)。
### 使用方法
-  运用了css的滤镜 filter 中的 grayscale
-  利用了内嵌的css,是在html里设置style  
![](/assets/images/Plane Design/2019-6-20-huidu.jpg)  

可以看到我们需要在html标签里面进行style的设置来进行灰度的转化，其中可以对`grayscale`的值进行灰度的设定
经过灰度的设定我们的网除图片外都会尝试灰度的变化

[更多关于filter应用](https://developer.mozilla.org/zh-CN/docs/Web/CSS/filter)
