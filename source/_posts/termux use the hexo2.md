---
title: 在termux中折腾hexo（2，让别人看到你的网站）
date: 2022-2-12 15:37:40
categories: termux
tags: hexo博客
---
# 注册GitHub账号
这玩意有手就行，这里直接略去。
# 创建GitHub的个人仓库
有手就行，不过请注意，仓库名必须和你的名字一样，将来要部署到GitHub的时候，才会被识别，也就是（你的名字.github.io）。
### 生成ssh ~~本来不想写的~~
在终端中输入：
<!-- more -->
`git config --global user.name "你的名字"
git config --global user.email "你的GitHub邮箱"`
再输入一个指令，创建ssh
ssh-keygen -t rsa -C "你的邮箱"
这时，你`ls`一下，会有一个.ssh的文件夹把它点开会发现里面有三个文件。
打开GitHub的设置，里面会有一个SSH and GPG keys的玩意，新建一个key，然后把id_rsa.pub（在.ssh文件夹里面）
然后在终端里面输入这个指令看看是否成功：
`ssh -T git@github.com`
### 把你的网站弄到GitHub上
打开配置文件_config.yml再最后面写上：
`deploy:`
  `type: git`
  `repo: https://github.com/你的名字/你的名字.github.io.git`
  `branch: master`
这个时候要安装deploy-git ，这样你才能用命令把你的网站部署到GitHub。
`npm install hexo-deployer-git --save`
然后：
`hexo clean`
`hexo generate`
`hexo deploy`
然后再访问一下`http://你的名字.github.io`看看是不是可以让别人看到你的网站了？
### 指令介绍
在这里，hexo clean是清除你之前生成的东西，一般可以不加，hexo generate是生成网页，可以用hexo g来代替，hexo deploy是把网站搞到GitHub上可以用hexo d代替。
注意，deploy时系统可能问你用户名和邮箱，照输进去就OK了
