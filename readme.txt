git init   添加仓库
git add <文件名>   把文件添加到仓库
git commit 告诉git把文件提交到仓库
	-m后面输入的是本次提交的说明 如 git commit -m "添加了一行"
git status 命令可以让我们时刻掌握仓库当前的状态
git diff <文件名>  查看具体修改了什么内容
git log 命令显示从最近到最远的提交日志  git log --pretty=oneline
试试回退功能
在Git中，用HEAD表示当前版本，上一个版本就是HEAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来，所以写成HEAD~100。
git reset --hard HEAD(或版本号或HEAD^等)
git reflog用来记录你的每一次命令

Git版本库里添加的时候，是分两步执行的：

第一步是用git add把文件添加进去，实际上就是把文件修改添加到暂存区；

第二步是用git commit提交更改，实际上就是把暂存区的所有内容提交到当前分支。

