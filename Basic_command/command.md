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
5. 修改表的结构
    * 语法：`alter table 数据表名 alter_specification[,alter_spec]···;`
    * 实例：`alter table tb_user add address varchar(60) not null,modify user varchar(50);`       
    表示添加一个新字段address,并将字段user的varchar改为50;
6. 重命名数据表
    * 语法：`rename table 数据表名1 to 数据表名2;`   实例：`rename table tb_user to my_user;`
7. 删除数据表
    * `drop table 数据表名;`
    * 删除不知道存不存在的表时：`drop table if exits 数据表名;`    

---
#### 数据表记录的更新操作
##### 我们操作数据库，真正要操作的其实是数据表中的数据

