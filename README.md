## git使用

Basic Commands

1.git   inint//初始化本地git仓库

2.git add<file> //添加文件

(1)git add  *.html //添加所有的html文件

(2)gi add . //添加所有文件

3.git status //查看状态

4.git commit//提交

5.git push //推送到仓库

6.git pull //从远程仓库拉去数据

7.git clone  //从远程仓库拷贝数据

8.git rm   //删除文件

## git安装  

windows安装路径<https://git-scm.com/download/win>

Git添加文件操作

git引入文件   Git commit

1.按键盘字母 i 进入insert模式

2.修改最上面那行黄色合并信息,可以不修改

3.按键盘左上角"Esc"

4.输入":wq",注意是冒号+wq,按回车键即可

也可以使用 -m 参数后跟提交说明的方式，在一行命令中提交更新。即：git commit -m "这里是信息"，添加就不会出现提示了

git 使用Git diff  查看修改痕迹

`git add`命令实际上就是把要提交的所有修改放到暂存区（Stage），然后，执行`git commit`就可以一次性把暂存区的所有修改提交到分支。

![1564839755293](C:\Users\Dell\AppData\Local\Temp\1564839755293.png)

![1564832185762](C:\Users\Dell\AppData\Local\Temp\1564832185762.png)

git 忽略文件设置

使用touch  设置  .gitignore文件

2.使用Git add .gitignore命令添加 到暂存库

3.将忽略的文件添加到 .gitignore中。将不再提示未加入Git库中

![1564834888075](C:\Users\Dell\AppData\Local\Temp\1564834888075.png)

![1564834911533](C:\Users\Dell\AppData\Local\Temp\1564834911533.png)

### Windows常用操作

1.使用mkdir  xx  可以创建文件夹

2.在g使用type nul>xx  创建新的文件

使用Git bash here 使用  touch 命令创建文件

### git  版本退回

- `HEAD`指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令`git reset --hard commit_id`。
- 穿梭前，用`git log`可以查看提交历史，以便确定要回退到哪个版本。
- 要重返未来，用`git reflog`查看命令历史，以便确定要回到未来的哪个版本。

### git  版本撤回

场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令`git checkout -- file`。

场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令`git reset HEAD <file>`，就回到了场景1，第二步按场景1操作。

场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考[版本回退](https://www.liaoxuefeng.com/wiki/896043488029600/897013573512192)一节，不过前提是没有推送到远程库。

### git 版本删除

命令`git rm`用于删除一个文件。如果一个文件已经被提交到版本库，那么你永远不用担心误删，但是要小心，你只能恢复文件到最新版本，你会丢失**最近一次提交后你修改的内容**。

git 分支

1.git branch login

1.Git  checkout login

## github使用

1.创建一个账号

2.将文件添加到Github

git remote add origin https://github.com/luwei113/newstart.git
git push -u origin    xx//xx:master系统自己创建的分支

git clone      xx  // xx:GitHub地址

## git 分支使用

Git鼓励大量使用分支：

查看分支：`git branch`

创建分支：`git branch <name>`

切换分支：`git checkout <name>`

创建+切换分支：`git checkout -b <name>`

合并某分支到当前分支：`git merge <name>`

删除分支：`git branch -d <name>`

删除Github：$ git push origin :xx //xx:为分支名字