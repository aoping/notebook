## 参考资料
[Git Workflows and Tutorials](https://github.com/oldratlee/translations/tree/master/git-workflows-and-tutorials)

## 集中式工作流
- git init --bare /path/to/repo.git
- git clone
- git status # 查看本地仓库的修改状态
- git add # 暂存文件
- git commit # 提交文件
- git push (git push origin master)
```
主流的git版本，可以省略后面2个参数：远程仓库别名、推送分支
```
- git pull --rebase (git pull --rebase origin master)
- git add <some-file> 
- git rebase --continue
- git rebase --abort

## 功能分支工作流
- git checkout -b marys-feature (git checkout -b marys-feature master)
- git push -u origin marys-feature
```
-u选项设置本地分支去跟踪远程对应的分支
```
- 开发者每次在开始新功能前先创建一个新分支。 功能分支应该有个有描述性的名字，比如animated-menu-items或issue-#1061，这样可以让分支有个清楚且高聚焦的用途。

## Gitflow工作流


## Forking工作流


## Pull Requests


