## Apache安装
* sudo apt-get update
* sudo apt-grt install tasksel
* sudo tasksel
## 安装编辑器atom
1. 搜索atom，将atom-amd64.deb的链接复制
1. 在命令行执行：waget -c 链接地址，进行下载
1. 执行sudo dpkg -i atom-amd64.deb命令
## Apache开启CGI
1. 在Apache中开启CGI支持：sudo ln -s /etc/apache2/mods-available/cgi.load 
1. 重启Apache服务器：service apache2 restart
1. CGI文件存放路径：/usr/lib/cgi-bin
1. 更改目录权限，方便对目录下的文件写：
* sudo mkdir /usr/lib/cgi-bin/文件名
* sudo chmod 777 /usr/lib/cgi-bin/文件名
## 安装MySQL的C语言库
* sudo apt-get update
* sudo apt-get install libmysqlclient-dev
