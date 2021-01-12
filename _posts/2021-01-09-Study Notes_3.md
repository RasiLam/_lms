---
layout: page
title: 关于媒体查询，你必须知道的几件事！
excerpt_separator: <!--more-->
categories:
     - 学习笔记
---

# 篇三
## title: 关于媒体查询，你必须知道的几件事！
> 媒体查询是可以让我们在某些条件下为网页应用样式，是网页设计中非常重要的一环。

<!--more-->

### 什么是媒体查询？
> 这是一条媒体查询的例子：http://www.infinistudio.cn/， 帮助你对媒体查询有一个初步的了解。
![](/assets/媒体查询1.jpg)

---
基本的条件逻辑：if/else语句

1.if语句：If满足……条件，则……

2.else语句：else 如果不满足…..条件，则……

---

### 媒体查询的语法
* @media +设备 +（条件）{执行的代码}


```
注意：设备默认为screen（屏幕），因此在大多数情况下，“设备”可以省略，则为：
* @media  +（条件） {执行的代码}
```

### 媒体查询的常用前缀
![](/assets/媒体查询2.jpg)

### 媒体查询可以测试哪些特性
---
Width：视口宽度

Height: 视口高度

Device-width：渲染表面的宽度（设备屏幕宽度）

Device-height:渲染表面的高度（设备屏幕宽高度）

Orientation：设备方向是水平还是垂直

Aspect-ratio：视口的宽高比。aspect-ratio：16/9

Color：颜色组分的位深。

Color-index: 设备颜色查找表中的条目数。

Resolution: 屏幕或打印分辨率。

Scan：针对电视的逐行扫描和各行扫描。

Grid：设备基于栅格还是位图。

---
```
媒体查询用的最多的特性是视口宽度（width），很少需要用到其他特性（偶尔会用到分辨率和视口高度）。
```
