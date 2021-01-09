---
layout: page
title: jekyll网站实现分页，多页面显示文章你学会了吗？
excerpt_separator: "<!--more-->"
categories:
     - 学习笔记
---

# 篇二
## title: jekyll网站实现分页，多页面显示文章你学会了吗？
#### 通过对jekyll网站设置，实现主页的分页化浏览

<!--more-->

对于许多网站尤其是博客将帖子的主要列表分成较小的列表并将其显示在多个页面上是很常见的。
Jekyll提供了一个分页插件，因此您可以自动生成分页列表所需的相应文件和文件夹。


### [本主题的分页设置指南](https://gitee.com/huangjieqi/huangjieqi#pagination)

#### 要点：
- 进行`_config.yml`文件的设置
- 文章的分页显示都需要在html文档中进行，所以需要将`index.md`修改为`index.html`
- 设置文章分页显示还需在头部信息中进行注明。

#### 步骤一
进行文件的修改  
将根目录下的将`index.md`修改为`index.html`
具体参考此条仓库修改[commit](https://gitee.com/huangjieqi/huangjieqi/commit/72435471168dd4dd4d3c22ffa598682a8cb23bdc)

#### 步骤二
设置分页数目(本主题下进行设置)
进入根目录下的`_config.yml`文件
```yml
paginate: 5  # 一个页面存放/显示多少篇文章
paginate_path: /page:num/
```

原理：
通过添加jekyll插件实现，可以在`_config.yml`文件中看到
```yml
plugins: # previsously gems
  - jekyll-feed
  - jekyll-seo-tag
  - jekyll-sitemap
  - jekyll-paginate
```
其中的`jekyll-paginate`就是开启分页的插件


#### 步骤三
修改`index.html`的头部信息
##### 修改前：
```yml
---
layout: home
image: assets/images/banner/home.jpg
---

```

##### 修改后
```yml
---
layout: home
image: assets/images/banner/home.jpg
paginate: true
---

```

我们可以发现，只需要在头部信息中增加一行代码即可开启分页设置,就是以下这条代码了
```yml
paginate: true
```


#### 总结
开启分页只需要在`_config.yml`中设置分页页数，再将`index.md`修改为`index.html`，最后在`index.html`中添加头部信息`paginate: true`即可完成
祝大家实践成功！！！
