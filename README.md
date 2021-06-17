# SQL COMMANDS (with important theory)

## Query information_schema with SELECT

Information_schema is a meta-database that holds information about your current database. information_schema has multiple tables you can query with the known SELECT * FROM syntax:

    tables: information about all tables in your current database
    columns: information about all columns in all of the tables in your current database 


## SQL COMMANDS FROM COMMAND PROMPT

- **cd** command to change the directory

  > cd../..

  > cd xampp/mysql/bin

  > mysql -u root -p -h localhost

## HOW TO SHOW DATABASES

  > show databases;

## HOW TO CREATE DATABASE WITH PARTICULAR NAME

  > create database youtubestu;

## HOW TO DELETE ANY DATABASES

  > DROP database youtubestu;
  
## HOW TO CHANGE DATABASES

  > use youtubestu;


## HOW TO SELECT DATABASES
   
  > select database();


## HOW TO CREATE TABLE STUDENTS(TABLE NAME)

  > create table students <br>
    -> ( <br>
    -> name varchar(55), <br>
    -> age int <br>
    -> );
  
## HOW TO DESCRIBE A TABLE

   > desc students

## HOW TO SHOW COLUMNS OF TABLE

   > show columns from studentsdemo;

## HOW TO DELETE A TABLE FROM DATABASE

   > drop table studentsdemo;

## HOW TO SHOW TABLES

   > show tables;

## HOW TO INSERT INTO A TABLE

   > insert into studentdiff <br>
    -> (id, name, class) <br>
    -> values(1, 'vinod' , 5);


## HOW TO SHOW THE TABLE**

   > select * from studentdiff;


## WHAT IS NOT NULL DATA IN TABLE

   > NULLmeans that the value is not known of a field

   > create table stunull <br>
    -> ( <br>
    -> id int not null, <br>
    -> name varchar(55) not null <br>
    -> );

## HOW TO SET DEFAULT VALUES IN THE TABLE

   > create table studef <br>
    -> ( <br>
    -> id int not null default 0, <br>
    -> name varchar(55) not null default 'unnamed' <br>
    -> );


## HOW TO NEW FIELD IN TEH TABLE

   > insert into studef() values ();
_Query OK, 1 row affected (0.045 sec)_

## HOW TO NEW FIELD IN THE TABLE BY USING ALTER TABLE

   > alter table studef ADD class int;

## WHAT IS PRIMARY KEY IN THE TABLE

   > CREATE TABLE stud_unique <br>
    -> ( <br>
    -> stud_id INT NOT NULL, <br>
    -> name VARCHAR(55), <br>
    -> age INT, <br>
    -> PRIMARY KEY (stud_id) <br>
    -> );

## HOW TO AUTO INCREMENT IN THE TABLE

   > CREATE TABLE stud_auto_ <br>
    -> ( <br>
    -> stud_id INT NOT NULL AUTO_INCREMENT, <br>
    -> name VARC(100), <br>
    -> age INT, <br>
    -> PRIMARY KEY (stud_id) <br>
    -> );
