# EX.NO.5 SubQueries, Views and Joins 
### DATE:07/11/2023
## AIM:
To use SubQueries, Views and Joins in SQL 
## Create employee Table:
```sql
CREATE TABLE EMP (EMPNO NUMBER(4) PRIMARY KEY,ENAME VARCHAR2(10),JOB VARCHAR2(9),MGR NUMBER(4),HIREDATE DATE,SAL NUMBER(7,2),COMM NUMBER(7,2),DEPTNO NUMBER(2));
```
## Insert the values:
```sql
INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7369, 'SMITH', 'CLERK', 7902, '17-DEC-80', 800, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7499, 'ALLEN', 'SALESMAN', 7698, '20-FEB-81', 1600, 300, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7521, 'WARD', 'SALESMAN', 7698, '22-FEB-81', 1250, 500, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7566, 'JONES', 'MANAGER', 7839, '02-APR-81', 2975, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7654, 'MARTIN', 'SALESMAN', 7698, '28-SEP-81', 1250, 1400, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7698, 'BLAKE', 'MANAGER', 7839, '01-MAY-81', 2850, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7782, 'CLARK', 'MANAGER', 7839, '09-JUN-81', 2450, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7788, 'SCOTT', 'ANALYST', 7566, '19-APR-87', 3000, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7839, 'KING', 'PRESIDENT', NULL, '17-NOV-81', 5000, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7844, 'TURNER', 'SALESMAN', 7698, '08-SEP-81', 1500, 0, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7876, 'ADAMS', 'CLERK', 7788, '23-MAY-87', 1100, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7900, 'JAMES', 'CLERK', 7698, '03-DEC-81', 950, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7902, 'FORD', 'ANALYST', 7566, TO_DATE('03-DEC-81', 'DD-MON-RR'), 3000, 20, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7934, 'MILLER', 'CLERK', 7782, TO_DATE('23-JAN-82', 'DD-MON-RR'), 1300, 10, 10);
```

## Create department table:
```sql
CREATE TABLE DEPT (DEPTNO NUMBER(2) PRIMARY KEY,DNAME VARCHAR2(14),LOC VARCHAR2(13));
```
## Insert the values in the department table:
```sql
INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (10, 'ACCOUNTING', 'NEW YORK');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (20, 'RESEARCH', 'DALLAS');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (30, 'SALES', 'CHICAGO');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (40, 'OPERATIONS', 'BOSTON');
```

### Q1) List the name of the employees whose salary is greater than that of employee with empno 7566.
### QUERY:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/f789d183-6a2c-49b1-9b01-1db0147649fe)


### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/6f8de4b4-e6fb-41f8-8fbf-f7b4e9bd04dc)

### Q2) List the ename,job,sal of the employee who get minimum salary in the company.

### QUERY:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/42d07219-17f7-4f18-87c9-c7e104ba875a)


### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/b4c23998-7929-458e-9105-35242f1c2a89)

### Q3) List ename, job of the employees who work in deptno 10 and his/her job is any one of the job in the department ‘SALES’.

### QUERY:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/8eb982be-70da-41b7-8fe3-5f2596762ff4)


### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/3df79f66-8408-43ab-b650-7871d4d4cf6d)


### Q4) Create a view empv5 (for the table emp) that contains empno, ename, job of the employees who work in dept 10.

### QUERY:

![image](https://github.com/NITHISH74/DBMS/assets/94164665/df16d737-f283-4d27-bd75-ec31942b9b37)

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/b1bf345b-c5ee-4920-9b18-1c20bc9b39c3)

### Q5) Create a view with column aliases empv30 that contains empno, ename, sal of the employees who work in dept 30. Also display the contents of the view.

### QUERY:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/992e863a-7087-402f-90b2-444df559116a)


### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/11c5bd61-cef9-4fb9-8a2c-6f2538bf5ff1)

### Q6) Update the view empv5 by increasing 10% salary of the employees who work as ‘CLERK’. Also confirm the modifications in emp table

### QUERY:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/07d42810-6247-4b3f-beac-5350271139f7)


### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/f02d4704-f834-40f0-ae47-1c5c375d4e5a)

## Create a Customer1 Table:
```sql
CREATE TABLE Customer1 (customer_id INT,cust_name VARCHAR(20),city VARCHAR(20),grade INT,salesman_id INT);
```
## Inserting Values to the Table:
```sql
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3002, 'Nick Rimando', 'New York', 100, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3007, 'Brad Davis', 'New York', 200, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3005, 'Graham Zusi', 'California', 200, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3008, 'Julian Green', 'London', 300, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3004, 'Fabian Johnson', 'Paris', 300, 5006);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3009, 'Geoff Cameron', 'Berlin', 100, 5003);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3003, 'Jozy Altidor', 'Moscow', 200, 5007);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3001, 'Brad Guzan', 'London', NULL, 5005);
```
## Create a Salesperson1 table:
```sql
CREATE TABLE Salesman1 (salesman_id INT,name VARCHAR(20),city VARCHAR(20),commission DECIMAL(4,2));
```
## Inserting Values to the Table:
```sql
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5001, 'James Hoog', 'New York', 0.15);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5002, 'Nail Knite', 'Paris', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5005, 'Pit Alex', 'London', 0.11);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5006, 'Mc Lyon', 'Paris', 0.14);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5007, 'Paul Adam', 'Rome', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5003, 'Lauson Hen', 'San Jose', 0.12);
```
### Q7) Write a SQL query to find the salesperson and customer who reside in the same city. Return Salesman, cust_name and city.

### QUERY:

![image](https://github.com/NITHISH74/DBMS/assets/94164665/a997d2b5-eb04-4537-9105-cdd4343edfe2)

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/37590c5b-f0d5-4fe4-9ed7-765131f2c216)

### Q8) Write a SQL query to find salespeople who received commissions of more than 13 percent from the company. Return Customer Name, customer city, Salesman, commission.


### QUERY:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/41f17aa0-b4e6-4c73-ab23-0ca28ca7dc68)


### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/018dc320-658a-40c9-b472-430242511a7c)

### Q9) Perform Natural join on both tables

### QUERY:

![image](https://github.com/NITHISH74/DBMS/assets/94164665/930b5e75-a18b-41ef-9213-e09da0f0847c)

### OUTPUT:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/004046ef-c39d-4256-bbfa-89ef8d1c8cab)

### Q10) Perform Left and right join on both tables

### QUERY:
### Left Join:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/d0492214-fe9f-42ad-a1b2-0b06f6d1293c)
### Right Join:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/51a98d8a-b01b-4b8f-b0a4-b2abf53a5580)


### OUTPUT:
### Left Join:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/649fb134-ab20-4a9a-a3f3-9d28e0b0d60f)

### Right Join:
![image](https://github.com/NITHISH74/DBMS/assets/94164665/c1772e49-4d60-4db3-871d-bd88f959170a)


## RESULT 
Thus the basics of subqueries,views,joins are performed in SQL.
