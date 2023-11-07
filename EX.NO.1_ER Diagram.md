# EXP NO 1: ER DIAGRAM CREATION, RELATIONAL MODEL AND SCHEMA GENERATION  
### DATE
## AIM:
<div align="justify">
   To create a ER Diagram for Bank management system or College management system using ERD Plus tool and generate the relational model with schema. 
</div>

## Algorithm
1. Create a login with https://erdplus.com.
2. Create a new ER Diagram with name
3. Create a strong entity, relation and attributes.
4. Create a weak entity, relation and attributes.
5. Specify attributes unique, multivalued and composite attributes.

### ER Diagram 
![image (1)](https://github.com/KISHORE22001263/DBMS/assets/121484538/538bdd94-91c5-4660-8585-00ab140f6d41)
### Relational model
![Screenshot 2023-10-26 082828](https://github.com/KISHORE22001263/DBMS/assets/121484538/8e162eec-e523-4155-9547-656b0d55bf5f)
### SQL DDL Schema 
```
NAME:RAGHUL.S
REF.NO:212222040128
```
```
CREATE TABLE bank
(
  code INT NOT NULL,
  Name INT NOT NULL,
  addr INT NOT NULL,
  PRIMARY KEY (code)
);

CREATE TABLE BANK_BRANCHES
(
  Addr INT NOT NULL,
  Branch_no INT NOT NULL,
  PRIMARY KEY (Branch_no)
);

CREATE TABLE ACCOUNT
(
  Acct_no INT NOT NULL,
  Balance INT NOT NULL,
  Type INT NOT NULL,
  PRIMARY KEY (Acct_no)
);

CREATE TABLE CUSTOMER
(
  Name INT NOT NULL,
  Ssn INT NOT NULL,
  phone INT NOT NULL,
  Addr INT NOT NULL,
  PRIMARY KEY (Ssn)
);

CREATE TABLE LOAN
(
  Loan_no INT NOT NULL,
  Amount INT NOT NULL,
  type INT NOT NULL,
  PRIMARY KEY (Loan_no)
);
```
## RESULT 
<div align="justify">
Thus the ER diagram was drawn and relational diagram, SQL DDL staements are generated using ERD plus tool.
</div>
