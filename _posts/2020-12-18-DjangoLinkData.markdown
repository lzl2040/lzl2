---
layout: post
title:  Django连接数据库
date:   2020-12-18 16:34:33 +0530
categories: Django 数据库
---
在利用Pycharm写后端的时候，我们常常需要连接数据库来方便操作，但这具体怎么做呢？相信很多初次接触这方面的人会很摸不着头脑，下面就是PyCharm中的Django项目连接数据库的操作。

## 1.建立一个数据库
为了方便管理。可以用[phpstudy]来管理操作，它里面集成了很多套件，环境一键配置，不需要再自行安装MySQL等  

![如图所示](https://gitee.com/lzl2040/pic-store/raw/master/jekyll-2020-12-18-DjangoLink/link-5.png)  
安装完成后启动MySQL5.7.X，Apache（Apache与Nginx二选一启动，用于数据库的可视化管理）
注意：如果自己之前安装过MySQL，phpstudy中的数据库服务启动不了！此时需要删掉原来安装过的Mysql,phpstudy中的Mysql要选择5.7.X版本，选择其他版本数据库导入时会出错！  
![如图所示](https://gitee.com/lzl2040/pic-store/raw/master/jekyll-2020-12-18-DjangoLink/link-6.png)
## 2.打开PyCharm,建立一个Django项目
这个打开Pycharm后就能看到一个Create Project
## 3.点击右边的DataBase,如图,选择Mysql,配置好地址，数据库的一些名称
具体情况如下图:  
![](https://gitee.com/lzl2040/pic-store/raw/master/jekyll-2020-12-18-DjangoLink/link-3.png)  
![](https://gitee.com/lzl2040/pic-store/raw/master/jekyll-2020-12-18-DjangoLink/link-4.png)  
![](https://gitee.com/lzl2040/pic-store/raw/master/jekyll-2020-12-18-DjangoLink/link-2.png)  
端口使用默认的3306即可
## 4.在Django项目中的settings.py文件中配置数据库

![如图](https://gitee.com/lzl2040/pic-store/raw/master/jekyll-2020-12-18-DjangoLink/link-1.png)

[phpstudy]:https://www.xp.cn/download.html