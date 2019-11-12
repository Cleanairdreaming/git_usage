# git_usage

## 1 添加文件
cd /target/dir  
git add .  

## 2 添加到远程仓库
git remote add origin https://github.com/your/repository/link.git  

## 3 push 
设定upstream  
git push --set-upstream origin master  
推送文件  
git push -u origin master, or git push.  

## 4 获取远程数据
git fetch origin

## 5 修改后提交
git commit -m "change text"  
push见[步骤3](#3-push)
