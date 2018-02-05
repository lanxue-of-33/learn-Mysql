### 这里记录的是一些基本的MySQL命令

---
#### 基础操作    
1. `show databases;`     
 选中数据库:`use 数据库名;`   选中数据库后才可以操作数据库中的所有对象       
 删除数据库：`drop database 数据库名;`   除非备份了数据库，否则删除的没有恢复的可能       
 创建数据库：`create database 数据库名;`      
2. `quit;`或`exit;`         
3. 创建表：`create table table_name(列名1 属性，列名2 属性···);`      
4. 查看表的结构
    * `show columns from 数据表名 from 数据库名;`  实例如： `show columns from tb_user from db_user;`          
    * `describe 简写成 desc` 格式有：`desc 数据表名` 或 `desc 数据表名 列名;` 
    实例有： `desc tb_user id;`

---
