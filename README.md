# fromRemote
git相关操作记录    
    

## 本地git仓库关联到远程步骤
1. 将本地项目初始化为git仓库
	1. `git init`
2. 远程新建repository
3. 正式进行关联和推送
	1. 关联远程库： `git remote add origin git@server-name:path/repo-name.git`
	2. 推送本地仓库内容 ：`git push -u origin master`
    

## 最基本操作
1. 工作目录--->暂存区 ：`git add .`
2. 暂存区  --->本地仓库 ： `git commit -m "some commit info"`
3. 本地仓库--->远程仓库 ： `git push origin 分支名`
**注意事项：** 
1. push到远程前要先pull远程数据
2. 若有冲突需先解决冲突
3. 然后再次提交
4. 最后push