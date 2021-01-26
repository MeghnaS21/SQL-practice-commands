# SQL-practice-commands
SQL Practice Commands. Copied from command prompt.

//==================================================================================
Microsoft Windows [Version 10.0.18362.900]
(c) 2019 Microsoft Corporation. All rights reserved.

//==========================================cd command to change the directory============

C:\Windows\system32>cd../..

C:\>cd xampp/mysql/bin

C:\xampp\mysql\bin>mysql -u root -p -h localhost
Enter password:
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 8
Server version: 10.4.17-MariaDB mariadb.org binary distribution

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.


MariaDB [(none)]> show databases
    -> Bye
Ctrl-C -- exit!

C:\xampp\mysql\bin>mysql -u root -p -h localhost
Enter password:
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 23
Server version: 10.4.17-MariaDB mariadb.org binary distribution

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

//==================================HOW TO SHOW DATABASES===========

MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| chatroom           |
| information_schema |
| mysql              |
| performance_schema |
| phpmyadmin         |
| phptute            |
| test               |
+--------------------+
7 rows in set (0.001 sec)

//================================how to create database with particular name========================

MariaDB [(none)]> create database youtubestu;
Query OK, 1 row affected (0.003 sec)

MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| chatroom           |
| information_schema |
| mysql              |
| performance_schema |
| phpmyadmin         |
| phptute            |
| test               |
| youtubestu         |
+--------------------+
8 rows in set (0.002 sec)

//==================================HOW TO DELETE ANY DATABASES===========

MariaDB [(none)]> DROP database youtubestu;
Query OK, 0 rows affected (0.076 sec)

MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| chatroom           |
| information_schema |
| mysql              |
| performance_schema |
| phpmyadmin         |
| phptute            |
| test               |
+--------------------+
7 rows in set (0.001 sec)

MariaDB [(none)]> create database youtubestu;
Query OK, 1 row affected (0.001 sec)

//==================================HOW TO CHANGE DATABASES===========
MariaDB [(none)]> use youtubestu;
Database changed

//==================================HOW TO SELECT DATABASES===========
MariaDB [youtubestu]> select database();
+------------+
| database() |
+------------+
| youtubestu |
+------------+
1 row in set (0.000 sec)

//==================================HOW TO CREATE TABLE STUDENTS(TABLE NAME)===========

MariaDB [youtubestu]> create table students
    -> (
    -> name varchar(55),
    -> age int
    -> );
Query OK, 0 rows affected (0.499 sec)

MariaDB [youtubestu]> show tables;
+----------------------+
| Tables_in_youtubestu |
+----------------------+
| students             |
| studentsdemo         |
+----------------------+
2 rows in set (0.001 sec)

//===================================================HOW TO DDESCRIBE A TABLE==================================

MariaDB [youtubestu]> desc students
    -> desc students;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'desc students' at line 2
MariaDB [youtubestu]> desc students;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| name  | varchar(55) | YES  |     | NULL    |       |
| age   | int(11)     | YES  |     | NULL    |       |
+-------+-------------+------+-----+---------+-------+
2 rows in set (0.004 sec)

//==================================HOW TO SHOW COLUMNS OF TABLE================================

MariaDB [youtubestu]> show columns from studentsdemo;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| name  | varchar(55) | NO   |     | NULL    |       |
| age   | int(11)     | NO   |     | NULL    |       |
+-------+-------------+------+-----+---------+-------+
2 rows in set (0.004 sec)

//==================================HOW TO DELETE A TABLE FROM DATABASE=========================

MariaDB [youtubestu]> drop table studentsdemo;
Query OK, 0 rows affected (1.423 sec)

//==================================HOW=========== TO======== SHOW======= TABLES========================================

MariaDB [youtubestu]> show tables;
+----------------------+
| Tables_in_youtubestu |
+----------------------+
| students             |
+----------------------+
1 row in set (0.001 sec)

MariaDB [youtubestu]> create table students(
    -> id int,
    -> name varchar(55),
    -> class int
    -> );
ERROR 1050 (42S01): Table 'students' already exists
MariaDB [youtubestu]> create table studentdiff(
    -> id int,
    -> name varchar(55),
    -> class int
    -> );
Query OK, 0 rows affected (0.296 sec)

MariaDB [youtubestu]> desc studentdiff;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| id    | int(11)     | YES  |     | NULL    |       |
| name  | varchar(55) | YES  |     | NULL    |       |
| class | int(11)     | YES  |     | NULL    |       |
+-------+-------------+------+-----+---------+-------+
3 rows in set (0.004 sec)

//==================================HOW TO INSERT INTO A TABLE======================

MariaDB [youtubestu]> insert into studentdiff
    -> (id, name, class)
    -> values(1, 'vinod' , 5);
Query OK, 1 row affected (0.150 sec)

//==================================HOW TO SHOW THE TABLE========================

MariaDB [youtubestu]> select * from studentdiff;
+------+-------+-------+
| id   | name  | class |
+------+-------+-------+
|    1 | vinod |     5 |
+------+-------+-------+
1 row in set (0.001 sec)

MariaDB [youtubestu]> insert into students(id, name, class)
    -> v
    -> v;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'v
v' at line 2
MariaDB [youtubestu]> show warnings;
+-------+------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| Level | Code | Message                                                                                                                                                 |
+-------+------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| Error | 1064 | You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'v
v' at line 2 |
+-------+------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
1 row in set (0.000 sec)

MariaDB [youtubestu]> desc studentdiff;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| id    | int(11)     | YES  |     | NULL    |       |
| name  | varchar(55) | YES  |     | NULL    |       |
| class | int(11)     | YES  |     | NULL    |       |
+-------+-------------+------+-----+---------+-------+
3 rows in set (0.062 sec)

MariaDB [youtubestu]> select * from studentdiff;
+------+-------+-------+
| id   | name  | class |
+------+-------+-------+
|    1 | vinod |     5 |
+------+-------+-------+
1 row in set (0.000 sec)

//=================================WHAT IS NOT NULL DATA IN TABLE=======================
//NULL--------------- means that the value is not known of a field==========================

MariaDB [youtubestu]> create table stunull
    -> (
    -> id int not null,
    -> name varchar(55) not null
    -> );
Query OK, 0 rows affected (0.391 sec)

MariaDB [youtubestu]> desc stunull;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| id    | int(11)     | NO   |     | NULL    |       |
| name  | varchar(55) | NO   |     | NULL    |       |
+-------+-------------+------+-----+---------+-------+
2 rows in set (0.005 sec)

MariaDB [youtubestu]> select * from stunull;
Empty set (0.001 sec)

MariaDB [youtubestu]> desc stunull;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| id    | int(11)     | NO   |     | NULL    |       |
| name  | varchar(55) | NO   |     | NULL    |       |
+-------+-------------+------+-----+---------+-------+
2 rows in set (0.078 sec)

//==================================HOW TO SET DEFAULT VALUES IN THE TABLE=================
MariaDB [youtubestu]> create table studef
    -> (
    -> id int not null default 0,
    -> name varchar(55) not null default 'unnamed'
    -> );
Query OK, 0 rows affected (0.465 sec)

MariaDB [youtubestu]> desc studef;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| id    | int(11)     | NO   |     | 0       |       |
| name  | varchar(55) | NO   |     | unnamed |       |
+-------+-------------+------+-----+---------+-------+
2 rows in set (0.005 sec)

//==================================HOW TO NEW FIELD IN TEH TABLE==========================

MariaDB [youtubestu]> insert into studef() values ();
Query OK, 1 row affected (0.045 sec)

MariaDB [youtubestu]> select * from studef;
+----+---------+
| id | name    |
+----+---------+
|  0 | unnamed |
+----+---------+
1 row in set (0.000 sec)

// //==================================HOW TO NEW FIELD IN THE TABLE BY USING ALTER TABLE===========

MariaDB [youtubestu]> alter table studef ADD class int;
Query OK, 0 rows affected (0.281 sec)
Records: 0  Duplicates: 0  Warnings: 0

MariaDB [youtubestu]> desc studef;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| id    | int(11)     | NO   |     | 0       |       |
| name  | varchar(55) | NO   |     | unnamed |       |
| class | int(11)     | YES  |     | NULL    |       |
+-------+-------------+------+-----+---------+-------+
3 rows in set (0.004 sec)

MariaDB [youtubestu]> alter table studef DROP COLUMN class;
Query OK, 0 rows affected (0.197 sec)
Records: 0  Duplicates: 0  Warnings: 0

//===============================================WHAT IS PRIMARY KEY IN THE TABLE=====================

MariaDB [youtubestu]> CREATE TABLE stud_unique
    -> (
    -> stud_id INT NOT NULL,
    -> name VARCHAR(55),
    -> age INT,
    -> PRIMARY KEY (stud_id)
    -> );
Query OK, 0 rows affected (0.409 sec)

MariaDB [youtubestu]> desc stud_unique;
+---------+-------------+------+-----+---------+-------+
| Field   | Type        | Null | Key | Default | Extra |
+---------+-------------+------+-----+---------+-------+
| stud_id | int(11)     | NO   | PRI | NULL    |       |
| name    | varchar(55) | YES  |     | NULL    |       |
| age     | int(11)     | YES  |     | NULL    |       |
+---------+-------------+------+-----+---------+-------+
3 rows in set (0.039 sec)

MariaDB [youtubestu]> insert into stud_unique
    -> (
    -> stud_id, name, age)
    -> values(1, 'vinod', 25);
Query OK, 1 row affected (0.137 sec)

MariaDB [youtubestu]> select * from stud_unique;
+---------+-------+------+
| stud_id | name  | age  |
+---------+-------+------+
|       1 | vinod |   25 |
+---------+-------+------+
1 row in set (0.000 sec)

MariaDB [youtubestu]> insert into stud_unique(stud_id, name, age)
    -> values(2, 'meghnasrivastava', 25);
Query OK, 1 row affected (0.128 sec)

MariaDB [youtubestu]> select * from stud_unique;
+---------+------------------+------+
| stud_id | name             | age  |
+---------+------------------+------+
|       1 | vinod            |   25 |
|       2 | meghnasrivastava |   25 |
+---------+------------------+------+
2 rows in set (0.000 sec)

MariaDB [youtubestu]> insert into stud_unique;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near '' at line 1
MariaDB [youtubestu]> select * from stud_unique;
+---------+------------------+------+
| stud_id | name             | age  |
+---------+------------------+------+
|       1 | vinod            |   25 |
|       2 | meghnasrivastava |   25 |
+---------+------------------+------+
2 rows in set (0.001 sec)

MariaDB [youtubestu]>
MariaDB [youtubestu]>
MariaDB [youtubestu]>
MariaDB [youtubestu]>
MariaDB [youtubestu]>
MariaDB [youtubestu]>
//==============================================HOW TO AUTO INCREMENT IN THE TABLE=====================================
MariaDB [youtubestu]>
MariaDB [youtubestu]> CREATE TABLE stud_auto
    -> (
    -> stud_id INT NOT NULL AUTO_INCREMENT,
    -> name VARCHAR(100),
    -> age INT,
    -> PRIMARY KEY (stud_id)
    -> );
Query OK, 0 rows affected (0.347 sec)

MariaDB [youtubestu]> desc stud_auto;
+---------+--------------+------+-----+---------+----------------+
| Field   | Type         | Null | Key | Default | Extra          |
+---------+--------------+------+-----+---------+----------------+
| stud_id | int(11)      | NO   | PRI | NULL    | auto_increment |
| name    | varchar(100) | YES  |     | NULL    |                |
| age     | int(11)      | YES  |     | NULL    |                |
+---------+--------------+------+-----+---------+----------------+
3 rows in set (0.009 sec)

MariaDB [youtubestu]> insert into stud_auto(name, age) values('vinod', 25);
Query OK, 1 row affected (0.117 sec)

MariaDB [youtubestu]> insert into stud_auto(name, age) values('megs', 26);
Query OK, 1 row affected (0.116 sec)

MariaDB [youtubestu]> insert into stude_auto(name, age) values('srivastava', 6);
ERROR 1146 (42S02): Table 'youtubestu.stude_auto' doesn't exist
MariaDB [youtubestu]> insert into stud_auto(name, age) values('srivastava', 26);
Query OK, 1 row affected (0.133 sec)

MariaDB [youtubestu]> select * from stud_auto;
+---------+------------+------+
| stud_id | name       | age  |
+---------+------------+------+
|       1 | vinod      |   25 |
|       2 | megs       |   26 |
|       3 | srivastava |   26 |
+---------+------------+------+
3 rows in set (0.000 sec)

MariaDB [youtubestu]>

