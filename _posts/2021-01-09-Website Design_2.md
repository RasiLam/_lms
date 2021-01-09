---
layout: page
title: 404报错？如何避免错误进行jekyll导航栏的设置
excerpt_separator: <!--more-->
categories:
     - 网页设计
---

# 篇二
## title: 404报错？如何避免错误进行jekyll导航栏的设置
#### 在很多同学进行jekyll导航栏的部署的时候经常会出现404报错的问题？是因为代码编写错误？还是gitee本身的问题？
#### 经过很多同学的踩雷经验，经历了很多次404的我们。对于jekyll导航栏的正确设置可以参考本片文章。避免踩雷，学习走起~

<!--more-->

### jekyll目录结构主要包含如下目录：
- _posts 博客内容
- _pages 其他需要生成的网页，如About页
- _layouts 网页排版模板
- _includes 被模板包含的HTML片段,可在_config.yml中修改位置
- assets 辅助资源 css布局 js脚本 图片等
- _data 动态数据
- _sites 最终生成的静态网页
- _config.yml 网站的一些配置信息
- index.html 网站的入口  

### 在本套主题中进行Jekyll的导航设置需要注意一下几点：
- 文章头部信息的撰写(官方文档关于头部信息的解释)[https://jekyllrb.com/docs/front-matter/]：所以的头部信息设置都是根据主题模板的不同进行设置的
- 文件的命名规范以及存放位置


### 头部信息的撰写
- 利用page模板设置，再利用categories/tags标注文章 category/tag模板进行分类显示
首先，在我们的根目录创建好我们需要的导航文章
- -关于我/about/
- -网站设计 /categories/网站设计/
- -平面设计  / categories /平面设计/
- -SVG制作  /tags/SVG制作/
- -学习笔记

![](/assets/images/Website Design/2019-6-24-nav1.jpg)

一定要在根目录下先创建好需要的导航模板文件
然后再对你所创建的文件做出以下更改：

```
---
title: 网站设计
layout: category
permalink: /categories/网站设计/
taxonomy: 网站设计
---
```

title为在导航中显示的导航文本，permalink路径的设置需要与文章同步
文章的头部信息的写法

```
---
layout: page
title: 响应式网页设计
categories:
     - 网站设计
---
```

title即为你文章的标题，需要自己起标题
categories为你需要分类到哪一个类别，如网站设计，你就可以在网站设计导航里面看见你所分类的文章

完成各个导航的文章模板设置和文章设置之后需要去往`jekyll-theme-basically-basic /_data`里面修改导航设置

![](/assets/images/Website Design/2019-6-24-nav2.jpg)

代码如下：
```
navigation_pages:
  - about.md
  - 网站设计.md
  - 平面设计.md
  - svg制作.md
  - 学习笔记.md
```
#### ps：在编写yml文件和头部信息的时候要记得空格缩进、大小写、中英文、标点符号等的yml格式编写注意事项。否则会报错，404！！！参照以上代码的同学，需要把所有的需要的导航都设置完再部署，仔细检查yml格式,可利用[YAML 文档除错工具](http://www.yamllint.com/)进行查错
