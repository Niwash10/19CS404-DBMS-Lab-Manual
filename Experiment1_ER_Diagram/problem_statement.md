# ER Diagram Workshop – Submission Template

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure including entities, relationships, attributes, and constraints.

---

# Scenario A: City Fitness Club Management

**Business Context:**  
FlexiFit Gym wants a database to manage its members, trainers, and fitness programs.

**Requirements:**  
- Members register with name, membership type, and start date.  
- Each member can join multiple programs (Yoga, Zumba, Weight Training).  
- Trainers assigned to programs; a program may have multiple trainers.  
- Members may book personal training sessions with trainers.  
- Attendance recorded for each session.  
- Payments tracked for memberships and sessions.

### ER Diagram:
<img width="1536" height="964" alt="image" src="https://github.com/user-attachments/assets/dfa19bbf-6048-4367-beb1-b7925b563008" />


### Entities and Attributes
<img width="1536" height="388" alt="image" src="https://github.com/user-attachments/assets/8aea5f42-7436-414e-86a5-844d5c9eea2e" />

### Relationships and Constraints
<img width="1536" height="360" alt="image" src="https://github.com/user-attachments/assets/0bb76f7b-27ea-4e16-bdca-124590e7f5ac" />

### Assumptions
```
1.Every Member has a unique Member_ID.
2.Every Program has a unique Program_ID.
3.Every Trainer has a unique Trainer_ID.
4.A member can enroll in multiple programs, and a program can have multiple members.
5.A trainer can conduct multiple programs, and a program can have multiple trainers.
6.Personal training sessions are booked between one member and one trainer.
7.Attendance is recorded separately for each member in each program.
```
---

# Scenario B: City Library Event & Book Lending System

**Business Context:**  
The Central Library wants to manage book lending and cultural events.

**Requirements:**  
- Members borrow books, with loan and return dates tracked.  
- Each book has title, author, and category.  
- Library organizes events; members can register.  
- Each event has one or more speakers/authors.  
- Rooms are booked for events and study.  
- Overdue fines apply for late returns.

### ER Diagram:
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/c024a7f3-9b01-49ef-a807-7764c46b001d" />

### Entities and Attributes
<img width="1536" height="372" alt="image" src="https://github.com/user-attachments/assets/a9319a37-2ab3-4b9b-96b0-9538cc089edb" />



### Relationships and Constraints
<img width="1536" height="380" alt="image" src="https://github.com/user-attachments/assets/5af13252-adad-4f0f-8a93-469e0875d0cc" />



### Assumptions
```
1.  Every Member, Book, Loan, Event, Speaker, Room, and Fine has a unique primary key.Amember can borrow multiple books, but each loan refers to one member and one book.
2. Amember may register for multiple library events.
3. Every event must have at least one speaker.
4. One room can host multiple events or study sessions at different times.
5. Overdue fines are applied only when books are returned after the due date.
```
---

# Scenario C: Restaurant Table Reservation & Ordering

**Business Context:**  
A popular restaurant wants to manage reservations, orders, and billing.

**Requirements:**  
- Customers can reserve tables or walk in.  
- Each reservation includes date, time, and number of guests.  
- Customers place food orders linked to reservations.  
- Each order contains multiple dishes; dishes belong to categories (starter, main, dessert).  
- Bills generated per reservation, including food and service charges.  
- Waiters assigned to serve reservations.

### ER Diagram:
<img width="1424" height="532" alt="image" src="https://github.com/user-attachments/assets/9122e41d-3928-447c-9a50-805c406a2c27" />


### Entities and Attributes
<img width="1528" height="280" alt="image" src="https://github.com/user-attachments/assets/9d55dc7a-4b5e-4cf4-a743-0407b97a7d5d" />



### Relationships and Constraints

<img width="1096" height="216" alt="image" src="https://github.com/user-attachments/assets/32e4694a-91c7-43c9-8a84-253bd4163a74" />


### Assumptions
```
1.Every Customer, Reservation, Table, Order, Dish, Category, Bill, and Waiter has a unique primary key.
2.A customer can make multiple reservations, but each reservation belongs to only one customer.
3.Each reservation is assigned to one table and one waiter.
4.A reservation may include one or more food orders.
5.Each order contains one or more dishes.
6.Every dish belongs to exactly one category (Starter, Main Course, or Dessert).
7.A bill is generated for each reservation and includes food charges, service charges, and the total amount.
8.Walk-in customers are recorded as reservations without prior booking.
```


## Instructions for Students

1. Complete **all three scenarios** (A, B, C).  
2. Identify entities, relationships, and attributes for each.  
3. Draw ER diagrams using **draw.io / diagrams.net** or hand-drawn & scanned.  
4. Fill in all tables and assumptions for each scenario.  
5. Export the completed Markdown (with diagrams) as **a single PDF**
