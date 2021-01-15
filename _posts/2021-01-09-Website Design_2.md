---
layout: page
title: 网页设计那些小事儿
excerpt_separator: <!--more-->
categories:
     - 网页设计
---

# 篇二
## title: 网页设计那些小事儿
### CSS
- 1.CSS的定义

CSS通常称为CSS样式表或层叠样式表（级联样式表），主要用于设置HTML页面中的文本内容（字体、大小、对齐方式等）、图片的外形（宽高、边框样式、边距等）以及版面的布局等外观显示样式。
CSS以HTML为基础，提供了丰富的功能，如字体、颜色、背景的控制及整体排版等，而且还可以针对不同的浏览器设置不同的样式。

- 2.CSS语法
CSS基础语法
CSS规则由两个主要部分构成：选择器以及一条或多条声明。
每条声明由一个属性和一个值组成。属性(property)是设置的样式属性，每个属性有一个值，属性和值被冒号分开。

比如 selector{property：value}
选择器通常是需要改变样式的HTML元素。

比如 h1{color:red; font-size:14px;}  
h1是选择器，color和font-size是属性，red和14px是值。
注意：

如果定义不止一个声明则需要用分号将每个声明分开。例如：p{text-align:center;color:red}
如果值为若干单词，则要给值加引号： 例如：p {font-family: "sans serif";}


- 3.创建CSS
CSS 创建样式表分为三种情况：
内部样式表



样式优先级：内联样式>内部样式>外部样式
三种样式表区别：

行内样式表 ：优点 书写方便；缺点 没有实现样式和结构相分离；使用情况 较少；控制范围 控制一个标签(少)。

内部样式表：优点 部分结构和样式相分离； 缺点 没有彻底分；使用情况 较多；控制范围 控制一个页面(中)。

外部样式表：优点 完全实现结构和样式相分离； 缺点 需要引入；使用情况 最多，推荐；控制范围 控制整个站点(多)。
- 4.透明度（transparent）

（1）、css中的定义：设置背景为透明
background:transparent
实际上background默认的颜色就是透明的属性，其使用场景：

当一个元素覆盖在另外一个元素之上，而你想显示下面的元素，这时你就需要把上面这个元素的background设置为transparent

（2）、transparent属性在不同css版本下的使用：
在css1中，transparent被用来作为background-color的一个参数值，用于表示背景透明。
在css2中，border-color也开始接受transparent作为参数值，《Open eBook(tm) Publication Structure 1.0.1》[OEB101]延伸到color也接受transparent作为参数值。
在css3中，transparent被延伸到任何一个有color值的属性上。
浏览器兼容
image
border-color和color属性不支持transparent


- #### Opacity
说明：css中设置元素的不透明级别
设置值：

0-1：规定不透明度。从 0.0 （完全透明）到 1.0（完全不透明）。
inherit：应该从父元素继承 opacity 属性的值。
3、opacity、transparent以及rgba的区别
opacity是作为一个完整属性出现的。transparent和rgba都是作为属性值出现的。
opacity是对于整个元素起作用的。而transparent和alpha是对元素的某个属性起作用的。任何需要设置颜色的地方都可以根据情况使用transparent或rgba。比如背景、边框、字体等等。
由于opacity和alpha设置的透明程度可调，就引出一个继承的问题。如果一个元素未设置opacity属性，那么它会从它的父元素继承opacity属性的值。而alpha不存在继承


-  5.CSS选择器种类
id选择器

根据提供的唯一id号快速获取标签对象

用于充当label标签for属性的值：用户名：，表示单击此label标签时，id为userid的标签获得焦点

类选择器 (class )

标签选择器 (h1)

相邻选择器

直接相邻元素选择器 (h1+p)

普通相邻元素选择器 （h2 ~ h2）

子选择器(ul>li)

后代选择器(li a)

通配符选择器(*)

属性选择器（a[rel = "XXX"]）

伪类选择器( :hover :first-child ···)

伪元素选择器( :before :after ···)

分组选择器 👉
CSS选择器优先级

优先级由高到低:!important > 内联style > ID选择器 > 类选择器 > 标签选择器 > 通配符选择器>继承

优先级算法(权重)

元素标签（派生选择器）：1



-  6.CSS元素选择器
最常见的CSS选择器就是元素选择器，也就是标签选择器，也就是在HTML中元素的最基本的选择器。

语法：
标签名{属性1:属性值1; 属性2:属性值2; 属性3:属性值3; }  或者
元素名{属性1:属性值1; 属性2:属性值2; 属性3:属性值3; }

> 标签选择器最大的优点是能快速为页面中同类型的标签统一样式，同时这也是他的缺点，不能设计差异化样式。

- 7.CSS背景(background)
background 属性用于定义 HTML 元素的背景。
定义元素背景效果的 CSS 属性有五种：


-  8.CSS字体 (font)
font 属性可用于设置文本字体，定义样式，如加粗，大小等，属于复合属性，也叫做简写属性。

- 9.Web服务器
什么是web服务器、应用服务器和web容器？
目前，“应用服务器”和“web服务器”之间的界线已经变得模糊不清了。但是人们还把这两个术语区分开来，作为强调使用。在Java方面，web容器一般是指Servlet容器。Servlet容器是与Java Servlet交互的web容器的组件。web容器负责管理Servlet的生命周期、把URL映射到特定的Servlet、确保URL请求拥有正确的访问权限和更多类似的服务。综合来看，Servlet容器就是用来运行你的Servlet和维护它的生命周期的运行环境。

- 10.服务器脚本
服务器脚本是对服务器行为的编程，这被称为服务器脚本。作用如下：1.可以动态的对web页面进行增删改查。2.对用户提交的请求进行响应。3.与数据库进行链接，访问数据库，并将数据返回给浏览器。4.提高网页的安全性。5.减少浏览器带来的运行结果差异，
