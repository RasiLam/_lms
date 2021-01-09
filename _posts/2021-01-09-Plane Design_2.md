---
layout: page
title: 你的网页字体安全吗？什么是衬线字体与非衬线字体？
excerpt_separator: <!--more-->
categories:
     - 平面设计
---

# 篇二
## title: 你的网页字体安全吗？什么是衬线字体与非衬线字体？
#### 什么是衬线字体？什么又是非衬线字体，你用的衬线和非衬线字体安全吗？进行网站内文和标题衬线字体的设置！
<!--more-->
让我们来学习衬线与非衬线字体的区别，打造更好看的网页。网页字体的设置往往跟浏览器所支持的字体编码有关，随着互联网的进步，浏览器包容的字体类型也越来越多，衬线字体与非衬线字体也开始被广泛应用


### 什么是衬线字体与非衬线字体
![衬线字体与非衬线字体](http://www.mrszhao.com/zb_users/upload/2017/02/201702161487217295544464.png)
* 衬线体的笔画在开始和结束处有额外的修饰，并且笔画横竖粗细不一。
* 非衬线体则是所有笔画粗细一致，并且在笔画的开始和结束处没有额外的修饰线条。  

![对比](http://www.mrszhao.com/zb_users/upload/2017/02/201702161487225911468675.jpg)  

#### 衬线体（serif）
* 「衬线」指的是字形笔画在首位的装饰和笔画的粗细不同，所以「衬线」又被称为「字脚」。
*  这种装饰线的笔画设计多认为来源于古罗马纪念碑上的拉丁字母，1968 年 Edward Catich 神父在著作《The Origin of the Serif》中提到罗马字母最初被雕刻到石碑上之前，要先用方头笔刷写好样子，再照样雕凿。由于直接用方头笔刷书写会导致笔画的起始和结尾出现毛糙，所以在笔画开始、结束和转角的时候增加了收尾的笔画，也就自然形成了衬线。  
![](http://www.mrszhao.com/zb_users/upload/2017/02/201702161487226137888317.jpg)

#### 无衬线体（sans-serif）
* 而无衬线体则没有笔画首尾的装饰，所有笔画的粗细也相同。无衬线体在 80 年代开始兴起，在当时被称为 Grotesque（荒唐的）或 Gothic（哥特的），因为天然的技术感和理性气质，无衬线字体多为科技型企业所青睐。随着「简约美」理念开始风行，1957 年上市的 Folio、Helvetica 和 Univers 三个极具代表性的无衬线字型开始成为当代字型的主流。
* 因为无衬线的字体结构简单，在同等字号下，无衬线的字体看上去要比有衬线的更大，结构也更清晰，所以电子设备的屏幕上也偏好使用无衬线字体。  
![](http://www.mrszhao.com/zb_users/upload/2017/02/201702161487226256399169.png)

#### 中文界的衬线体与无衬线体
* 而在中文字体界，两个有代表性的分类——宋体和黑体，分别对应着衬线字体和无衬线字体。  
![](http://www.mrszhao.com/zb_users/upload/2017/02/201702161487226333858665.jpg)  

### jekyll中衬线体和无衬线体的修改!
![](/assets/images/Plane Design/2019-6-21-ziti1.jpg)  
在网页里，右键chorme inspector在原网页中均为无衬线体的格式
去源文件里找对应的css代码。找到在base.scss中，body没有使用变量，h1-h6使用变量“$headerline-font-family”
![](/assets/images/Plane Design/2019-6-21-ziti2.jpg)  
需要给body添加一个变量“$global-font-family”
![](/assets/images/Plane Design/2019-6-21-ziti3.jpg)  
之后要找到源文件中，$header-font-family和$global-font-family的规定。
找到了_variables.scss中的规定如下：
而$global-font-family的规定没有，需要自行添加。
![](/assets/images/Plane Design/2019-6-21-ziti4.jpg)  
按项目要求，要补充中文字体
所以，需要找到$header-font-family和$global-font-family两个变量的源代码。
找到了themes中，对应到你目前使用的皮肤，可以修改变量
![](/assets/images/Plane Design/2019-6-21-ziti5.jpg)  
$serif: DFKai-SB,Kai,Kaiti SC,KaiTi,BiauKai,\\6977\4F53,\\6977\4F53_GB2312,Songti SC,Georgia, Times, serif !default;
$sans-serif: "Helvetica Neue",YouYuan,\\5E7C\5706,幼圆,"Segoe UI",-apple-system, BlinkMacSystemFont, "Roboto", "Segoe UI","Helvetica Neue", "Lucida Grande", Arial, sans-serif !default;
也可自行添加所需字体


### 参考：
- [这20款字体你可以在web中放心使用](https://www.jianshu.com/p/95f8225603b0)
- [关于网页字体扯出来的一些事](https://www.jianshu.com/p/dc066b55e406)
- [原来衬线字体和非衬线字体是这样区分的！](http://www.mrszhao.com/post/72.html)
- [CSS 字体栈](https://www.cssfontstack.com/)
- [CSS字体font-family的正确选择方案](http://caibaojian.com/font-family.html)
