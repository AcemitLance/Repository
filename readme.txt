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