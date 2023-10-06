# EX 2 Data Manipulation Language (DML) Commands and built in functions in SQL
## AIM:
To create a manager database and execute DML queries using SQL.


## DML(Data Manipulation Language)
<div align="justify">
The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements. It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.
</div>

## List of DML commands: 
<div align="justify">
INSERT: It is used to insert data into a table.<br>
UPDATE: It is used to update existing data within a table.<br>
DELETE: It is used to delete records from a database table.<br>
</div>

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


### OUTPUT:

### Q2) Delete the records from manager table where the salary less than 2750.


### QUERY:
~~~
delete managerss1 where salary<2750;
~~~
### OUTPUT:

![WhatsApp Image 2023-10-05 at 10 34 53_17750bba](https://github.com/21005984/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/94748389/83909a25-c950-40cc-ab1e-c7d9191fdb66)

### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)
### QUERY:
~~~
SELECT
empname AS "empname",
salary*12 AS "Annual Salary"
from
managerss;
~~~
### OUTPUT:

![WhatsApp Image 2023-10-05 at 10 37 12_2dd8367c](https://github.com/21005984/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/94748389/adec2aea-dc90-4cfa-bf78-e07cc58f92f5)

### Q5)	List the names of Clerks from emp table.
### QUERY:
~~~
select empname from managerss where designation != 'manager';
~~~
### OUTPUT:

![WhatsApp Image 2023-10-05 at 10 37 41_c7ddb672](https://github.com/21005984/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/94748389/6bf20319-6d5f-44b6-a180-2d29e9dec0d7)

### Q6)	List the names of employee who are not Managers.
### QUERY:
~~~
select empname from managerss where designation != 'manager';
~~~
### OUTPUT:

![WhatsApp Image 2023-10-05 at 10 37 56_53717b66](https://github.com/21005984/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/94748389/6526bd88-7fd4-48e2-96d9-cf5c2d2d9529)

### Q7)	List the names of employees not eligible for commission.
### QUERY:
~~~
select empname from managerss where commission = 0;
~~~
### OUTPUT:

![WhatsApp Image 2023-10-05 at 10 38 15_f371a461](https://github.com/21005984/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/94748389/2719f913-3097-402e-ace7-cb38e7c9d972)

### Q8)	List employees whose name either start or end with ‘s’.
### QUERY:
~~~
select empname from managerss where empname LIKE 's%' OR empname LIKE '%s';
~~~
### OUTPUT:

![WhatsApp Image 2023-10-05 at 10 38 53_6dce431b](https://github.com/21005984/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/94748389/bd86733d-4c11-461f-8594-fefa5cf17202)

### Q9) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.


### QUERY:


### OUTPUT:


### Q10) List the Details of Employees who have joined before 30 Sept 81.


### QUERY:


### OUTPUT:


### Q11)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.


### QUERY:


### OUTPUT:


### Q12) List the names of employees not belonging to dept no 30,40 & 10


### QUERY:


### OUTPUT:

### Q13) Find number of rows in the table EMP

### QUERY:


### OUTPUT:


### Q14) Find maximum, minimum and average salary in EMP table.

### QUERY:


### OUTPUT:


### Q15) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:


### OUTPUT:
