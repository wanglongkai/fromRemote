# fromRemote
git相关操作记录    
    

## 本地git仓库关联到远程步骤
1. 将本地项目初始化为git仓库
	1. git init
2. 远程新建repository
3. 正式进行关联和推送
	1. 关联远程库： git remote add origin git@server-name:path/repo-name.git
	2. 推送本地仓库内容 ：git push -u origin master
