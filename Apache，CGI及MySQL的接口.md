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
## CGI基本使用
### 获取表单数据
```c
cgiFormResultType   cgiFormString(char *name, char *result, int max);
参数：  name, 指定要获取的表单项的名字
       result,将获得的数据存储到result中
       max， 指定最多读取的字符个数
```
### atoi函数
```c
int atoi(const char *nptr);
功能：将一个字符串转换成对应的数字，比如：“1234” ==》 1234
```
### fprintf函数
``` c
int fprintf(FILE *stream, const char *format, ...);
功能： 将格式化的语句输出到指定的流
fprintf(stdin, "helloworld\n")  
等价于 printf("helloworld\n);
```
### 接口介绍
```c
MYSQL *mysql_init(MYSQL *mysql)
功能：初始化函数，参数为NULL即可，接收返回值。
失败，NULL
```

```c
MYSQL *mysql_real_connect(MYSQL *mysql, const char *host, const char *user, const char *passwd, const char *db, unsigned int port, const char *unix_socket, unsigned long client_flag)
功能：连接mysql服务器
失败，NULL
```

```c
void mysql_close(MYSQL *mysql)
功能：关闭服务器连接
```

```c
int mysql_real_query(MYSQL *mysql, const char *stmt_str, unsigned long length)
功能：执行sql语句，sql语句不能以“；”结尾
成功，0
失败， 非0
```

```c
int mysql_query(MYSQL *mysql, const char *stmt_str)
功能：执行sql语句，sql语句不能以“；”结尾
```

```c
void mysql_free_result(MYSQL_RES *result)
//功能：释放空间
```
