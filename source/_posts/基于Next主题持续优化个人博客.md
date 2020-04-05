---
title: 基于Next主题持续优化个人博客
date: 2020-04-05 21:56:41
tags: hexo
---

Hexo默认主题太简单，功能比较少，需要变更主题，最流行的主题是Next，样式简单，基本功能都有。更换主题很简单。

## 更换主题

Hexo官网中有很多推荐主题（[Hexo主题](https://hexo.io/themes/)），在其中搜索Next，可以查看示例（版本发布说明）与进入github代码库。

进入Github下载上一个稳定版本，https://github.com/theme-next/hexo-theme-next/tags，我下载的是7.7.2版本。

<img src="基于Next主题持续优化个人博客/image-20200405221102474.png" alt="image-20200405221102474" style="zoom:50%;" />

下载后，解压到博客目录下的themes目录内，blog/themes/next-7.7.2。然后变更主配置文件的theme

~~~yml blog/_config.yml
theme: next-7.7.2
~~~

重启Hexo服务，查看效果（我已经在主配置中修改了博客名：解思垚）：

![image-20200405225450089](基于Next主题持续优化个人博客/image-20200405225450089.png)

## 配置Next

配置参考：[Next-Getting-Started](https://theme-next.org/docs/getting-started/)

### 修改样式

~~~yml next-7.7.2/_config.yml
#scheme: Muse
#scheme: Mist
#scheme: Pisces
scheme: Gemini #左小右大
~~~

![image-20200405231749022](基于Next主题持续优化个人博客/image-20200405231749022.png)

### 添加标签

~~~shell
hexo new page tags # INFO  Created: D:\github\blog\source\tags\index.md
~~~

在新建的blog/source/tags/index.md中修改标签页

~~~markdown source/tags/index.md
---
title: 标签
date: 2020-04-05 23:03:46
type: tags
---
~~~

将标签页加到菜单中

~~~yml next-7.7.2/_config.yml
menu:
  home: / || home
  #about: /about/ || user
  tags: /tags/ || tags
~~~

|| 前是目录，|| 后是图标

tag添加在文章的头部说明中。

### 添加分类

分类和标签类似，略

### 添加图册

类似分类和标签。



### 画廊功能

文章内图片支持浮现

~~~yml next-7.7.2/_config.yml
fancybox: true
~~~

