# Experiment 2: DDL Commands

## AIM
To study and implement DDL commands and different types of constraints.

## THEORY

### 1. CREATE
Used to create a new relation (table).

**Syntax:**
```sql
CREATE TABLE (
  field_1 data_type(size),
  field_2 data_type(size),
  ...
);
```
### 2. ALTER
Used to add, modify, drop, or rename fields in an existing relation.
(a) ADD
```sql
ALTER TABLE std ADD (Address CHAR(10));
```
(b) MODIFY
```sql
ALTER TABLE relation_name MODIFY (field_1 new_data_type(size));
```
(c) DROP
```sql
ALTER TABLE relation_name DROP COLUMN field_name;
```
(d) RENAME
```sql
ALTER TABLE relation_name RENAME COLUMN old_field_name TO new_field_name;
```
### 3. DROP TABLE
Used to permanently delete the structure and data of a table.
```sql
DROP TABLE relation_name;
```
### 4. RENAME
Used to rename an existing database object.
```sql
RENAME TABLE old_relation_name TO new_relation_name;
```
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE) or after it is created (using ALTER TABLE).
### 1. NOT NULL
When a column is defined as NOT NULL, it becomes mandatory to enter a value in that column.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) NOT NULL
);
```
### 2. UNIQUE
Ensures that values in a column are unique.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) UNIQUE
);
```
### 3. CHECK
Specifies a condition that each row must satisfy.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) CHECK (logical_expression)
);
```
### 4. PRIMARY KEY
Used to uniquely identify each record in a table.
Properties:
Must contain unique values.
Cannot be null.
Should contain minimal fields.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) PRIMARY KEY
);
```
### 5. FOREIGN KEY
Used to reference the primary key of another table.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size),
  FOREIGN KEY (column_name) REFERENCES other_table(column)
);
```
### 6. DEFAULT
Used to insert a default value into a column if no value is specified.

Syntax:
```sql
CREATE TABLE Table_Name (
  col_name1 data_type,
  col_name2 data_type,
  col_name3 data_type DEFAULT 'default_value'
);
```

**Question 1**
--
<img width="1227" height="345" alt="image" src="https://github.com/user-attachments/assets/5c581f70-6e2d-4f86-80c8-16f394f2d23c" />
```

```
ALTER TABLE employee
ADD COLUMN designation varchar(50);

```

**Output:**

<img width="1230" height="305" alt="Screenshot 2026-08-10 182445" src="https://github.com/user-attachments/assets/bd7de382-b653-47bf-ada5-60645ef83017" />


**Question 2**
---
<img width="1235" height="540" alt="Screenshot 2026-08-10 182627" src="https://github.com/user-attachments/assets/87423811-d596-4e8a-b1e5-5e62b1667e68" />

```sql
INSERT INTO Student_details (RollNo,Name,Gender,Subject,MARKS) VALUES (205,"Olivia Green","F",NULL,NULL),(207,"Liam Smith","M","Mathematic",85),(208,"Sophia Johns","F","Science",NULL);
```

**Output:**

<img width="1237" height="322" alt="Screenshot 2026-08-10 182729" src="https://github.com/user-attachments/assets/96a14840-8bd4-420f-8627-e9ffe9edca32" />


**Question 3**
---
<img width="1235" height="427" alt="Screenshot 2026-08-10 182753" src="https://github.com/user-attachments/assets/7226c653-5fea-4cbe-bdf5-7978ed7518e5" />


```sql
CREATE TABLE Invoices(
InvoiceID INTEGER PRIMARY KEY,
InvoiceDate Date,
DueDate DATE CHECK(DueDate>InvoiceDate),
Amount REAL check(Amount>0));

```

**Output:**

<img width="1226" height="300" alt="image" src="https://github.com/user-attachments/assets/1dfb0689-833b-4a51-aa42-d9d2cc95e4cf" />


**Question 4**
---
<img width="1238" height="418" alt="Screenshot 2026-08-10 182952" src="https://github.com/user-attachments/assets/204c7c88-966b-4ae5-b7ac-8dd63178bded" />


```sql
INSERT INTO Products SELECT * FROM Discontinued_products;
```

**Output:**
<img width="1241" height="305" alt="Screenshot 2026-08-10 183017" src="https://github.com/user-attachments/assets/4c14ae8a-2151-4dd6-9136-30ecc84af733" />



**Question 5**
---
<img width="1252" height="506" alt="image" src="https://github.com/user-attachments/assets/e0fe2c50-75d7-4dee-a123-da03942c3cf8" />


```sql
CREATE TABLE Employees(
EmployeeID INTEGER,
FirstName TEXT,
LastName TEXT,
HireDate DATE);

```

**Output:**
<img width="1240" height="337" alt="image" src="https://github.com/user-attachments/assets/9332dae2-5714-40b3-a35b-65881a0d033c" />



**Question 6**
---
<img width="1235" height="392" alt="image" src="https://github.com/user-attachments/assets/5c5ef5cc-a7da-44de-924e-b9e82a40d843" />


```sql
CREATE TABLE Bonuses(
BonusID INTEGER PRIMARY KEY,
EmployeeID INTEGER,
BonusAmount REAL CHECK(BonusAmount>0),
BonusDate DATE,
Reason TEXT NOT NULL,
FOREIGN KEY (EmployeeID) REFERENCES Employees(EmployeeID));
```

**Output:**

<img width="1240" height="337" alt="Screenshot 2026-08-10 183142" src="https://github.com/user-attachments/assets/ed8866b9-0a18-4b1d-8202-058320371854" />


**Question 7**
---
<img width="1252" height="506" alt="Screenshot 2026-08-10 183111" src="https://github.com/user-attachments/assets/9998d262-e335-40f8-a940-cd2496bb0b15" />


```sql
create table ProjectAssignments(
    AssignmentID integer primary key,
    EmployeeID integer,
    ProjectID integer,
    AssignmentDate date NOT NULL,
    foreign key (EmployeeID) references Employees(EmployeeID),
    foreign key (ProjectID) references Projects(ProjectID)
);
```

**Output:**
<img width="1240" height="337" alt="Screenshot 2026-08-10 183142" src="https://github.com/user-attachments/assets/495cfa3c-ff1e-4e84-8688-a40ebbdf449b" />


**Question 8**
---
<img width="1227" height="642" alt="image" src="https://github.com/user-attachments/assets/73df7348-66b6-4020-bf10-cbc0c3e7885c" />


```sql
alter table customer
add column email VARCHAR(100) 
```

**Output:**
<img width="1240" height="337" alt="Screenshot 2026-08-10 183142" src="https://github.com/user-attachments/assets/0988070f-5dd2-4590-aefb-df2c6c585861" />



**Question 9**
---
<img width="1237" height="495" alt="image" src="https://github.com/user-attachments/assets/92cd0393-8052-4b1c-b41b-906f81345dc0" />


```sql
insert into Customers (CustomerID,Name,Address)
values (304,"Peter Parker","Spider St");
```

**Output:**

<img width="1241" height="322" alt="image" src="https://github.com/user-attachments/assets/83cc861b-3dfb-43c2-b02b-fa03a42326fc" />


**Question 10**
---
<img width="1252" height="506" alt="Screenshot 2026-08-10 183111" src="https://github.com/user-attachments/assets/b5058eb2-fbe8-4c35-80c9-11e3e58e308a" />


```sql
create table Employees(
    EmployeeID integer primary key,
    FirstName varchar(50) not null,
    LastName varchar(50) not null,
    Email varchar(50) UNIQUE,
    Salary integer check(Salary>0),
    DepartmentID integer,
    foreign key (DepartmentID) references Departments(DepartmentID)
);
```

**Output:**

<img width="1240" height="337" alt="Screenshot 2026-08-10 183142" src="https://github.com/user-attachments/assets/4bf97dfd-95bb-4bf1-9c63-8485ac479b82" />


**MODULE-1 SEB:**
<img width="1887" height="852" alt="Screenshot 2026-08-10 184040" src="https://github.com/user-attachments/assets/b658b3f0-c2ae-4051-8fbc-fa5ea090b079" />



## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
