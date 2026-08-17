# Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**
--
<img width="1452" height="744" alt="Screenshot 2026-08-17 105303" src="https://github.com/user-attachments/assets/7898dfdb-9f15-4a0a-b15d-881e18680db0" />


```sql
update Employees
set salary=salary+500 ,email='updated'
where job_id='SA_REP' and commission_pct>0.15;
```

**Output:**
<img width="1260" height="641" alt="image" src="https://github.com/user-attachments/assets/127ac183-e88f-4556-8189-f0340116419f" />


**Question 2**
---
<img width="1458" height="597" alt="image" src="https://github.com/user-attachments/assets/8e4941d2-7afe-470c-a3b6-c59fb10ad656" />


```sql
update products
set reorder_lvl=reorder_lvl*1.30
where category='Food' and quantity <(0.50*reorder_lvl);
```

**Output:**
<img width="1237" height="427" alt="image" src="https://github.com/user-attachments/assets/711b21af-0818-4523-acab-1d5ae525ed6d" />


**Question 3**
---
<img width="1422" height="402" alt="image" src="https://github.com/user-attachments/assets/bed21402-cba1-4d8b-8c28-fe52dc0683de" />


```sql
update suppliers
set supplier_name='A1 Suppliers'
where supplier_id=8;
```

**Output:**

<img width="1247" height="422" alt="image" src="https://github.com/user-attachments/assets/31f5fbfc-07d2-4a2c-8d7a-52aadb3f80e1" />


**Question 4**
---
<img width="1431" height="587" alt="image" src="https://github.com/user-attachments/assets/20b0c3a5-571b-4409-bbdd-ef6504edbdc1" />

```sql
update SALES
set total_sell_price=quantity*sell_price
where product_id=10;
```

**Output:**

<img width="1237" height="515" alt="image" src="https://github.com/user-attachments/assets/1e7050bf-b2c1-47a8-b910-f5e6e28e4981" />


**Question 5**
---
<img width="1432" height="572" alt="image" src="https://github.com/user-attachments/assets/e65ba782-caba-47f3-b0f4-30dec71f133b" />


```sql
update Products
set reorder_lvl=20
where quantity<10 and category='Snacks';
```

**Output:**
<img width="1277" height="598" alt="image" src="https://github.com/user-attachments/assets/1748a718-f782-4a4e-90e5-6f0415dba421" />


**Question 6**
---
<img width="1432" height="223" alt="image" src="https://github.com/user-attachments/assets/c696f070-8ba0-44c2-8fef-965423a11533" />


```sql
delete from Doctors
where specialization='Cardiology';
```

**Output:**
<img width="1227" height="432" alt="image" src="https://github.com/user-attachments/assets/5f0a26de-83b1-4c24-84fc-c21b50f9031c" />



**Question 7**
---
<img width="1428" height="591" alt="image" src="https://github.com/user-attachments/assets/f6169855-62d7-4f69-be84-846843a336d1" />


```sql
delete from Customer
where GRADE=2 AND CUST_NAME LIKE "M%" AND PAYMENT_AMT<3000;
```

**Output:**

<img width="1262" height="477" alt="image" src="https://github.com/user-attachments/assets/448d8a17-d4fb-43d5-8bef-1cf7fed67805" />


**Question 8**
---
<img width="1425" height="571" alt="image" src="https://github.com/user-attachments/assets/8b0a9558-8cd7-4ec4-9e21-2e8be5f29ed9" />


```sql
delete from Customer
where (GRADE=3 or AGENT_CODE='A008')AND OUTSTANDING_AMT<5000;
```

**Output:**

<img width="1251" height="451" alt="image" src="https://github.com/user-attachments/assets/d3f29507-ead2-46ff-bb7e-d309ad6d139b" />


**Question 9**
---
<img width="1422" height="578" alt="image" src="https://github.com/user-attachments/assets/ac7810b9-9d05-4757-94ef-60486c67006c" />


```sql
delete from Surgeries
where surgery_date="2024-02-28";
```

**Output:**

<img width="1267" height="427" alt="image" src="https://github.com/user-attachments/assets/82dd5e32-be57-4e2f-b195-11ff88211481" />


**Question 10**
---
<img width="1458" height="868" alt="image" src="https://github.com/user-attachments/assets/4ae37cde-d987-41c3-a74b-6fbc46664788" />


```sql
delete from Customer
where CUST_COUNTRY='India' and CUST_CITY !='Chennai';
```

**Output:**
<img width="1452" height="845" alt="image" src="https://github.com/user-attachments/assets/e4ff42cd-6025-47c5-9e02-9783a5d976e0" />

**SEB**


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
