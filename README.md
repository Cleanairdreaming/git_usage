# Git self-guidance  
## 目录  
- [Git self-guidance](#git-self-guidance)
  - [目录](#目录)
  - [1 添加文件](#1-添加文件)
  - [2 添加到远程仓库](#2-添加到远程仓库)
  - [3 push](#3-push)
  - [4 获取远程数据](#4-获取远程数据)
    - [4.1 fetch and merge](#41-fetch-and-merge)
    - [4.2 pull](#42-pull)
  - [5 修改后提交](#5-修改后提交)
  - [6 有语法疑问](#6-有语法疑问)
  - [7 删除所有提交历史记录](#7-删除所有提交历史记录)

## 1 添加文件
* 自己创建文件
切换到工作目录  
`$ cd /target/dir`  
初始化工作目录  
`$ git init`  
添加当前目录到git  
`$ git add .`  

* clone仓库，省去了添加到远程仓库的操作  
`$ git init`  
`$ git clone <repositoy url>`  

## 2 添加到远程仓库
`$ git remote add origin https://github.com/your/repository/link.git`  

## 3 push 
设定upstream  
`$ git push --set-upstream origin master`  
推送文件  
`$ git push -u origin master, or git push.`  

## 4 获取远程数据
### 4.1 fetch and merge  
* Fetch files  
git fetch  
`$ git fetch <远程主机名> //这个命令将某个远程主机的更新全部取回本地`  
or fetch the specified branch  
`$ git fetch <远程主机名> <分支名> //注意之间有空格`  
commonly used command  
`$ git fetch origin master`  
or simply use  
`$ git fetch`  

* Check the updates info  
`$ git log -p FETCH_HEAD`  

* Merge the updates  
`$ git merge FETCH_HEAD`  

### 4.2 pull
* Synopsis  
`$ git pull [<options>] [<repository> [<refspec>…]]`  
or simply  
`$ git pull`  

## 5 修改后提交
* 修改后须重新添加  
`$ git add .`  
* 提交修改  
`$ git commit -m "change text"`  
* push  
push见[步骤3](#3-push)  
## 6 有语法疑问
* 如果有语法疑问直接  
`$ git help <command>`  
* 备忘参考
[cheat sheet for github](/docs/github-git-cheat-sheet.pdf)  
[cheat sheet offical link](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)

## 7 删除所有提交历史记录  
具体实现方式为：  
1. 生成新的仓库  
`$ git checkout --orphan latest_branch `  
1. 把所有文件添加到新仓库  
`$ git add -A`  
1. 提交  
`$ git commit -am "commit message" `  
1. 删除master仓库  
`$ git branch -D master `  
1. 重名命当前仓库  
`$ git branch -m master `  
1. 强制更新当前仓库  
`$ git push -f origin master `    


