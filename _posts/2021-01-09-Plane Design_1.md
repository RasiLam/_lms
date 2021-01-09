---
layout: page
title: web隐藏术？你看到的可能只是网页的一部分
excerpt_separator: "<!--more-->"
categories:
     - 平面设计
---

# 篇一
## title: web隐藏术？你看到的可能只是网页的一部分
#### 在web网站的构建中，往往有些元素是需要被隐藏起来。今天我们就来进行一个小小web隐藏术的修行！
<!--more-->
让一个元素隐藏起来的实现方案会有很多种，比如利用图片替换文本CSS方法，用图片替代文本的方案都适合于元素的隐藏
只不过每种不同的技术方案实现的原理和最终呈现给用户的渲染方式会有所不同。
而且每种隐藏的方式在不同的媒体设备上看到的都不一样。


### [display 属性](http://www.w3school.com.cn/cssref/pr_class_display.asp)

#### 定义和用法
display 属性规定元素应该生成的框的类型。
说明:这个属性用于定义建立布局时元素生成的显示框类型。对于 HTML 等文档类型，如果使用 display 不谨慎会很危险，因为可能违反 HTML 中已经定义的显示层次结构。对于 XML，由于 XML 没有内置的这种层次结构，所有 display 是绝对必要的。
![通过none值进行隐藏](/assets/images/Plane Design/2019-6-20-ycs_0.jpg)
在CSS的世界中，HTML中的任何一个元素都是一个`矩形框`，即`盒模型`。可以通过display的值来改变盒模型在Web页面中的渲染模式。
使用display设置为none值时可以隐藏元素，不会产生这个盒模型。

### 移除掉首页一个重复的h1标题
![jpg](/assets/images/Plane Design/2019-6-20-ycs_1.png)
在文字class选择器里面未进行none值的设置，可以发现文字会正常显示，我们需要通过设置none值去隐藏文字
![jpg](/assets/images/Plane Design/2019-6-20-ycs_2.png)
当我们对none值进行设定的时候，神奇的隐藏术就开始了！h1标签被成功隐藏！

### 如何在Jekyll中移除h1标签，实践隐藏术！  

![jpg](/assets/images/Plane Design/2019-6-20-ycs_3.png)  

利用jekyll的层级结构，在找到在`_layouts/home.html`页面中的%7b % include page-intro.html % %7d下方添加如下代码：  

```
<style>
.intro-title {
    display: none;
}
</style>
```
再次部署，成功实现h1标题的隐身

