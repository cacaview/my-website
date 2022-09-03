---
title: 使用taskel在大便系统中安装各种东西
date: 2021-12-4 13:20:18
categories: Linux
tags: 技术支持
---

在ubuntu系统中，常用的安装软件命令有apt和pkg。当然，还有一种更为简单的方式。那就是一个叫做tasksel的东西。

tasksel是一个易于使用的软件安装器，他可以快速的安装例如LAMP服务器，邮件服务器 ，DNS服务器之类的软件，有点像宝塔一键安装软件套装一样。

## 安装tasksel

要安装tasksel，只需要一个指令：
apt-get install tasksel -y
安装Tasksel后，它可以安装一个或多个预定义的软件包组。 用户需要使用几个参数从命令行运行它，当然，它也提供了一个图形用户界面，可以选择要安装的软件。
<!-- more -->
## tasksel的用法

tasksel的一般语法为：
sudo tasksel install task_name
sudo tasksel remove task_name
sudo tasksel command_line_options
如果要用他的图像界面，则只需要：
sudo tasksel

你也许看到了有些选项前面有（*），这代表了它已经安装，你可以使用向上和向下箭头，移动红色高亮部分，按空格键来选择软件，并使用Tab键移动到<ok> 。 然后按回车键安装

或者，你也可以使用以下命令从命令行中列出所有任务。 注意，在表的第一列， u （卸载）指软件没有安装和i （安装）装置安装的软件。
如：
sudo tasksel --list-tasks

## 更多用法

使用man帮助页查看更多的用法：
man tasksel