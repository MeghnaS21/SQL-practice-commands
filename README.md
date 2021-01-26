**SQL COMMANDS FROM COMMAND PROMPT**

*cd command to change the directory*

C:\Windows\system32>cd../..

C:\>cd xampp/mysql/bin

C:\xampp\mysql\bin>mysql -u root -p -h localhost

**HOW TO SHOW DATABASES**

MariaDB [(none)]> show databases;

**How to create database with particular name**

MariaDB [(none)]> create database youtubestu;

**HOW TO DELETE ANY DATABASES**

MariaDB [(none)]> DROP database youtubestu;

**HOW TO CHANGE DATABASES**
MariaDB [(none)]> use youtubestu;
Database changed

**HOW TO SELECT DATABASES**
MariaDB [youtubestu]> select database();


**HOW TO CREATE TABLE STUDENTS(TABLE NAME)**

MariaDB [youtubestu]> create table students
    -> (
    -> name varchar(55),
    -> age int
    -> );
**HOW TO DDESCRIBE A TABLE**

MariaDB [youtubestu]> desc students

**HOW TO SHOW COLUMNS OF TABLE**

MariaDB [youtubestu]> show columns from studentsdemo;

**HOW TO DELETE A TABLE FROM DATABASE**

MariaDB [youtubestu]> drop table studentsdemo;

**HOW TO SHOW TABLES**

MariaDB [youtubestu]> show tables;

**HOW TO INSERT INTO A TABLE**

MariaDB [youtubestu]> insert into studentdiff
    -> (id, name, class)
    -> values(1, 'vinod' , 5);
Query OK, 1 row affected (0.150 sec)

**HOW TO SHOW THE TABLE**

MariaDB [youtubestu]> select * from studentdiff;


**WHAT IS NOT NULL DATA IN TABLE**
*NULLmeans that the value is not known of a field

MariaDB [youtubestu]> create table stunull
    -> (
    -> id int not null,
    -> name varchar(55) not null
    -> );
Query OK, 0 rows affected (0.391 sec)


**HOW TO SET DEFAULT VALUES IN THE TABLE**
MariaDB [youtubestu]> create table studef
    -> (
    -> id int not null default 0,
    -> name varchar(55) not null default 'unnamed'
    -> );
Query OK, 0 rows affected (0.465 sec)

**HOW TO NEW FIELD IN TEH TABLE

MariaDB [youtubestu]> insert into studef() values ();
Query OK, 1 row affected (0.045 sec)

**HOW TO NEW FIELD IN THE TABLE BY USING ALTER TABLE**

MariaDB [youtubestu]> alter table studef ADD class int;

**WHAT IS PRIMARY KEY IN THE TABLE**

MariaDB [youtubestu]> CREATE TABLE stud_unique
    -> (
    -> stud_id INT NOT NULL,
    -> name VARCHAR(55),
    -> age INT,
    -> PRIMARY KEY (stud_id)
    -> );

**HOW TO AUTO INCREMENT IN THE TABLE**

MariaDB [youtubestu]> CREATE TABLE stud_auto
    -> (
    -> stud_id INT NOT NULL AUTO_INCREMENT,
    -> name VARCHAR(100),
    -> age INT,
    -> PRIMARY KEY (stud_id)
    -> );
