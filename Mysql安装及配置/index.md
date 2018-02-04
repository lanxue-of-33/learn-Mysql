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
6. 启动服务：`net mysql`
7. 登陆：`mysql -u root -p` 因为没有密码，所以直接按回车键就行。
8. 我们也可以不登陆，因为密码是空的，所以先进行密码设定：   
  `mysqladmin -u root -p password 此处输入新的密码`   
  `Enter password: 此处输入旧的密码` 因为一开始没有密码，所以直接按回车
---

#### 出现的问题
1. 删除残存的MySQL：`mysqld -remove`
2. 其实，自己当初捣鼓一下午的错误是因为自己的.ini文件配置错误造成的    
