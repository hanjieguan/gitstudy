# git push -u origin master 跟git push origin master 有什么区别
`git push -u origin master` 和 `git push origin master` 的区别在于是否设置了上游分支（upstream branch）。

`git push -u origin master` 命令会将本地分支 `master` 推送到远程仓库的 `origin` 仓库，并将本地分支与远程分支建立关联，使得本地分支成为远程分支的上游分支。这样，在以后的推送或拉取操作中，Git 将自动将本地分支与远程分支进行比较和合并，从而更方便地进行协作开发。

`git push origin master` 命令只是将本地分支 `master` 推送到远程仓库的 `origin` 仓库，但不会建立本地分支与远程分支的关联。这意味着，在以后的推送或拉取操作中，Git 不会自动将本地分支与远程分支进行比较和合并，需要手动指定远程分支名进行操作。

在第一次推送本地分支时，应该使用 `git push -u origin master` 命令，以建立本地分支和远程分支之间的关联。之后，可以使用 `git push` 命令进行推送操作，Git 将自动将本地分支与远程分支进行比较和合并。如果需要推送其他分支，也可以使用类似的命令建立分支关联。
