---
layout: page
title: 首页布局不好看？如何隐藏文章部分内容，显示摘要
excerpt_separator: "<!--more-->"
categories:
     - 网站设计
---

# 篇三
## title: 首页布局不好看？如何隐藏文章部分内容，显示摘要
#### 多人在进行jekyll实践的时候会发现，在进行文章编写完成之后，在主页居然显示了整篇文章， 实践如何隐藏部分文章内容，显示摘要内容。
<!--more-->

## 我遇到的问题:
在我进行文章部署的时候，发生了以下的问题

页面显示的内容太多了我想要只显示文章的摘要，是页面可读性增强，那应该怎么办呢？
后来我参考了[廖老师的页面](http://hanteng.gitee.io/jekyll-theme-basically-basic/)
![](/assets/images/Website Design/2019-06-25-Website Design_more_1.jpg)  
发现他的文章就是只显示文章摘要
后来我就去后台查看[廖老师的文章](https://gitee.com/hanteng/jekyll-theme-basically-basic/raw/gh-pages/_posts/2019-03-01-Platform_01.md)
发现有些不一样的地方，所以决定去寻找答案
![](/assets/images/Website Design/2019-06-25-Website Design_more_2.jpg)  
## 我怎么找答案
bing中搜索jekyll隐藏部分文章
最终终于找到满意的答案
[找到的文章参考](https://juejin.im/post/5b3497ffe51d4558c5394a35/#heading-12)


## 答案参考
在问题头信息中插入
```
excerpt_separator: "<!--more-->"
```
更改后的文章头部信息应该是这样的
```
---
layout: page
title: 404报错？如何避免错误进行jekyll导航栏的设置
excerpt_separator: "<!--more-->"
categories:
     - 网站设计
---

```
然后在头部信息的下面编写你的文章摘要
如我的
```
在很多同学进行jekyll导航栏的部署的时候经常会出现404报错的问题？是因为代码编写错误？还是gitee本身的问题？
经过很多同学的踩雷经验，经历了很多次404的我们。对于jekyll导航栏的正确设置可以参考本片文章。避免踩雷，学习走起~
```
写完在这后面加入
```
<!--more-->
```
最终你的文章会是这样的格式
```
---
layout: page
title: 404报错？如何避免错误进行jekyll导航栏的设置
excerpt_separator: "<!--more-->"
categories:
     - 网站设计
---

在很多同学进行jekyll导航栏的部署的时候经常会出现404报错的问题？是因为代码编写错误？还是gitee本身的问题？
经过很多同学的踩雷经验，经历了很多次404的我们。对于jekyll导航栏的正确设置可以参考本片文章。避免踩雷，学习走起~

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
```
即添加头部信息之后，在再文章中添加`<!--more-->`,`<!--more-->`的上面是在主页显示的部分，下面为不显示的部分。
参考资料
[网上资料](https://juejin.im/post/5b3497ffe51d4558c5394a35/#heading-12)
[廖老师的文章实践](https://gitee.com/hanteng/jekyll-theme-basically-basic/raw/gh-pages/_posts/2019-03-01-Platform_01.md)
