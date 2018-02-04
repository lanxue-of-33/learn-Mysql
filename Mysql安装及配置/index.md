### Mysql的安装及ini文件配置

---
#### 下载的具体步骤见如下链接
[mysql 5.7.19下载步骤](http://www.jb51.net/article/119369.htm?utm_source=debugrun&utm_medium=referral)
[mysql 5.7.20下载步骤]()

---
#### 步骤总结如下
1. 下载好Mysql，并安装再自己指定的文件处。
2. 配置系统变量，快捷打开方式为：`sysdm.cpl`
3. 配置好后，cd到安装的文件的bin目录下，运行命令:`mysqld.exe -install`,存在了的话执行移除命令。
4. 5.7版本的mysql没有给了.ini配置文件和data文件夹，此时我们应该先运行命名：`mysqld --initialize-insecure --user=mysql`，表示初始化MySQL数据，并创建一个具有空密码的root用户
5. 初始化完后，新建.ini文件，保存到\bin文件夹下
  *ini文件
  ```.ini文件
  [mysql] 
  # 设置mysql客户端默认字符集 
  default-character-set=utf8  
  [mysqld] 
  #设置3306端口 
  port = 3306  
  # 设置mysql的安装目录 
  basedir=E:\Program Files\mysql-5.7.20-winx64 
  # 设置mysql数据库的数据的存放目录 
  datadir=E:\Program Files\mysql-5.7.20-winx64\data 
  # 允许最大连接数 
  max_connections=200 
  # 服务端使用的字符集默认为8比特编码的latin1字符集 
  character-set-server=utf8 
  # 创建新表时将使用的默认存储引擎 
  default-storage-engine=INNODB
  ```
6. 启动服务：`net mysql`
7. 登陆：`mysql -u root -p` 因为没有密码，所以直接按回车键就行。
---

#### 出现的问题
1. 删除残存的MySQL：`mysqld -remove`
