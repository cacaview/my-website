---
title: 在termux中折腾hexo（1）
date: 2021-11-28 23:13:40
categories: termux
tags: hexo博客
---

本文将会分几个片段来介绍在termux中安装，配置，以及美化hexo博客的过程

# hexo介绍

Hexo是一款基于Node.js的静态博客框架，依赖少易于安装使用，可以方便的生成静态网页托管在GitHub和Coding上，是搭建博客的首选框架。大家可以进入hexo的官网进行详细查看

# 第一步：安装Git

hexo的网页托管在Git上。对于Linux来说，安装git真的是太简单了，因为最开始的git就是在Linux系统上写出来的。对此，我们这需要一条指令：
sudo apt-get install git
<!-- more -->
# 第二步：安装nodejs

Hexo是基于nodeJS编写的，所以需要安装一下nodeJs和里面的npm工具。这十分简单，只需两条指令：
sudo apt-get install nodejs
sudo apt-get install npm
接着输入以下指令验证是否安装成功：
node -v
npm -v

# 第三步，请出我们的hexo

[如果不出什么差错，我们应该就可以来安装hexo了，建议新建一个文件夹，显得没这么乱。
输入这个命令安装hexo：
npm install -g hexo-cli
使用hexo -v来看看是否安装成功
接着初始化一下hexo：
hexo init myblog
这个myblog起什么名字都可以的，你喜欢就好
接着：
cd myblog
npm install
至此，hexo的东西就都弄好了。

# 接下来……

弄好之后，你ls一下，你的目录中会有以下文件：

node_modules: 依赖包

public：存放生成的页面

scaffolds：生成文章的一些模板

source：用来存放你的文章

themes：主题

_config.yml: 博客的配置文件
输入这个指令：
hexo g
hexo server
这是打开hexo的服务，在浏览器输入localhost:4000就可以看到你的博客啦
按ctrl+c可以把服务关掉。