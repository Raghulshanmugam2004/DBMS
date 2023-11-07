# EX 3 Data Manipulation Language (DML) Commands and built in functions in SQL
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## DML(Data Manipulation Language)
*  The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements.
*  It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.

## List of DML commands: 
1. INSERT: It is used to insert data into a table.
2. UPDATE: It is used to update existing data within a table.
3. DELETE: It is used to delete records from a database table.
4. SELECT: The SELECT command shows the records of the specified table.

## Create the table as given below:
```sql
create table manager(enumber number(6),ename char(15),salary number(5),commission number(4),annualsalary number(7),Hiredate date,designation char(10),deptno number(2),reporting char(10));
```
## insert the following values into the table
```sql
insert into manager values(7369,'Dharsan',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
```

### Q1) Update all the records of manager table by increasing 10% of their salary as bonus.

### QUERY:
```sql
update manager set salary=salary+(salary*0.10);
```

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/b5b04b21-a26d-44af-8036-4511509c87a1)

### Q2) Delete the records from manager table where the salary less than 2750.

### QUERY:
```sql
delete from manager where salary<2750;
```
### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/7634f880-c775-4e0d-9829-c787b47c0a86)


### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)

### QUERY:
```sql
select ename as "Name",salary*12 as "Annual salary" from manager;
```

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/baa59d2c-7b22-42af-9018-705137f648a5)

### Q4)	List the names of Clerks from emp table.


### QUERY:
```sql
select ename from manager where designation='clerk';
```

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/aba4ce43-5ffd-48c6-9054-7967797935a9)


### Q5)	List the names of employee who are not Managers.
### QUERY:
```sql
select ename from manager where designation <> 'manager';
```

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/218d0d61-22a9-4a77-b79d-3dafed9571c8)


### Q6)	List the names of employees not eligible for commission.
### QUERY:
```sql
select ename from manager where commission=0;
```

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/5adb0d43-2e11-41b6-b885-7367bd975c08)


### Q7)	List employees whose name either start or end with ‘s’.
### QUERY:
```sql
select ename from manager where ename like '%s' or ename like 's%';
```

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/94f4c320-0270-4a9a-accd-4a6500b67d69)


### Q8) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.
### QUERY:
```sql
select ename,designation as "job",deptno,hiredate from manager order by hiredate asc;
```

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/d0e4e455-4376-4fbd-b394-1a5d17654f21)


### Q9) List the Details of Employees who have joined before 30 Sept 81.
### QUERY:
```sql
select * from manager where hiredate<to_date('1981-09-30','YYYY-MM-DD');
```

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/98418635-f955-4115-8741-553b35622b7b)


### Q10)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.
### QUERY:
```sql
 select ename,deptno,salary from manager order by deptno asc,salary desc;
```

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/5921aa13-bfcf-4155-b3ff-26ef2a14e5e2)


### Q11) List the names of employees not belonging to dept no 30,40 & 10
### QUERY:
```sql
select ename from manager where deptno not in (30,40,10);
```

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/f0522e32-9af9-45c3-9991-2b1d613bf299)

### Q12) Find number of rows in the table EMP

### QUERY:
```sql
 select count(*) from manager;
```

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/67c43609-4d86-4bc7-9ca4-1f4ea995a635)


### Q13) Find maximum, minimum and average salary in EMP table.
### MAXIMUM:
### MAXIMUM QUERY:
```sql
select max(salary) from manager;
```

### MAXIMUM OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/ba48958f-c981-4a02-bb15-5f656baa2b34)

### MINIMUM:
### MINIMUM QUERY:
```sql
select min(salary) from manager;
```
### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/a4888786-355e-4da2-94f1-45781ea6b580)

### AVERAGE:
### AVERAGE QUERY:
```sql
select avg(salary) from manager;
```

### AVERAGE OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/45aa9700-f879-4d5e-9249-893672367e45)


### Q14) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:
```sql
SELECT designation AS job, COUNT(*) AS num_employees FROM manager GROUP BY designation ORDER BY num_employees DESC;
```

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/bbdb8d5f-0b43-4131-9f6e-19f99ff719b2)


## RESULT :
To create a manager database and execute DML queries using SQL is executed successfully.


Thus the basic DML commands are executed.
