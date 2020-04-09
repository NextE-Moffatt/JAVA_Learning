### DDL  操作数据库、表

 1.  操作数据库：CRUD

     * C：create  创建
     * R：retrieve  查询
     * U：update   修改
       * alter 
     * D：delete   删除
       * drop

	2. 使用数据库

    * 查询正在使用的数据库的名称

         select database（）

    * 使用某个数据库

      ​     use  +  数据库名

	3. 操作表

    * C: 创建   

      ​      create   table   + 表名{

      ​          列名   数据类型1，

      ​          列名   数据类型2，

      ​                   ...

      ​      }

    * R：查询

    ​            desc +表名
    
     *  U：修改
    
        ​      ```alter table 表名  rename  to```
    
        ​	   ``` alter   table    表名     character   set   utf8```
    
    * D:  删除
    
      ​	  ```drop  table   表名```

### DML ：增删改表中数据

  *   **添加数据**

       	* 语法：

      ​        * insert  into   表名（列名1，列名2，。。。列名n）

### 约束

   1. 主键约束     Primary key

      *  自动增长    **auto_increment 可以来完成值得自动增长

   2. 非空约束     not null

   3. 唯一约束      unique

   4. 外键约束      foreign  key

         * 在创建表时可以添加外键：

           ​       create  table   表名{

           ​              ....

           ​          外键列

           ​          constraint   外键名称  foreign  key   （外键列名称）    reference   主表名称（主列表名称）

           ​        };

      * 删除外键

      * 级联操作

        ​          on  update    cascade

        ​          on   delete    cascade

---



## 数据库的设计

* **多表之间的关系**

   1. 一对一

      添加外键或相同主键或是合成一张表

   2. 一对多

   3. 多对多

​           需要添加中间表

* **数据库设计的范式**
  * 在设计数据库时需要遵循的规范
  * 第一范式：每一列都是不可分割对的原子数据列。（**去除冗余**）
  * 第二范式：在1NF的基础上，非码属性必须完全依赖于候选码。（**消除部分依赖**）
  * 第三范式：在1NF、2NF的基础上，任何非主属性不依赖于其他非主属性。（**消除传递依赖**）

---

## 多表查询

### 1. 查询语法

​              select   

​                       列名列表

​               from

​                       表名列表

​               where

​                       条件语句

### 2. 分类

   * 内连接

           1. 隐式内连接
              2. 显式内连接

   * 外连接

         1.  左外连接
            2.  右外连接

   * 子查询

     **查询中嵌套查询**

---

## 分类

1. 事务的基本介绍
   * 如果一个包含多个步骤的业务操作，被事务管理，那么要么这些操作同时失败
   * 操作
     1. 开启事务：start  transaction
     2. 回滚：rollback
     3. 提交：commit
2. 事务的四大特征
   1. **原子性**
   2. **持久性**
   3. **隔离性**
   4. **一致性**

## DCL:管理用户

## DQL: 查询表中数据

