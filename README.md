# git常见命令
以下是一些常用的 Git 命令：

1. 克隆远程仓库到本地：

```
git clone <remote_repository_url>
```

2. 拉取远程仓库的最新代码：

```
git pull
```

3. 查看当前项目的状态：

```
git status
```

4. 添加所有更改的文件到暂存区：

```
git add .
```

5. 提交暂存区的文件到本地仓库：

```
git commit -m "commit message"
```

6. 将本地仓库的代码推送到远程仓库：

```
git push
```

7. 创建新分支:

```
git branch new-branch-name>
```

8. 切换到某个分支:

```
git checkout <branch-name>
```

9. 查看历史版本（按行查看）:

```
git log --oneline
```

10. 查看当前仓库有多少分支:

```
git branch
```


# git push -u origin master 跟git push origin master 有什么区别
`git push -u origin master` 和 `git push origin master` 的区别在于是否设置了上游分支（upstream branch）。

`git push -u origin master` 命令会将本地分支 `master` 推送到远程仓库的 `origin` 仓库，并将本地分支与远程分支建立关联，使得本地分支成为远程分支的上游分支。这样，在以后的推送或拉取操作中，Git 将自动将本地分支与远程分支进行比较和合并，从而更方便地进行协作开发。

`git push origin master` 命令只是将本地分支 `master` 推送到远程仓库的 `origin` 仓库，但不会建立本地分支与远程分支的关联。这意味着，在以后的推送或拉取操作中，Git 不会自动将本地分支与远程分支进行比较和合并，需要手动指定远程分支名进行操作。

在第一次推送本地分支时，应该使用 `git push -u origin master` 命令，以建立本地分支和远程分支之间的关联。之后，可以使用 `git push` 命令进行推送操作，Git 将自动将本地分支与远程分支进行比较和合并。如果需要推送其他分支，也可以使用类似的命令建立分支关联。

# 查看某个文件的历史版本或回滚到某个历史版本
`git log --oneline` 查看历史版本记录，找到要查看的例示版本SHA-1。

`git checkout <SHA-1号码> <文件名称>`  该命令就可以查看某个例示版本。若需要执行回滚，则此时用 `git commit ...`  去提交。
# 推送新分支到远程仓库
使用`git push --all origin`  以及 `git push --tags origin` 去推送。单独推送到github可能会产生一些意外。
