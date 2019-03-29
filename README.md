# fromRemote
git相关操作记录    
<br/><br/>   


## 本地git仓库关联到远程步骤
1. 将本地项目初始化为git仓库
	1. `git init`
2. 远程新建repository
3. 正式进行关联和推送
	1. 关联远程库： `git remote add origin git@server-name:path/repo-name.git`
	2. 推送本地仓库内容 ：`git push -u origin master`
<br/><br/>  


## 最基本操作
1. 工作目录--->暂存区 ：`git add .`
2. 暂存区  --->本地仓库 ： `git commit -m "some commit info"`
3. 本地仓库--->远程仓库 ： `git push origin 分支名`
**注意事项：** 
1. push到远程前要先pull远程数据
2. 若有冲突需先解决冲突
3. 然后再次提交(add和commit)
4. 最后push(如果push到master分支，可以简写为`git push`)  
<br/><br/>


## git pull命令
**作用**：取回远程仓库某个分支的更新，并与本地某个分支合并。    
**完整语法**：git pull 远程主机名 远程分支名:本地分支名    
**举例**：`git pull origin wlk:main`  &nbsp;&nbsp;&nbsp;&nbsp; 取回远程origin主机的wlk分支与本地的main分支合并。  
如果时git clone的项目：可以直接使用 `git pull origin`
<br/><br/>  


## 暂存区回退到工作区
`git reset HEAD <file>` 将file从暂存区回退到工作空间    
`git reset` 简写，回滚暂存区的所有添加  
<br/><br/>


## 取消本次修改(还没有进入暂存区的修改)
`git checkout -- <file>` 将工作空间的还没有add的修改取消掉
<br/><br/>


## 覆盖上次的commit
`git commit --amend -m "message"` 覆盖掉上一次的commit信息
<br/><br/>


## 回退到指定版本(commit-id)
回退到上一个版本：`git reset --hard HEAD^`    
回退到上三个版本：`git reset --hard HEAD^^^`    
回退到指定版本：`git reset --hard commit-id`    
**注意**    
1.版本回退时，若工作区和暂存区有未提交的修改，会被撤销掉。这点要**特别注意**    
2.若回退后，再想恢复，可用 `git reflog` 查看历史命令，找到相关commit-id，再次reset。 
<br/><br/>


## 分支操作