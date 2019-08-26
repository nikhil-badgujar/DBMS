Enter password: ****
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 8
Server version: 5.1.38-community MySQL Community Server (GPL)

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> create database work;
Query OK, 1 row affected (0.00 sec)

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| anuja              |
| bookworm           |
| bookwormpro        |
| data               |
| db                 |
| db1                |
| employee           |
| exam               |
| fleemantestdb      |
| functions          |
| gita               |
| hobman             |
| icon               |
| java               |
| lakika             |
| mydata             |
| mydb               |
| mydb07             |
| mydemo             |
| mysql              |
| nikhil             |
| nikkhil            |
| nikkkhil           |
| pg                 |
| prasanna           |
| product            |
| project1           |
| queries            |
| renuka             |
| sak_md             |
| samruddha          |
| sandesh            |
| suraj              |
| test               |
| test1              |
| usha               |
| vb                 |
| vehicledb          |
| vivek              |
| work               |
| works              |
+--------------------+
42 rows in set (0.01 sec)

mysql> use works;
Database changed
mysql> create table product
    -> (
    -> ProductID int,
    -> Name varchar(20)
    -> );
Query OK, 0 rows affected (0.06 sec)

mysql> insert into product values(1,'bikes');
Query OK, 1 row affected (0.03 sec)

mysql> insert into product values(2,'Acekories');
Query OK, 1 row affected (0.03 sec)

mysql> insert into product values,'');
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near ''')' at line 1
mysql> insert into product values(3,'Clothing');
Query OK, 1 row affected (0.01 sec)

mysql> insert into product values(4,'Components');
Query OK, 1 row affected (0.02 sec)

mysql> select *from product;
+-----------+------------+
| ProductID | Name       |
+-----------+------------+
|         1 | bikes      |
|         2 | Acekories  |
|         3 | Clothing   |
|         4 | Components |
+-----------+------------+
4 rows in set (0.00 sec)

mysql> update product
    -> set name='Accesories'
    -> where ProductID=2;
Query OK, 1 row affected (0.01 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> select *from product;
+-----------+------------+
| ProductID | Name       |
+-----------+------------+
|         1 | bikes      |
|         2 | Accesories |
|         3 | Clothing   |
|         4 | Components |
+-----------+------------+
4 rows in set (0.00 sec)

mysql> delete from product
    -> where name='Components';
Query OK, 1 row affected (0.01 sec)

mysql> select *from product;
+-----------+------------+
| ProductID | Name       |
+-----------+------------+
|         1 | bikes      |
|         2 | Accesories |
|         3 | Clothing   |
+-----------+------------+
3 rows in set (0.00 sec)

mysql> truncate table product;
Query OK, 0 rows affected (0.03 sec)

mysql> select *from product;
Empty set (0.00 sec)

mysql> drop table product;
Query OK, 0 rows affected (0.03 sec)

mysql> select *from product;
ERROR 1146 (42S02): Table 'works.product' doesn't exist
mysql>
