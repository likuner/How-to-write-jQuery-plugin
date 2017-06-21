### Git常用命令
初始化一个项目
```
git init
```
从远程分支克隆一个版本库
```javascript
git clone https://github.com/likuner/fragment.git
```
克隆版本库时，远程分支自动被命名为origin，如果想自定义远程分支名
```
git clone -o repo https://github.com/likuner/fragment.git
```
查看工作区(working directory)的改动情况
```
git status
```
将工作区改动的代码添加到暂存区(stage/index)
```
git add ./
```
将暂存区改动的代码同步到本地版本库(repository)
```
git commit -m "take notes about this commit"
```
删除一个文件
```
git rm aa.md
```
删除一个文件夹
```
git rm -r aa
```
查看历史改动记录
```
git log --pretty=oneline
git reflog --pretty=oneline
```
回退到某一个历史版本
```
git reset --hard 111111
```
查看所有分支
```
git branch
```
创建一个分支
```
git branch dev
```
切换到指定分支
```
git checkout dev
```
删除指定分支
```
git branch -d dev
```
比较两个分支之间的差异
```
git log master...dev
```
合并dev分支的代码到master,需切换到master分支上
```
git merge dev
```
将master分支的代码提交到远程分支
```
git push origin master
```
取回远程分支的更新
```
git fetch origin master
```
取回远程分支的更新，并与本地分至合并
```
git pull origin master
```
查看所有远程主机
```
git remote -v
```
添加远程主机
```
git remote add repo https://github.com/likuner/fragment.git
```
删除远程主机
```
git remote rm repo
```
重新命名远程主机
```
git remote rename repo newrepo
```
修改配置信息
```
git config --global user.name=peter
git config --global user.email=111@163.com
```

