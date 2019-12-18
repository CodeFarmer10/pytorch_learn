# Git命令学习笔记

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