# Git最基础

## 命令一览 
```bash

# 下载一个远程仓库和它的整个代码历史
$ git clone [url]

# 取回远程仓库的变化，并与本地分支合并
$ git pull [remote] [branch]

# 设置提交代码时的用户信息
$ git config [--global] user.name "[name]"
$ git config [--global] user.email "[email address]"

# 添加指定文件到暂存区
$ git add [file1] [file2] ...

# 添加指定目录到暂存区，包括子目录
$ git add [dir]

# 提交暂存区到仓库区
$ git commit -m [message]

# 显示有变更的文件
$ git status

# 显示某次提交的元数据和内容变化
$ git show [commit]

# 显示当前分支的最近几次提交
$ git reflog

# 显示所有远程仓库
$ git remote -v

# 上传本地指定分支到远程仓库
$ git push [remote] [branch]
```
## 几个重要步骤
### git pull——整齐划一的起点
> git操作最终还是为了发布——将每一次的修改、补丁发布到远端的Git仓库中；
> 本地git仓要先与远端仓库‘站在同一起跑线’，后续的修改、发布才算有了*起点*
### git commit——工作进程的转折点
### git push——有始有终的终点
