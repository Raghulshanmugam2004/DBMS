# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
### DATE : 07/11/2023
## AIM:
To create a student database and execute DDL queries using SQL.
## THEORY
### DDL (Data Definition Language)

* DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
* It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
* DDL is a set of SQL commands used to create, modify, and delete database structures but not data.
* These commands are normally not used by a general user, who should be accessing the database via an application.

 
### List of DDL commands: 
1. CREATE: This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
2. DROP: This command is used to delete objects from the database.
3. ALTER: This is used to alter the structure of the database.
4. TRUNCATE: This is used to remove all records from a table, including all spaces allocated for the records are removed.
5. RENAME: This is used to rename an object existing in the database.

## Query:
### 1) Create a database studentdb   
### SQL QUERY:
```
create database stu_db;
```
### output:
![Screenshot 2023-10-26 090023](https://github.com/KISHORE22001263/DBMS/assets/121484538/b4302b36-6019-47f5-9bcc-4bd2164ddee4)

### 2) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
```
create table student(reg int,NAME varchar(20),AGE int,ADDRESS varchar(50),PHONE_NO varchar(20),DEPT varchar(100));
```
### OUTPUT:
![Screenshot 2023-10-26 090109](https://github.com/KISHORE22001263/DBMS/assets/121484538/0269a442-f3ea-4663-bf72-7a11f6fb5b3a)

### 3) Alter the above student table by adding another attribute department

### SQL QUERY: 
```
alter table student add cgpa varchar(20);
```
### OUTPUT:
![Screenshot 2023-10-26 090205](https://github.com/KISHORE22001263/DBMS/assets/121484538/3190a476-fee0-4382-9983-4e35e7870c46)

### 5) Delete the student rows using truncate keyword

### SQL QUERY: 
```
truncate table student;
```
### OUTPUT:
 ![Screenshot 2023-10-26 091245](https://github.com/KISHORE22001263/DBMS/assets/121484538/3d8ef379-ae4b-4f21-be4c-4baf0044314b)
### 4) Drop the AGE table
 
### SQL QUERY: 
```
 alter table student drop AGE;
```
### OUTPUT:
![Screenshot 2023-10-26 090213](https://github.com/KISHORE22001263/DBMS/assets/121484538/4dd884da-4695-4a24-a534-36420f65a770)
## Result:
Thus the basic DDL commands in SQL are executed. 
