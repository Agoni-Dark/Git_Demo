参考笔记

```txt
https://github.com/liuqingg/GIt-GitHub_Note/blob/master/Git%E6%93%8D%E4%BD%9C.md#16-rebase
//IDEA整合git完成代码提交到远程仓库
https://blog.csdn.net/weixin_47632717/article/details/109717526
//从前慢-git以及github的使用
https://blog.csdn.net/unique_perfect/article/details/104833391
```

#### Git

###### Git介绍 分布式版本控制工具  VS   集中式版本控制工具

###### Git安装 

```text
https://git-scm.com/    直接官网下载，然后默认安装即可

建议软件装在ProgramFiles  这个是没有空格，64位。带x86的是32位系统
```

###### **<u>Git常用命令</u>**

```text
Git Base Here  git的命令工具窗口
git --version	查看git版本
git config --global user.name 用户名	设置用户签名为Junc
git config --golbal user.email邮箱	 设置用户邮箱为Junclink@Gmail.com
      -----设置完后在当前用户下有个.gitconfig文件可以查看-----
git init							  初始化本地库
	  ---（在文件夹里面使用Git Base Here打开，输入命令），初始化的文件是隐藏的
git status							  查看本地库状态
	  ---（初始化后就能使用git status查看状态了）
git add文件名							 添加到暂存区
	  ---（使用git add 文件名，将文件添加到暂存区）这个时候文件只是保存在暂存区，是可以删除的
	  ---（git rm --cached 文件名 可以删除暂存区里面的文件）
git commit-m"日志信息" 文件名			  提交到本地库
      ---（git commit -m "第一次提交" hello.txt       这也就将暂存区的文件提交到本地库了）
git reflog							  查看历史记录
git log								  查看详细日志（可以看到用户签名 日期以及当时日志注释）
	如果修改了文件，需要再次git add，然后再git commit -m "日志信息" 文件名
git reset --hard 版本号				版本穿梭
	并日志也会记录版本穿梭的记录
	
```

```text
linux 命令  在Git Base Here里面输入
ll      查看文件
ll -a   可以查看隐藏文件
ctrl + L 清屏

vim hello.txt     使用vim创建一个hello.txt，并打开文件进入一般模式
i    进入输入模式
esc  退出输入模式，回到一般模式
:wq  保存并退出
:q 是直接退出
cat 文件名    是直接查看文件类容
tail -n 1 文件名     查看文件最后一行是啥

```



###### Git分支 分支特性、分支创建、分支转换、分支合并、代码合并冲突解决

```text
git branch 分支名			创建分支
	---(git branch hot-fix  创建一个hot-fix的分支)
git branch -v			  查看分支
git checkout 分支名		切换分支
	---( git checkout hot-fix 切换到hot-fix的分支上)
git merge 分支名			把指定的分支合并到当前分支上
	--(首先先回到主分支上，然后合并hot-fixs分支上的内容 git merge hot-fix就行了)
	
	
	代码冲突合并问题解决 
	直接git merge (需要被合并的分支) 
	如果是同一行需要vim 文件名 进去手动合并 
	合并完走 add 和 commit 流程  注（代码冲突的这次commit 不需要写文件名
									直接git commit -m "注释"）
```



###### Idea集成Git



#### GitHub

###### 创建运程仓库

```txt
登录GitHub账号，右上角+号，点击Create a New Repository，一般来讲远程仓库和本地仓库是同名
Repository name 填入仓库名字
直接Create repository就行
实例：https://github.com/Agoni-Dark/Git_Demo.git
```

```txt
创建远程仓库别名 ( 基于Git Base Here  git的命令工具窗口 )
git remote -v	查看当前所有远程地址别名
git remote add 别名 远程地址
		---git remote add Git-Demo https://github.com/Agoni-Dark/Git_Demo.git
git push 别名 分支		推送本地分支上的内容到远程仓库
		---git push Git-Demo(直接放连接也行) master
git clone 远程地址		将远程仓库内容克隆到本地
		---git clone https://github.com/Agoni-Dark/Git_Demo.git
		---克隆代码不需要账号，而且克隆会1.拉取代码 2.初始化本地仓库 3.创建别名
git pull 远程仓库地址别名 远程分支名			将远程仓库对于分支最新内容拉下来后与当前本地分支直接合并
		---直接在线修改内容，然后下面写上注释。然后在本地git bash here
		---git pull Git-Demo master	pull拉取和push推送的命令都是一样的，都要写上远程厂库名 和分支名
```



###### 代码推送 Push

###### 代码拉取 Pull

###### 代码克隆 Clone

###### SSH免密登录

###### Idea集成GitHub



#### Gitee

###### 码云创建远程仓库

###### Idea集成Gitee

###### 码云连接GitHub进行代码的复制和迁移

#### GitLab

###### GitLab服务器的搭建和部署

###### Idea集成GitLab



