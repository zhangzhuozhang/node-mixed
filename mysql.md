

### mysql
<span style="color:red">语句必须以；结束</span>

```
* 进入数据库
    mysql -u root -p
* 展示数据库
    show databases;
* 如果没有 test 数据库，创建 test 数据库
    create database test;
    show databases;
* 使用 test 数据库，否则操作的时候需要制定数据库的名字
    use test;
    在 test 数据库中创建一张表
    create table books (book_id INT, title TEXT, status INT);
    show tables;   // show tables from test;
* 显示表的信息
    describe books;
* 插入数据
    insert into books values(100, 'Heart of Darkness', 0);
    insert into books values(101, 'The Catcher of the Rye', 1);
    insert into books values(102, 'My Antonia', 0);
*查找数据
    select * from books;
    select * from books where status = 1
* 删除数据
    delete from 表明 where 条件;
* 查看表的细节
    show create table 表名；
* 解决表格中中文乱码情况
    结尾加上 CHARSET=utf8
```
***


