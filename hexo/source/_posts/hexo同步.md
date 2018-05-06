---
layout: poat
title: hexo同步
tags:
---
<p><b>历经多次碰壁，终于把这个同步的问题解决了థ౪థ<br>
大致了解一下步骤</b></p><br>
<ul>
<li>A上传</li>
<li>B下载</li>
<li>进入项目文件</li>
<li>安装hexo再配置一下</li>
</ul>
假设两台有A、B两台设备<br>A已经搭好hexo  B全新 分支名：hexo
<br>
<p><b>上传</b></p>
A把本地的项目上传到github。<br>
>git init #git初始化 
>git remote add origin https://github.com/用户名/你的GitHub用户名.github.io.git #添加仓库地址 
git checkout -b hexo #新建分支并切换到新建的分支 
git add . #添加所有本地文件到git 
git commit -m "这里填写你本次提交的备注，内容随意" #git提交 
>git push origin 分支名 #文件推送到hexo分支
<br>
<p><b>下载</b></p>
好了，A完工接下来轮到B选手上场<br>
看啊，B上来就是一套技能<br>
>pkg install git
>pkg install nodejs
>git clone -b 分支名 https://github.com/用户名/你的GitHub用户

<p><b>安装</b></p>
<br>接着B乘胜追击cd进了那个克隆下来的文件夹里<br>
>npm install -g hexo-cli #安装hexo,注意这里不需要hexo初始化,否则之前的hexo配置参数会重置 
>npm install --save
>npm install #安装依赖库 
>npm install hexo-deployer-git #安装git部署相关配置
<br>
<h1>victory</h1><br>

<p><b>后续的发表与同步</b></p>
<br>
>hexo g -d
>git add . 
>git commit -m "这里填写你本次提交的备注" 
>git push origin 分支名
<br>
<p><b>完成后再夸一下自己 []~（￣▽￣）~*</b></p>