---
layout: post
title:  "利用Git拉取远程仓库"
date:   2020-12-13 15:10:12 +0530
categories: Git Github
---
## 1.先创建一个文件夹，名字为远程仓库的名称
![如图所示](https://img-blog.csdnimg.cn/20201204151048355.png#pic_center)

## 2.在该文件目录下打开Git Bash
## 3.输入git init,进行初始化
## 4.连接远程仓库
输入下列命令
```
git remote add origin git@github.com:yourName/repositoryname.git
git remote add origin https://github.com/yourName/repositoryname.git
```
# 5.从远程仓库拉取文件
```
git pull origin master
```
# 6.查看工作目录状态
```
git status
```
# 7.提交更改，添加备注信息
```
git commit -m "备注信息"
注意：若第6步的信息中有以下情况：
1.Untraked Files
使用git add .解决该问题
2.Changes not staged for commit
使用 git commit -am "备注信息" 解决
```
# 8.将本地文件push到远程仓库
```
git push origin master
```
更多精彩即将呈现。

