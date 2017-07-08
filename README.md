# This repository is created for practicing git
***

##文件操作
本地仓库 -- 暂存区 -- 远程仓库

- 查看本地文件：

		输入 ls

- 删除本地文件：

		输入 rm 文件名

- 查看缓存区文件：

		输入 git ls-files

- 删除缓存区文件：

		输入 git rm 文件名

- 在根目录或者任何子目录中都可创建忽略文件：

		输入 touch .gitignore

	编辑文件（Git忽略语法），每个要忽略的文件占一行，如：

		*.o
		code2.c
		.gitignore（忽略自己）

- 文件归档：

		git archive

	基于最新提交建立归档文件：

		输入 git archive -o file.zip HEAD

	只将部分文件(src,doc)建立到归档文件：

		输入 git archive -o file.zip HEAD src doc
	...

##常用命令

创建一个空文件夹files

- 将该文件夹初始为git仓库：

		输入 git init

- 添加远程仓库地址：

		输入 git remote add origin https://git.oschina.net/hustrenesaslab/Baby_Pro.git

- 修改远程仓库地址：

		1.输入 git remote set-url origin [url]
		2.修改./git/config
		3.先删除后添加 git remote rm origin; git remote add origin [url]

- 拉取master分支下的文件：

		输入 git pull origin master

	注意：git pull = git fetch + git merge
	多个开发者对同一文件的同一区域做了不同修改时，产生冲突将导致pull失败
		
		输入 git ls-files -s
	
	发生合并冲突的文件会显示大于0的暂存区编号，意为暂存区存在多个版本
	编号为1的文件为冲突文件的父版本，其他为冲突子版本

	可通过手工编辑或者图形化冲突解决工具解决冲突，重新提交

		输入 git mergetool

- 添加文件到暂存区（*表示添加所有文件）：

		输入 git add */文件名

- 交互式添加文件到暂存区：

		输入 git add -i

- 提交：

		输入 git commit -m "注释"

- 修改提交：

		输入 git commit --amend -m "注释"

- 允许空提交：

		输入 git commit --allow-empty -m "注释"

- 查看提交记录：

		输入 git log [--stat（查看文件变更信息）--oneline（简易显示）]

- 文件修改后，查看差异输出：

		输入 git diff [文件名]

- 撤销未提交的修改（*表示撤销所有文件的修改）：

		输入 git checkout */文件名

- 保存当前进度：

		输入 git stash [save "注释说明"]

- 查看保存的进度：

		输入 git stash list

- 恢复保存的进度，继续之前的工作：

		输入 git stash apply/pop（恢复后自动删除此进度区）

- 删除保存的所有进度：

		输入 git stash clear

- 推送：

		输入 git push origin master

	注意单个文件不能大于100MB

- 查看分支：

		输入 git branch [-v] (查看本地分支)
		输入 git remote / branch -r (查看远程分支)

- 创建分支：

		输入 git branch 分支名 [起点]

- 切换分支：

		输入 git checkout 分支名

- 创建分支同时切换到该分支：

		输入 git checkout -b 分支名

	注意：创建分支后要 `git push origin 分支名` 才会在远程库生成分支 

- 创建本地分支映射到远程分支：

		输入 git checkout -b 本地分支名 origin/远程分支名

- 修改本地分支名称：

		输入 git branch -m 本地分支原名称 本地分支新名称

- 删除分支：
		
		输入 git branch -d/D 分支名（只是删除本地分支名）
		输入 git push origin :分支名 或者
		     git push origin --delete 分支名(删除远程分支)

- 合并分支：
		
		先切换到目的分支，再
		输入 git merge 源分支

	注意：要 `git push origin 目的分支` 才会在远程库更新合并后的目的分支

- 创建附注标签：

		输入 git tag -a v0.0 -m "最初版本"

- 查看标签：

		输入 git tag（查看当前分支下的标签）
		输入 git show 标签名（查看某个标签的详细信息）
		输入 git ls-remote --tags (查看远程分支)

- 删除标签：

		输入 git tag -d 标签名 (删除本地标签)
		输入 git push origin :标签名 (删除远程标签)

- 标签发布：
		
		输入 git push origin 标签名
		输入 git push origin --tags（一次性提交所有标签）

- 暂存区重置，本地库内容不受影响：

		输入 git reset --soft 提交ID

- 本地库重置，即修改游标（慎用！此提交ID之后的数据再被彻底丢弃）：

		输入 git reset --hard 提交ID

	重置之后，提交记录也被修改，git log已经查看不到此提交ID之后的信息

	如何挽救错误的重置？查看.git/logs/refs/heads/master，记录了所有指向的变化。使用git reflog操作该文件：

  	查看文件内容：

		输入 git reflog show master [| head -5（只显示前5条）]

	重置master：

		输入 git reset --hard <refname@{<n>}>

		<refname@{<n>}>为提交ID的简易符，例如：master@{2}

##图形化工具

Git自带的工具

- 浏览版本库：

		输入 gitk

- 版本库操作：

		输入 git gui 或者 git citool

需自行安装的工具

- 版本库浏览+操作 gitg、qgit：

		输入 sudo aptitude install gitg/qgit 安装(linux)
		输入 gitg/qgit & 启动

##Git管理工具

Git自带的工具

- 版本库清理、优化：

		输入 git gc

	按需自动执行优化：

		输入 git gc --auto

##常见错误

- git status [-s（精简格式输出）]

		stderr: error: bad signature
		fatal: index file corrupt

		输入 rm -f .git/index
		    git reset

重启后，重新add，commit，push

***
Author : ZuoJiawei XiangcaiHuang
Date   : July 8,2017
