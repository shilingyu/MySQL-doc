## Apache安装
* sudo apt-get update
* sudo apt-grt install tasksel
* sudo tasksel
## Apache开启CGI
1. 在Apache中开启CGI支持：sudo ln -s /etc/apache2/mods-available/cgi.load 
1. 重启Apache服务器：service apache2 restart
1. CGI文件存放路径：/usr/lib/cgi-bin
1. 更改目录权限，方便对目录下的文件写：
  * sudo mkdir /usr/lib/cgi-bin/文件名
   * sudo chmod 777 /usr/lib/cgi-bin/文件名
1. 安装MySQL的C语言库
   * sudo apt-get update
   * sudo apt-get install libmysqlclient-dev
