# DBMS-EXP-7
mysql> create database data;
Query OK, 1 row affected (0.01 sec)

mysql> use data
Database changed
mysql> create table emp(empno int(3),ename varchar(10),department_no int(3),sal int(7));
Query OK, 0 rows affected, 3 warnings (0.02 sec)

mysql> desc emp;
+---------------+-------------+------+-----+---------+-------+
| Field         | Type        | Null | Key | Default | Extra |
+---------------+-------------+------+-----+---------+-------+
| empno         | int         | YES  |     | NULL    |       |
| ename         | varchar(10) | YES  |     | NULL    |       |
| department_no | int         | YES  |     | NULL    |       |
| sal           | int         | YES  |     | NULL    |       |
+---------------+-------------+------+-----+---------+-------+
4 rows in set (0.01 sec)

mysql> insert into emp values(1,"sara",567,50000),(2,"arun",568,40000),(3,"kavi",569,55000),(4,"kani",569,20000);
Query OK, 4 rows affected (0.01 sec)
Records: 4  Duplicates: 0  Warnings: 0

mysql> select * from emp;
+-------+-------+---------------+-------+
| empno | ename | department_no | sal   |
+-------+-------+---------------+-------+
|     1 | sara  |           567 | 50000 |
|     2 | arun  |           568 | 40000 |
|     3 | kavi  |           569 | 55000 |
|     4 | kani  |           569 | 20000 |
+-------+-------+---------------+-------+
4 rows in set (0.00 sec)

mysql> select avg(sal),COUNT(*) from emp;
+------------+----------+
| avg(sal)   | COUNT(*) |
+------------+----------+
| 41250.0000 |        4 |
+------------+----------+
1 row in set (0.00 sec)

mysql> select min(sal) from emp;
+----------+
| min(sal) |
+----------+
|    20000 |
+----------+
1 row in set (0.00 sec)

mysql> select max(sal) from emp;
+----------+
| max(sal) |
+----------+
|    55000 |
+----------+
1 row in set (0.00 sec)

mysql> select sum(sal) from emp;
+----------+
| sum(sal) |
+----------+
|   165000 |
+----------+
1 row in set (0.00 sec)

mysql> select count(*) from emp;
+----------+
| count(*) |
+----------+
|        4 |
+----------+
1 row in set (0.00 sec)

mysql> select distinct department_no from emp;
+---------------+
| department_no |
+---------------+
|           567 |
|           568 |
|           569 |
+---------------+
3 rows in set (0.00 sec)

mysql> select department_no,count(*) from emp group by department_no;
+---------------+----------+
| department_no | count(*) |
+---------------+----------+
|           567 |        1 |
|           568 |        1 |
|           569 |        2 |
+---------------+----------+
3 rows in set (0.00 sec)

mysql> create table student(std_id varchar(5),name varchar(10));
Query OK, 0 rows affected (0.02 sec)

mysql> desc student;
+--------+-------------+------+-----+---------+-------+
| Field  | Type        | Null | Key | Default | Extra |
+--------+-------------+------+-----+---------+-------+
| std_id | varchar(5)  | YES  |     | NULL    |       |
| name   | varchar(10) | YES  |     | NULL    |       |
+--------+-------------+------+-----+---------+-------+
2 rows in set (0.00 sec)

mysql>

mysql> create table mark(std_id varchar(5),total_mark int(3));
Query OK, 0 rows affected, 1 warning (0.02 sec)

mysql> desc mark;
+------------+------------+------+-----+---------+-------+
| Field      | Type       | Null | Key | Default | Extra |
+------------+------------+------+-----+---------+-------+
| std_id     | varchar(5) | YES  |     | NULL    |       |
| total_mark | int        | YES  |     | NULL    |       |
+------------+------------+------+-----+---------+-------+
2 rows in set (0.00 sec)

mysql> insert into mark values("01",89),("02",98),("03",97),("04",96);
Query OK, 4 rows affected (0.01 sec)
Records: 4  Duplicates: 0  Warnings: 0

mysql> select * from mark;
+--------+------------+
| std_id | total_mark |
+--------+------------+
| 01     |         89 |
| 02     |         98 |
| 03     |         97 |
| 04     |         96 |
+--------+------------+
4 rows in set (0.00 sec)

mysql> insert into student values("01","abi"),("02","havi"),("03","kavi"),("04","kani");
Query OK, 4 rows affected (0.01 sec)
Records: 4  Duplicates: 0  Warnings: 0

mysql> select * from student;
+--------+------+
| std_id | name |
+--------+------+
| 01     | abi  |
| 02     | havi |
| 03     | kavi |
| 04     | kani |
+--------+------+
4 rows in set (0.00 sec)

mysql> select * from student where std_id>02;
+--------+------+
| std_id | name |
+--------+------+
| 03     | kavi |
| 04     | kani |
+--------+------+
2 rows in set (0.00 sec)

mysql>
