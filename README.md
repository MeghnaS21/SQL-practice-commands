**SQL COMMANDS FROM COMMAND PROMPT**

*cd command to change the directory*

cd../..

C:\>cd xampp/mysql/bin

C:\xampp\mysql\bin>mysql -u root -p -h localhost

**HOW TO SHOW DATABASES**

_show databases;_

**How to create database with particular name**

_create database youtubestu;_

**HOW TO DELETE ANY DATABASES**

_DROP database youtubestu;_

**HOW TO CHANGE DATABASES**

_use youtubestu;_


**HOW TO SELECT DATABASES**
_select database();_


**HOW TO CREATE TABLE STUDENTS(TABLE NAME)**

_create table students_
    -> (
    -> name varchar(55),
    -> age int
    -> );
**HOW TO DDESCRIBE A TABLE**

_desc students_

**HOW TO SHOW COLUMNS OF TABLE**

_show columns from studentsdemo;_

**HOW TO DELETE A TABLE FROM DATABASE**

_drop table studentsdemo;_

**HOW TO SHOW TABLES**

_show tables;_

**HOW TO INSERT INTO A TABLE**

_insert into studentdiff_
    -> (id, name, class)
    -> values(1, 'vinod' , 5);


**HOW TO SHOW THE TABLE**

_select * from studentdiff;_


**WHAT IS NOT NULL DATA IN TABLE**
_NULLmeans that the value is not known of a field_

_create table stunull_
    -> (
    -> id int not null,
    -> name varchar(55) not null
    -> );

**HOW TO SET DEFAULT VALUES IN THE TABLE**
_create table studef_
    -> (
    -> id int not null default 0,
    -> name varchar(55) not null default 'unnamed'
    -> );


**HOW TO NEW FIELD IN TEH TABLE

_insert into studef() values ();_
_Query OK, 1 row affected (0.045 sec)_

**HOW TO NEW FIELD IN THE TABLE BY USING ALTER TABLE**

_alter table studef ADD class int;_

**WHAT IS PRIMARY KEY IN THE TABLE**

_CREATE TABLE stud_unique_
    -> (
    -> stud_id INT NOT NULL,
    -> name VARCHAR(55),
    -> age INT,
    -> PRIMARY KEY (stud_id)
    -> );

**HOW TO AUTO INCREMENT IN THE TABLE**

_CREATE TABLE stud_auto_
    -> (
    -> stud_id INT NOT NULL AUTO_INCREMENT,
    -> name VARCHAR(100),
    -> age INT,
    -> PRIMARY KEY (stud_id)
    -> );
