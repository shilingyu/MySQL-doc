## 安装git
1.	在命令模式下，执行如下命令安装分布式版本控制软件git，如图所示：
![安装git](https://github.com/shilingyu/MySQL-doc/blob/master/img/安装git.png)
### git基本命令：
*	git status：查看仓库
*	git add . ：监视改变的文件
*	git commit –a –m “提交的文件名”：将文件提交到本地仓库
*	git diff commitID1 commitID2：比较两个版本的不同
*	git remote add origin 远程仓库链接地址：将本地仓库添加到远程仓库
*	git push origin master：将本地仓库内容提交到远程仓库
*	git clone url：将git仓库的源码拉取到本地
*	git pull：将服务器的源码与本地源进行同步
### github的使用
1.	创建本地版本库及使用
  
  (1)	新建目录：mkdir 仓库名
    
  (2)	切换到该目录下，执行git init初始化仓库
  (3)	git status查看仓库目前状态
  (4)	将需要提交到本地的文件执行git add file
  (5)	提交文件状态，保存此次修改，执行命令：git commit 需要加此次提交的标题记录，保存退出
  (6)	如果是第一次提交需要配置用户信息及编辑器
  *	用户名：git config –global user.name
  *	邮箱：git config –global user.email
  *	编辑器：git config –global core.editor vim

