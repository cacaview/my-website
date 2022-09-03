---
title: 在termux中折腾hexo（3，配置你的网站）
date: 2022-02-12 15:50:31
categories: termux
tags: hexo博客
---
先配置一下你的网站再给别人看吧~
### 网站基本配置
在你的hexo主目录中有一个叫做`_config.yml`的文件，它是整个网站的配置文件，里面可以看到hexo的大部分配置。你可以在里面修改网站配置，[可前往官网上查看](https://hexo.io/zh-cn/docs/configuration)
这是网站的配置：
- title   网站的标题

- subtitle   网站副标题

- description    网站描述

<!-- more -->

- author   您的名字

- language   网站语言

- timezone   网站时区，hexo默认使用你手机上的时区

其中，description主要用于SEO，告诉搜索引擎一个关于你的网站简单描述，通常建议在其中包含您网站的关键词。author参数用于主题显示文章的作者。自己自行配置。或查看官方文档。

这是网址的配置：

- url   网址，填你的网站域名

- root   网站的根目录

- permalink   网站的链接格式

- permalink_defaults   永久链接中各部分的默认值

对于链接格式，[可以到官网上查看](https://hexo.io/zh-cn/docs/permalinks)
中间的默认即可，接下来我们就来换一个主题吧
### 美化你的网站

如果你觉得默认的landscape主题不好看，那么可以在官网的主题中，选择你喜欢的一个主题进行修改就可以啦。[这里推荐next主题](https://hexo.io/themes/)
我们直接在github链接上下载下来，然后放到theme文件夹下就行了，然后再在刚才说的配置文件中把theme换成那个主题文件夹的名字，它就会自动在theme文件夹中搜索你配置的主题。
而后进入next这个文件夹，可以看到里面也有一个配置文件_config.xml，有时候它默认是_config.xml.example，把它复制一份，重命名为_config.xml就可以了。
### 菜单栏
在菜单栏中的about中，你是看不到网页的。但你可以：
`hexo new page about`
它就会在根目录下source文件夹中新建了一个about文件夹，以及index.md，在index.md中写上你想要写的东西，就可以在网站上展示出来了。
如果你想新建一个菜单栏选项，你可以：
`hexo new page yourdiy`
然后在主题配置文件的menu菜单栏添加一个 Yourdiy : /yourdiy，注意冒号后面要有空格，以及前面的空格要和menu中默认的保持整齐。然后在languages文件夹中，找到zh-CN.yml，在index中添加yourdiy: '中文意思'就可以显示中文了。
