# Git命令学习笔记

## 基本操作

- 初始化仓库

  > git init

- 添加文件至仓库

  > git add <filename>  #到暂存区

- 文件提交到仓库

  > git commit -m  <message> #一次性将暂存区提交到分支

- 查看仓库当前状态

  > git status

- 对比文件,查看修改

  > git diff <filename>

- 查看提交日志

  > git log 
  >
  > git log --pretty=oneline
  >
  > git log --graph #分支合并图

- 版本回退

  > git reset --hard HEAD^    删除新增本地文件
  >
  > git reset --soft HEAD^     不删除新增本地文件
  >
  > git reset --hard <verisonid>

- 查看命令历史

  > git reflog

- 撤销文件修改

  > git checkout -- <filename>  #恢复到最近一次git commit或git add时的状态
  >
  > git reset HEAD <filename> #撤销暂存区的修改，放回工作区

- 删除文件

  > git rm <filename>

- 关联远程仓库

  > git remote add origin <远程仓库地址>  #origin远程库名称，可修改

- 推送分支

  > git push -u origin <branchname> # -u第一次推送，本地分支与远程分支关联

- 克隆仓库

  > git clone <远程仓库地址>

## 分支管理

- 创建分支

  > git checkout -b <branchname>  # -b创建并切换
  >
  > git branch <branchname> # 创建分支

- 切换分支

  > git checkout <branchname>

- 查看当前分支

  > git branch

- 删除分支

  > git branch -d <branchname>
  >
  > git branch -D <branchname> #强行删除未合并的分支

- 合并分支

  > git merge <branchname>  #Fast forward模式，删除分支后，丢掉分支信息
  >
  > git merge --no-f -m <message> <branchname> #禁用Fast forward模式，生成新的commit，分支历史看出分支信息

- 储藏工作现场

  > git stash

- 查看工作现场列表

  > git stash list

- 恢复工作现场

  > git stash apply   #恢复后，stash并不删除
  >
  > git stash pop      #恢复并删除stash
  >
  > git stash drop     #删除stash

- 复制特定的提交到当前分支

  > git cherry-pick <versionid>