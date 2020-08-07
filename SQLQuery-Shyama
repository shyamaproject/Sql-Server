-- SqlServer Tutorial-- 01
-- Creation of DB
create database Djshyama

--How can we use DB
use Djshyama


--******************
--******************
--******************
--Creation of Table in DB
create table shyamatable
(
ID int, 
Name nvarchar(50), 
Salary int, 
Addresss nvarchar(100)
)

--Select the table all record(*)
select * from shyamatable

--Add/insert record into table
insert into shyamatable values(1,'Ali',55000,'North Karachi')
insert into shyamatable values(2,'Lara',75000,'North Karachi')
insert into shyamatable values(3,'John',65000,'North Karachi')
insert into shyamatable values(4,'Bob',59000,'North Karachi')

--Answer:++++++++++++++++++++++++
--ID	Name	Salary	Addresss
--1		Ali		55000	North Karachi
--2		Lara	75000	North Karachi
--3		John	65000	North Karachi
--4		Bob		59000	North Karachi

--******************
--******************
--******************


--Delete all record from table (where Clause)
delete from shyamatable where ID=2

/*
Multi
line
Comments
*/



-- SqlServer Tutorial-- 02
--insert another query
insert into shyamatable(ID,Name) values(5,'Eve')
insert into shyamatable(ID, Salary, Addresss) values(6,45000,'Karachi')

-- Update Query
update shyamatable
set Name = 'Raheel'
where ID =1

update shyamatable
set Name = 'Adam'
where Salary =75000

select * from shyamatable




-- SqlServer Tutorial-- 03
--Where Clause

select * from shyamatable where ID=1
select ID, Name from shyamatable where ID=1
select ID, Name,Salary from shyamatable where ID=1

--Operators ( AND, NOT ,OR) WITH WHERE CLAUSE

select * from shyamatable where Name= 'Raheel' AND Salary =55000
select * from shyamatable where Name= 'Rahel' AND Salary =55000

select * from shyamatable where Name= 'Rael' OR Salary =55000
select * from shyamatable where Name= 'Rahel' OR Salary =5000

select * from shyamatable where NOT Name='Raheel'

-- Order by (sorting) asc/desc
select * from shyamatable
order by Salary asc




-- SqlServer Tutorial-- 04
--is null / is not null
select * from shyamatable
where Salary is null

select * from shyamatable
where Salary is not null

select * from shyamatable
where (Salary is null OR Name is not null)




-- SqlServer Tutorial-- 05
-- Alter (add Column)
alter table shyamatable
add UC_Number nvarchar(50)

insert into shyamatable values(7,'John',69000,'North Karachi','UC-5')

--Alter (Column data types Change)
alter table shyamatable
alter column UC_Number varchar(50)


-- Alter drop (Column delete)
alter table shyamatable
drop column UC_Number


-- SqlServer Tutorial-- 06
--Data types in Sql
--create table shyamatable
--(ID tinyint, Name char(50), Salary int, Addresss nvarchar(100))


declare @aa tinyint
set @aa = 255
select @aa

declare @bb smallint
set @bb = -400
select @bb

declare @cc int
set @cc = -5260
select @cc

declare @dd bigint
set @dd = -5260
select @dd

declare @aa bit
set @aa = null
select @aa

declare @aa decimal(7,2)
set @aa = 255.121239
select @aa

declare @aa numeric(7,2)
set @aa = 255.129
select @aa

declare @aa nvarchar(77)
set @aa = N'????'
select @aa

declare @aa char(77)
set @aa = 'asdfasd'
select @aa

declare @aa nchar(77)
set @aa = '????'
select @aa

declare @aa varchar(77)
set @aa = 'asdf asdf asdf '
select @aa

declare @aa nvarchar(77)
set @aa = N'????'
select @aa

declare @aa money
set @aa = 25678567856785.129
select @aa

declare @aa smallmoney
set @aa = 214112
select @aa

declare @aa Date
set @aa = getDate()
select @aa

declare @aa Date
set @aa = '12-12-2009'
select @aa

declare @aa time
set @aa = '12:12:12'
select @aa

declare @ab float
set @ab = 12.12123123123
select @ab

declare @ab real
set @ab = 12.12123123123
select @ab




-- SqlServer Tutorial-- 07
--SQL constraints are used to specify rules for data in a table.
--PK, identity (auto_increment), FK, unique, not null, default,


create table aa
(ID int primary key ,
Name nvarchar(50) Not null,
RollNo int unique,
Date date default getdate(),
Serial_Number int identity(1,1))

select * from aa
insert into aa values(1, 'ali',123,'11-11-2000')
insert into aa(ID,Name,RollNo) values(2, 'Rashid',456) -- automatic datatime in Computer DateTime
insert into aa values(1, 'ali',1,null,null) -- Here Datatime null & serial_number is Automatic 




-- SqlServer Tutorial-- 08
--Operator in SQL
--Arithmetic operators

select 10 + 10
select 10 - 10
select 10 * 10
select 10 / 10
select 10 % 10

--SQL Comparison Operators
declare @a int
set @a =10
select @a where 10 <> 20  -- no column Name


select @a where 10 < 20 -- ans : 10


--Command Operator a=a+10 (a+=10)
declare @b int
set @b = 10
set @b +=10 -- = 10+10
select @b

--Bitwise operator

select 1 & 2
select 1 | 2
select 1 ^ 2
select ~2




-- SqlServer Tutorial-- 09
-- Max, Min and top function of SQL

select * from shyamatable
select max(Salary) from shyamatable 
select min(Salary) from shyamatable
select * from shyamatable
select TOP 3 Salary from shyamatable



-- SqlServer Tutorial-- 10
--AGGREGATE FUNCTION OF SQL
select * from shyamatable
select count(Name) from shyamatable
select avg(Salary) from shyamatable
select SUM(Salary) from shyamatable




-- SqlServer Tutorial-- 11
-- SubQuery

select Salary from shyamatable
where Salary < 6000

select Salary from shyamatable  --outer query
where Salary >=  (select max(salary) from shyamatable) --inner query

select max(salary) from shyamatable
where Salary < (select max(salary) from shyamatable)




-- SqlServer Tutorial-- 12
Create table tblDepartment
(
ID int primary key,
DepartmentName nvarchar(50),
Location nvarchar(50),
DepartmentHead nvarchar(50)
)


Insert into tblDepartment values (1, 'FINANCE', 'Karachi', 'Haris')
Insert into tblDepartment values (2, 'PRODUCTION', 'Lahore', 'Laraib')
Insert into tblDepartment values (3, 'HR', 'Multan', 'Junaid')
Insert into tblDepartment values (4, 'UNKNOWN', 'Sakkar', 'Ahmed')

Create table tblEmployee
(
ID int primary key,
Name nvarchar(50),
Gender nvarchar(50),
Salary int,
--DepartmentId int foreign key references tblDepartment(Id)
)


Insert into tblEmployee values (1, 'Tom', 'Male', 4000, 1)
Insert into tblEmployee values (2, 'Pam', 'Female', 3000, 3)
Insert into tblEmployee values (3, 'John', 'Male', 3500, 1)
Insert into tblEmployee values (4, 'Sam', 'Male', 4500, 2)
Insert into tblEmployee values (5, 'Todd', 'Male', 2800, 2)
Insert into tblEmployee values (6, 'Ben', 'Male', 7000, 1)
Insert into tblEmployee values (7, 'Sara', 'Female', 4800, 3)
Insert into tblEmployee values (8, 'Valarie', 'Female', 5500, 1)
Insert into tblEmployee values (9, 'James', 'Male', 6500, NULL)

--JOIN OR INNER JOIN
SELECT Name, Gender, Salary, DepartmentName
FROM tblEmployee
INNER JOIN tblDepartment
ON tblEmployee.DepartmentId = tblDepartment.Id


-- JOIN (Only Join)
create table OrdersTable -- onetable
(
 OrderID int primary key,
 CustomerID int,
 Orderdate nvarchar(50)
 )

 insert into OrdersTable values(1,2,'One')
 insert into OrdersTable values(2,55,'two')
 insert into OrdersTable values(3,575,'three')

 create table cutomers -- twotable
 (
  CustomerID int,
  CustomerName nvarchar(50),
  ContactName nvarchar(50),
  Country nvarchar(50)
 )

	insert into cutomers values(1,'Shyama','Shyama','India')
	insert into cutomers values(2,'tara','tara','Londan')
	insert into cutomers values(3,'ranjit','ranjit','America')

	-- OrdersTable Notun name create hobe jekhane tui table er modhye bachchi kore neya hobe.
	select OrdersTable.OrderID, cutomers.CustomerName ,OrdersTable.Orderdate
	from OrdersTable   -- One Table
	-- Customers table joint hobe.
	inner join cutomers -- Two Table
	--OrderTable sathe Cutomer Id..
	on OrdersTable.CustomerID = cutomers.CustomerID

 select * from OrdersTable
 select * from cutomers

--(INNER) JOIN: Returns records that have matching values in both tables
--LEFT (OUTER) JOIN: Returns all records from the left table, and the matched records from the right table
--RIGHT (OUTER) JOIN: Returns all records from the right table, and the matched records from the left table
--FULL (OUTER) JOIN: Returns all records when there is a match in either left or right table
--LEFT JOIN OR LEFT OUTER JOIN


--SQL INNER JOIN SYNTAX 

SELECT column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;


	-- OrdersTable Notun name create hobe jekhane tui table er modhye bachchi kore neya hobe.
	select OrdersTable.OrderID, cutomers.CustomerName 
	from OrdersTable  -- One Table
	-- Customers table joint hobe.
	inner join cutomers  -- Two Table
	--OrderTable sathe Cutomer Id..
	on OrdersTable.CustomerID = cutomers.CustomerID


	select OrdersTable.OrderID, cutomers.Country 
	from OrdersTable  -- One Table
	-- Customers table joint hobe.
	inner join cutomers  -- Two Table
	--OrderTable sathe Cutomer Id..
	on OrdersTable.CustomerID = cutomers.CustomerID


 select * from OrdersTable
 select * from cutomers

--Three Table Inner Join
SELECT Orders.OrderID, Customers.CustomerName, Shippers.ShipperName
FROM ((Orders
INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID)
INNER JOIN Shippers ON Orders.ShipperID = Shippers.ShipperID);


--SQL LEFT JOIN SYNTAX 
SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;

--OrderTable & Customer Table
SELECT cutomers.CustomerName, OrdersTable.OrderID
FROM cutomers
LEFT JOIN OrdersTable --jehetu Order Table Left & Right Table Customer
ON cutomers.CustomerID = OrdersTable.CustomerID
ORDER BY cutomers.CustomerName;
 select * from OrdersTable
 select * from cutomers

 --SQL RIGHT JOIN SYNTAX 
 SELECT column_name(s)
FROM table1
RIGHT JOIN table2
ON table1.column_name = table2.column_name;


--Order Table  & Employees Table
--Hera Orders Table & Employees Table
SELECT Orders.OrderID, Employees.LastName, Employees.FirstName
FROM Orders
RIGHT JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID
ORDER BY Orders.OrderID;


--SQL FULL JOIN SYNTAX 
SELECT column_name(s)
FROM table1
FULL OUTER JOIN table2
ON table1.column_name = table2.column_name
WHERE condition;

--Hera Orders Table & Customers Table
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
FULL OUTER JOIN Orders ON Customers.CustomerID=Orders.CustomerID
ORDER BY Customers.CustomerName;


--SQL SELF JOIN SYNTAX 
--Ekti Table sathe jog hoy..
SELECT column_name(s)
FROM table1 T1, table1 T2
WHERE condition;

SELECT A.CustomerName AS CustomerName1, B.CustomerName AS CustomerName2, A.City
FROM Customers A, Customers B
WHERE A.CustomerID <> B.CustomerID
AND A.City = B.City
ORDER BY A.City;

SELECT Name, Gender, Salary, DepartmentName
FROM tblEmployee
LEFT OUTER JOIN tblDepartment
ON tblEmployee.DepartmentId = tblDepartment.Id

--RIGHT JOIN OR RIGHT OUTER JOIN

SELECT Name, Gender, Salary, DepartmentName
FROM tblEmployee
RIGHT OUTER JOIN tblDepartment
ON tblEmployee.DepartmentId = tblDepartment.Id

--FULL JOIN OR FULL OUTER JOIN
SELECT Name, Gender, Salary, DepartmentName
FROM tblEmployee
FULL OUTER JOIN tblDepartment

ON tblEmployee.DepartmentId = tblDepartment.Id




-- SqlServer Tutorial-- 13
--SELF JOIN:

 CREATE TABLE EmployeeTable
(
 EmployeeID  int primary key,
 EmployeeName varchar(20) NULL,
 JoinData date NULL,
 Employe_SuperViser int NULL,
 CONSTRAINT Employe_SuperViser FOREIGN KEY(Employe_SuperViser)  REFERENCES EmployeeTable(EmployeeID)
)

Insert into EmployeeTable values (1, 'Tom',  '1-JAN-2000', NULL)
Insert into EmployeeTable values (2, 'Pam', '1-FEB-2000', 1)
Insert into EmployeeTable values (3, 'John','1-DEC-2000', 2)
Insert into EmployeeTable values (4, 'Sam','1-MAR-2000',  2)
Insert into EmployeeTable values (5, 'Todd','1-JUN-2000', 1)
Insert into EmployeeTable values (6, 'Ben','1-JUL-2000' , 4)
Insert into EmployeeTable values (7, 'Sara','1-MAY-2000', 5)

select * from EmployeeTable

SELECT 

a.EmployeeID AS "Emp_ID", -- Here Emp_Id is a Heading
a.EmployeeName AS "Employee Name",-- Here Employee Name is a Heading
b.EmployeeID AS "Supervisor ID", --Create Supevisor ID is a Column Name 
b.EmployeeName AS "Supervisor Name" --Create Supervisor Name is a Column Name 

FROM EmployeeTable a, EmployeeTable b --Two Table Create temporary

WHERE a.Employe_SuperViser = b.EmployeeID; --Here a te asbe main table Employe_SuperViser & b te asbe main table EmployeeID


--SELF JOIN:
CREATE TABLE employee123
(emp_id  int primary key,
emp_name varchar(20) NULL,
dt_of_join date NULL,
emp_supv int NULL,
CONSTRAINT emp_supv FOREIGN KEY(emp_supv)  REFERENCES employee12(emp_id)
)

Insert into employee12 values (1, 'Tom',  '1-JAN-2000', NULL)
Insert into employee12 values (2, 'Pam', '1-FEB-2000', 1)
Insert into employee12 values (3, 'John','1-DEC-2000', 2)
Insert into employee12 values (4, 'Sam','1-MAR-2000',  2)
Insert into employee12 values (5, 'Todd','1-JUN-2000', 1)
Insert into employee12 values (6, 'Ben','1-JUL-2000' , 4)
Insert into employee12 values (7, 'Sara','1-MAY-2000', 5)


select * from employee12

SELECT a.emp_id AS "Emp_ID",a.emp_name AS "Employee Name",
b.emp_id AS "Supervisor ID",b.emp_name AS "Supervisor Name"
FROM employee12 a, employee12 b

WHERE a.emp_supv = b.emp_id;




-- SqlServer Tutorial-- 14
create database UnionDB
use UnionDB

create table Emp
(ID int primary key identity(1,1), Name nvarchar(50),
Salary int, Country nvarchar(50))

insert into Emp values('Laraib',55000,'pak')
insert into Emp values('Haris',53000,'ind')
insert into Emp values('Jazz',7500,'agh')
insert into Emp values('Hamjoo',85000,'china')
insert into Emp values('Eve',15000,'Bag')
insert into Emp values('Kajul',7000,'Bag')
insert into Emp values('Hamza',95000,'china')
insert into Emp values('lara',47000,'Bag')

create table Tem
(ID int primary key identity(1,1), Name nvarchar(50),
Salary int, Country nvarchar(50))

insert into Tem values('Muz',55000,'pak')
insert into Tem values('Jazz',55000,'ind')
insert into Tem values('Telenor',55000,'agh')
insert into Tem values('Kjo',55000,'china')
insert into Tem values('Lolo',55000,'Bag')

select * from Emp
union
select * from Tem


select * from Emp
union all
select * from Tem


select * from Emp

select COUNT(ID), country
from Emp
group by Country




-- SqlServer Tutorial-- 15
select COUNT(ID), country
from Emp
group by Country
having COUNT(ID) >=2




-- SqlServer Tutorial-- 16
declare @ID int
set @ID =5
select
case @ID
when 1 then 'Value is 1'
when 2  then'Value is 2'
when 3 then 'Value is 3'
else 'None'
end

select * from Emp

select
CASE
when Salary >=2000 and Salary <=10000 then 'Manager'
when Salary >=11000 and Salary <=20000 then 'Senior Manager'
else 'Director'

End as Designation from Emp

					

-- SqlServer Tutorial-- 17
create table Emp1
(ID int , Name nvarchar(50),
Salary int, Country nvarchar(50))

insert into Emp1 values(1,'Laraib',55000,'pak')
insert into Emp1 values(2,'Haris',53000,'ind')
insert into Emp1 values(3,'Jazz',7500,'agh')
insert into Emp1 values(4,'Hamjoo',85000,'china')
insert into Emp1 values(5,'Eve',15000,'Bag')
insert into Emp1 values(6,'Kajul',7000,'Bag')
insert into Emp1 values(7,'Hamza',95000,'china')
insert into Emp1 values(8,'lara',47000,'Bag')

create table Tem1
(ID int, Name nvarchar(50),
Salary int, Country nvarchar(50))

insert into Tem1 values(1,'Muz',55000,'pak')
insert into Tem1 values(2,'Jazz',55000,'ind')
insert into Tem1 values(3,'Telenor',55000,'agh')
insert into Tem1 values(4,'Kjo',55000,'china')
insert into Tem1 values(5,'Lolo',55000,'Bag')

select * from Emp1
select * from Tem1


insert into Tem1 select * from Emp1
insert into Tem1(__,__,_) select * from Emp1

insert into Tem1(ID,Name) select * from Emp1 where ID=1




-- SqlServer Tutorial-- 18
--Department Table
CREATE TABLE Department
(
ID int PRIMARY KEY, --primary key
Name nvarchar (50) NOT NULL,
Address nvarchar (50) NOT NULL
)
insert into Department values(1,'IT','Karachi')
insert into Department values(2,'HR','Lahore')
insert into Department values(3,'Marketing','Multan')
--Student Table
CREATE TABLE Student
(
ID int PRIMARY KEY, --primary key
RollNo varchar(10) NOT NULL,
Name nvarchar(50) NOT NULL,
EnrollNo nvarchar(50) UNIQUE, --unique key
Address nvarchar(200) NOT NULL,
DeptID int FOREIGN KEY REFERENCES Department(ID) --foreign key
)
insert into Student values(1,123,'Rashid','Student159','North Karachi',2)
insert into Student values(2,148,'Ali','Student1239','North',1)

 

insert into Student values(3,423,'Sara','Student1439','North Nazi',3)


CREATE TABLE userdata (
userid INT,
userdataid INT,
info char(200),
primary key (userid, userdataid)
);
select * from userdata
insert into userdata values(1,2,'Yes Sold')


					

-- SqlServer Tutorial-- 19
create database Cart1
use Cart1

-- 1 to 1 relationship
CREATE TABLE Person
(
Pk_Person_Id INT IDENTITY PRIMARY KEY,
Name VARCHAR(255),
EmailId VARCHAR(255),
);

CREATE TABLE PassportDetails
(
Pk_Passport_Id INT PRIMARY KEY,
Passport_Number VARCHAR(255),
Fk_Person_Id INT UNIQUE FOREIGN KEY REFERENCES dbo.Person(Pk_Person_Id)
);

INSERT INTO Person VALUES ('Niraj','v.a@emails.com');
INSERT INTO Person VALUES ('Vishwanath','v.v@emails.com');

 

INSERT INTO Person VALUES ('Chetan','c.v@emails.com');


INSERT INTO PassportDetails VALUES (101, 'C3031R33', 1);
INSERT INTO PassportDetails VALUES (102, 'VRDK5695', 2);
INSERT INTO PassportDetails VALUES (103, 'A4DEK33D', 3);
INSERT INTO PassportDetails VALUES (104, 'A4DEK33D', 3);


SELECT * FROM Person
SELECT * FROM PassportDetails;


-- 1 to many relationship
CREATE TABLE Book
(
Pk_Book_Id INT PRIMARY KEY,
Name VARCHAR(255),
ISBN VARCHAR(255)
);

CREATE TABLE Author
(
Pk_Author_Id INT PRIMARY KEY,
FullName     VARCHAR(255),
MobileNo     CHAR(10),
Fk_Book_Id   INT FOREIGN KEY REFERENCES Book(Pk_Book_Id)
);

INSERT INTO Book VALUES (1, 'Let is Snow', 'ISBN3030303');
INSERT INTO Book VALUES (2, 'Three Cups of Tea','ISBN638242');

 



INSERT INTO Author VALUES(100,'John Green','30303',1);
INSERT INTO Author VALUES(101,'Maureen Johnson','4343',1);
INSERT INTO Author VALUES(102,'Lauren Myracle','76665',1);
INSERT INTO Author VALUES(103,'Greg Mortenson','6434',2);
INSERT INTO Author VALUES(104,'David Oliver Relin','72322',2);


SELECT * FROM Book;
SELECT * FROM Author;

-- SqlServer Tutorial-- 20
-- Many to 1 relationship
--inverse to many to 1...

-- Many to Manay relationship

CREATE TABLE Class(
ID int PRIMARY KEY,
Title varchar(30),
Instructor varchar(30),
Day varchar(15),
Time varchar(10)
);
insert into Class values(1,'Class 1','Rizwan','Tuesday','10:10:10')
insert into Class values(2,'Class 2','Haris','Firday','12:10:10')

 

insert into Class values(3,'Class 3','Rajo','Saturday','09:10:10')


CREATE TABLE Student(
ID int PRIMARY KEY,
Name varchar(35),
Major varchar(35),
ClassYear varchar(10),
Status varchar(10)
); 

insert into Student values(1,'Lara','CS','2000','yes')
insert into Student values(2,'Junaid','CS','2001','yes')
insert into Student values(3,'Aslam','CS','2002','No')


CREATE TABLE ClassStudentRelation(
ID int NOT NULL,
StudentAddress varchar(14) NOT NULL,
ClassID int foreign key references Class(ID),
StudentID int foreign key references Student(ID)
 
);
insert into ClassStudentRelation values(1,'Karachi',1,2)
insert into ClassStudentRelation values(2,'Lahore',2,3)
insert into ClassStudentRelation values(3,'Multan',1,1)



-- SqlServer Tutorial-- 21
--Store Procedure in SQL
select * from Emp

Create procedure SPemp
as
begin
select EName, job from Emp where EmpNo=1001
end

exec SPemp
execute SPemp

drop procedure SPemp

Create procedure SPempPara
@EmpNo int,
@Ename nvarchar(50)
as
begin
select * from Emp where EmpNo=@EmpNo and Ename=@Ename
end


exec SPempPara 1001,'Husaam'




CREATE TABLE EmployeeTable
(
 EmployeeID  int Primary key ,
 EmployeeName varchar(20) NULL,
 JoinData date NULL,
 Employe_SuperViser int NULL,
)

Insert into EmployeeTable values (1, 'Tom',  '1-JAN-2000', NULL)
Insert into EmployeeTable values (2, 'Pam', '1-FEB-2000', 1)
Insert into EmployeeTable values (3, 'John','1-DEC-2000', 2)
Insert into EmployeeTable values (4, 'Sam','1-MAR-2000',  2)
Insert into EmployeeTable values (5, 'Todd','1-JUN-2000', 1)
Insert into EmployeeTable values (6, 'Ben','1-JUL-2000' , 4)
Insert into EmployeeTable values (7, 'Sara','1-MAY-2000', 5)


select * from EmployeeTable

CREATE PROCEDURE EmployeeTablePro -- create store procedure
as
begin 
select EmployeeID,EmployeeName,JoinData,Employe_SuperViser from EmployeeTable
end

exec EmployeeTablePro


CREATE PROCEDURE EmployeeTableProcedure  
--@declare kora hole exec korar somoy value pass korte hobe.
-- Jato Gulo Value takbe tatogulo value dite hobe.
 @EmployeeID  int ,
 @EmployeeName varchar(20) --, deyo jabe na.


as
begin
select * from EmployeeTable where EmployeeID = @EmployeeID AND EmployeeName = @EmployeeName 
end

execute EmployeeTableProcedure 1,'Tom'




------------------------------------------
-----------Sql Server Tutorial------------
------------------------------------------
--Example - 01
--SQL CREATE DATABASE
--CREATE DATABASE databasename
--Eti Sql Server database naam create kore.
Create Database Djshyama


--Example - 02
--SQL DROP DATABASE
--DELETE OR REMOVE OR DROP DATABASE databasename
--Eti Sql Server database naam delete kore.
DROP DATABASE Djshyama


--Example - 03
--SQL Alter DATABASE
--Alter DATABASE TableName(Old) Modify Name = NewTableName
--Eti Sql Server database naam change kore annya name.
Alter DATABASE Djshyama Modify Name = ShyamaFile


--Example - 04
--SQL CREATE TABLE
--Create Table TableName
CREATE TABLE Persons (
	PersonID int,
	LastName varchar(255),
	FirstName varchar(255),
	Address varchar(255),
	City varchar(255)
);


--Example - 05
--SQL DROP TABLE 
--DROP TABLE table_name
--Eti je kono table ke delete kore.
DROP TABLE Persons;


--Example - 06
--SQL ALTER TABLE (	NEW COLUMN ADD)
--ALTER TABLE - ADD Column
--Eti je kono table er side a column create kore.
ALTER TABLE table_name
ADD column_name datatype;

	--Ex:
ALTER TABLE Customers
ADD Email varchar(255);


--Example - 07
--ALTER TABLE DELETE OR REMOVE OR DROP COLUMN 
--ALTER TABLE - DROP COLUMN
--Eti je kono table er side a column delete kore.
ALTER TABLE table_name
DROP COLUMN column_name;
			
	--Ex:
ALTER TABLE Customers
DROP COLUMN Email;


--Example - 08
--ALTER TABLE - ALTER/MODIFY COLUMN
--ALTER TABLE table_name ALTER COLUMN column_name datatype;
ALTER TABLE table_name
ALTER COLUMN column_name datatype;

	--Ex:
ALTER TABLE table_name
MODIFY COLUMN column_name datatype;

	--Ex:
ALTER TABLE table_name
MODIFY column_name datatype;


	--Example - 09
--SQL Constraints
--CREATE TABLE table_name
--SQL constraints are used to specify rules for data in a table.
--Constraints can be specified when the table is created with the CREATE TABLE statement, or after the table is created with the ALTER TABLE statement.

CREATE TABLE table_name (
	column1 datatype constraint,
	column2 datatype constraint,
	column3 datatype constraint,
	....
);
		

--Example - 10
--SQL UNIQUE Constraint on CREATE TABLE
CREATE TABLE Persons (
	ID int NOT NULL UNIQUE,
	LastName varchar(255) NOT NULL,
	FirstName varchar(255),
	Age int
);

-- Allow Null: OR NULL :- Value na likhle o Cholbe...
-- NOT NULL :- Value must be likhte hobe...
CREATE TABLE Persons (
	ID int NOT NULL,
	LastName varchar(255) NOT NULL,
	FirstName varchar(255),
	Age int,
	UNIQUE (ID)
);

CREATE TABLE Persons (
	ID int NOT NULL,
	LastName varchar(255) NOT NULL,
	FirstName varchar(255),
	Age int,
	CONSTRAINT UC_Person UNIQUE (ID,LastName)
);

--Example - 12
--SQL UNIQUE Constraint on ALTER TABLE
--Unique Key te Ekti Number Press Hobe...
ALTER TABLE Persons
ADD UNIQUE (ID);

ALTER TABLE Persons
ADD CONSTRAINT UC_Person UNIQUE (ID,LastName);


--Example - 13
--SQL NOT NULL Constraint
--
CREATE TABLE Persons (
    ID int NOT NULL,	--Value Must be Enter
    LastName varchar(255) NOT NULL,
    FirstName varchar(255) NOT NULL,
    Age int
);


--Example - 14
--SQL UNIQUE Constraint on ALTER TABLE
--
ALTER TABLE Persons
MODIFY Age int NOT NULL; --Value Must be Enter

--Example - 15
--SQL UNIQUE Constraint
--
CREATE TABLE Persons (
    ID int NOT NULL UNIQUE,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int
);


CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    UNIQUE (ID)
);

CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CONSTRAINT UC_Person UNIQUE (ID,LastName)
);

--Example - 16
--SQL UNIQUE Constraint on ALTER TABLE
--
ALTER TABLE Persons
ADD UNIQUE (ID);

ALTER TABLE Persons
ADD CONSTRAINT UC_Person UNIQUE (ID,LastName);

--Example - 17
--DROP a UNIQUE Constraint
--
ALTER TABLE Persons
DROP INDEX UC_Person;

ALTER TABLE Persons
DROP CONSTRAINT UC_Person;


--Example - 18
--SQL PRIMARY KEY Constraint
--
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    PRIMARY KEY (ID)
);

CREATE TABLE Persons (
    ID int NOT NULL PRIMARY KEY,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int
);

CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CONSTRAINT PK_Person PRIMARY KEY (ID,LastName)
);

--Example - 19
--SQL PRIMARY KEY on ALTER TABLE
--
ALTER TABLE Persons
ADD PRIMARY KEY (ID);

ALTER TABLE Persons
ADD CONSTRAINT PK_Person PRIMARY KEY (ID,LastName);

--Example - 20
--DROP a PRIMARY KEY Constraint
--
ALTER TABLE Persons
DROP PRIMARY KEY;

ALTER TABLE Persons
DROP CONSTRAINT PK_Person;

--Example - 20
--SQL CHECK on CREATE TABLE
--
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CHECK (Age>=18)
);


CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int CHECK (Age>=18)
);


CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    City varchar(255),
    CONSTRAINT CHK_Person CHECK (Age>=18 AND City='Sandnes')
);

--Example - 21
--SQL CREATE INDEX Statement
--Creates an index on a table. Duplicate values are allowed:
CREATE INDEX index_name
ON table_name (column1, column2,...);

CREATE INDEX idx_lastname
ON Persons (LastName);

CREATE INDEX idx_pname
ON Persons (LastName, FirstName);

--Example - 22
--DROP INDEX Statement
--
DROP INDEX index_name ON table_name;
DROP INDEX table_name.index_name;

ALTER TABLE table_name
DROP INDEX index_name;


--Example - 23
--SQL Working With Dates
--
SELECT * FROM Orders WHERE OrderDate='2008-11-11'

--Example - 24
--SQL CREATE VIEW 
--
CREATE VIEW [Brazil Customers] AS
SELECT CustomerName, ContactName
FROM Customers
WHERE Country = 'Brazil';


CREATE VIEW [Products Above Average Price] AS
SELECT ProductName, Price
FROM Products
WHERE Price > (SELECT AVG(Price) FROM Products);


--Example - 25
--SQL Updating a View
--
CREATE OR REPLACE VIEW [Brazil Customers] AS
SELECT CustomerName, ContactName, City
FROM Customers
WHERE Country = 'Brazil';

--Example - 26
--SQL Injection
--Eti emon ekti code jeti database ke nosta kore.
--Hacking kore.
SELECT * FROM Users WHERE UserId = 105 OR 1=1;
SELECT UserId, Name, Password FROM Users WHERE UserId = 105 or 1=1;

--Example - 27
--SQL LIKE Operator
--Eti Table naam searching korte use hoy.


SELECT * FROM Customers
WHERE CustomerName LIKE 'a%';


SELECT * FROM Customers
WHERE CustomerName LIKE '%a';

--Example - 28
--SQL Aliases
--SQL aliases are used to give a table, or a column in a table, a temporary name.
--Aliases are often used to make column names more readable.
--An alias only exists for the duration of the query.
SELECT column_name AS alias_name
FROM table_name;

SELECT column_name(s)
FROM table_name AS alias_name;

SELECT CustomerID AS ID, CustomerName AS Customer
FROM Customers;

SELECT o.OrderID, o.OrderDate, c.CustomerName
FROM Customers AS c, Orders AS o
WHERE c.CustomerName='Around the Horn' AND c.CustomerID=o.CustomerID;


--Example - 29
--SQL Stored Procedures
--
CREATE PROCEDURE procedure_name
AS
sql_statement
GO;

EXEC procedure_name;

CREATE PROCEDURE SelectAllCustomers
AS
SELECT * FROM Customers
GO;


CREATE PROCEDURE SelectAllCustomers 
@City nvarchar(30)
AS
SELECT * FROM Customers 
WHERE City = @City
GO;

CREATE PROCEDURE SelectAllCustomers @City nvarchar(30), @PostalCode nvarchar(10)
AS
SELECT * FROM Customers WHERE City = @City AND PostalCode = @PostalCode
GO;

EXEC SelectAllCustomers @City = 'London', @PostalCode = 'WA1 1DP';


--Example - 101
--SQL Quick Reference

--ALTER TABLE :- 	
ALTER TABLE table_name
ADD column_name datatype

or

ALTER TABLE table_name
DROP COLUMN column_name


--AS (alias):-	
SELECT column_name AS column_alias
FROM table_name

or

SELECT column_name
FROM table_name  AS table_alias


--CREATE TABLE:-
CREATE TABLE table_name
(
column_name1 data_type,
column_name2 data_type,
column_name3 data_type,
)

--CREATE VIEW:-	
CREATE VIEW view_name AS
SELECT column_name(s)
FROM table_name
WHERE condition


--DELETE:-
DELETE FROM table_name
WHERE some_column=some_value

or

DELETE FROM table_name
(Note: Deletes the entire table!!)

DELETE * FROM table_name
(Note: Deletes the entire table!!)


--DROP DATABASE:-
DROP DATABASE database_name

--DROP TABLE:-	
DROP TABLE table_name

--EXISTS:-	
IF EXISTS (SELECT * FROM table_name WHERE id = ?)
BEGIN
--do what needs to be done if exists
END
ELSE
BEGIN
--do what needs to be done if not
END


--INSERT:- 
INTO	INSERT INTO table_name
VALUES (value1, value2, value3,....)

or

INSERT INTO table_name
(column1, column2, column3,...)
VALUES (value1, value2, value3,....)


--INSERT:-
INTO	INSERT INTO table_name
VALUES (value1, value2, value3,....)

or

INSERT INTO table_name
(column1, column2, column3,...)
VALUES (value1, value2, value3,....)


--LEFT JOIN:-	
SELECT column_name(s)
FROM table_name1
LEFT JOIN table_name2
ON table_name1.column_name=table_name2.column_name

--RIGHT JOIN:- 
	
SELECT column_name(s)
FROM table_name1
RIGHT JOIN table_name2
ON table_name1.column_name=table_name2.column_name


--FULL JOIN:-	
SELECT column_name(s)
FROM table_name1
FULL JOIN table_name2
ON table_name1.column_name=table_name2.column_name


--LIKE(%)-	
SELECT column_name(s)
FROM table_name
WHERE column_name LIKE pattern


--ORDER BY:-	
SELECT column_name(s)
FROM table_name
ORDER BY column_name [ASC|DESC]


--SELECT:-	
SELECT column_name(s)
FROM table_name

--SELECT *:-	
SELECT * FROM table_name

--TRUNCATE:- 
TABLE TRUNCATE TABLE table_name

--UNION:-	
SELECT column_name(s) FROM table_name1
UNION
SELECT column_name(s) FROM table_name2

--UNION ALL:-	
SELECT column_name(s) FROM table_name1
UNION ALL
SELECT column_name(s) FROM table_name2

--UPDATE:-	
UPDATE table_name
SET column1=value, column2=value,...
WHERE some_column=some_value


--WHERE:-	
SELECT column_name(s)
FROM table_name
WHERE column_name operator value



--**************************
--**************************

--Inner Join----
create table tableone  --TableOne
(
 Id int primary key,
 Name nvarchar(50),
 Adress nvarchar(50)
)

insert into tableone values(1,'shyama','egra')
insert into tableone values(2,'tara','contai')
insert into tableone values(3,'surajeet','egra')
insert into tableone values(4,'rangeet','contai')
insert into tableone values(5,'subhajeet','egra')

create table tabletwo --TableTwo
(
 Id int primary key,
 Deparment nvarchar(50)
)

insert into tabletwo values(1,'Hr')
insert into tabletwo values(2,'Maneger')
insert into tabletwo values(3,'Admin')




select Name,Adress,Deparment from tableone
inner join tabletwo
on tableone.Id=tabletwo.Id 

--one tableone id & tabletwo id join

select * from tableone
select * from tabletwo

------------Answer-------------	
--Name		Adress		Deparment
--shyama	egra		Hr
--tara		contai		Maneger
--surajeet	egra		Admin




--**************************
--**************************
--Self Join----
Create table EmployeeClass
(
EmployeeID int primary key,
EmployeeName varchar(50),
ManegerID int
)

Insert into EmployeeClass(EmployeeID,EmployeeName,ManegerID)values (1001,'Manish',1001); 
Insert into EmployeeClass(EmployeeID,EmployeeName,ManegerID)values (1002,'Deepti',1001);
Insert into EmployeeClass(EmployeeID,EmployeeName,ManegerID)values (1003,'Amit',1001);
Insert into EmployeeClass(EmployeeID,EmployeeName,ManegerID)values (1004,'Sandy',1002);
Insert into EmployeeClass(EmployeeID,EmployeeName,ManegerID)values (1005,'Ankit',1003);
Insert into EmployeeClass(EmployeeID,EmployeeName,ManegerID)values (1006,'Kapil',1002);

Select * from EmployeeClass;

SELECT 
a.EmployeeID as Id, 
a.EmployeeName as Employee,  

b.EmployeeName as Supervisor 

   
FROM 
EmployeeClass a, 
EmployeeClass b   

where a.ManegerID = b.EmployeeID

--------    Answer  -----------------
--Id		Employee	Supervisor
--1001		Manish		Manish
--1002		Deepti		Manish
--1003		Amit		Manish
--1004		Sandy		Deepti
--1005		Ankit		Amit
--1006		Kapil		Deepti




