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


git checkout -- file 把文件在工作区的修改全部撤销，这里有两种情况：

一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；

一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。

总之，就是让这个文件回到最近一次git commit或git add时的状态。

git rm 用于删除一个文件

 git remote add origin git@github.com:michaelliao/learngit.git  本地仓库关联github仓库


把本地库的内容推送到远程，用git push命令  git push -u origin master

git clone 克隆远程仓库到本地

git checkout命令加上-b参数表示创建并切换分支 如git checkout -b dev
git branch命令会列出所有分支，当前分支前面会标一个*号
测试分支
git checkout master 切换回主分支
git merge命令用于合并指定分支到当前分支
git branch -d <dev> 删除指定分支

查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>   准备合并dev分支，请注意--no-ff参数，表示禁用Fast forward：

删除分支：git branch -d <name>

用git log --graph命令可以看到分支合并图。
git status查看工作区，就是干净的（除非有没有被Git管理的文件），因此可以放心地创建分支来修复bug。

首先确定要在哪个分支上修复bug，假定需要在master分支上修复，就从master创建临时分支：

git stash list命令刚才的工作现场存到哪去了
工作现场还在，Git把stash内容存在某个地方了，但是需要恢复一下，有两个办法：

一是用git stash apply恢复，但是恢复后，stash内容并不删除，你需要用git stash drop来删除；

另一种方式是用git stash pop，恢复的同时把stash内容也删了：

