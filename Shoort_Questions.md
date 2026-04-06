# 📝 MySQL Course – Complete Short Questions & Answers (100 Questions)

## Exam Important Indicators

| Symbol | Meaning |
|--------|---------|
| ✅ | High probability – must know |
| ⭐ | Logical/application question – think before answering |
| 🔁 | Repeatedly asked in exams |

---

## MODULE 1: Database Basics (Questions 1-10)

**Q1.** ✅ What is the difference between **data** and **information**?  
**Ans:** Data is raw, unorganized facts (e.g., "Ali", 22). Information is processed data with meaning (e.g., "Ali is 22 years old").

**Q2.** ✅ Define DBMS. Give two examples.  
**Ans:** DBMS is software to create, manage, and use databases. Examples: MySQL, Oracle.

**Q3.** What is **metadata**? Give an example.  
**Ans:** Data about data. Example: Column name "StudentName" with data type VARCHAR(50) is metadata.

**Q4.** ✅ List three advantages of DBMS over file systems.  
**Ans:** 1) Reduced redundancy, 2) Data sharing, 3) Better security.

**Q5.** ⭐ Why can't we store student photos directly in a VARCHAR column?  
**Ans:** VARCHAR stores text only. For images, use BLOB (Binary Large Object) data type.

**Q6.** 🔁 What is the default MySQL port number?  
**Ans:** 3306

**Q7.** ✅ What command checks MySQL version?  
**Ans:** `mysql --version`

**Q8.** ⭐ A company has 3 branches. Without a DBMS, each branch maintains its own customer list. What problem will occur?  
**Ans:** Data redundancy and inconsistency – same customer may have different contact details across branches.

**Q9.** What is **program-data independence**?  
**Ans:** Changes in database structure do not require changes in application programs.

**Q10.** 🔁 Name three types of database users.  
**Ans:** End users, Application programmers, Database Administrators (DBA).

---

## MODULE 2: Database Design (Questions 11-30)

**Q11.** ✅ Define **Primary Key**.  
**Ans:** A column (or set of columns) that uniquely identifies each row in a table. Cannot be NULL.

**Q12.** ✅ Define **Foreign Key**.  
**Ans:** A column in one table that references the PRIMARY KEY of another table.

**Q13.** ⭐ Can a foreign key accept NULL values? Why?  
**Ans:** Yes, because a row may not have a related parent record (e.g., an order without a customer).

**Q14.** 🔁 What is the difference between **Candidate Key** and **Primary Key**?  
**Ans:** Candidate keys are all columns that can uniquely identify a row. Primary key is one selected candidate key.

**Q15.** ✅ What is **1NF**?  
**Ans:** First Normal Form requires that each column contains atomic (indivisible) values – no repeating groups or multi-valued attributes.

**Q16.** ✅ What is **2NF**?  
**Ans:** Second Normal Form requires 1NF + no partial dependencies (non-key attributes must depend on the entire candidate key).

**Q17.** ✅ What is **3NF**?  
**Ans:** Third Normal Form requires 2NF + no transitive dependencies (non-key attributes cannot depend on other non-key attributes).

**Q18.** 🔁 What is **BCNF**? How is it different from 3NF?  
**Ans:** Boyce-Codd Normal Form requires that for every functional dependency X → Y, X must be a candidate key. Stricter than 3NF.

**Q19.** ⭐ A table has columns: `OrderID, ProductID, ProductName`. `ProductName` depends only on `ProductID`, not the full key. Which normal form is violated?  
**Ans:** 2NF (partial dependency violation).

**Q20.** ⭐ A table has: `StudentID → AdvisorID → AdvisorName`. Which normal form is violated?  
**Ans:** 3NF (transitive dependency).

**Q21.** 🔁 What is an **Entity Relationship Diagram (ERD)**?  
**Ans:** A graphical representation of entities, attributes, and relationships in a database.

**Q22.** ⭐ In a university database, what relationship exists between **Student** and **Course**?  
**Ans:** Many-to-many (M:N) – one student takes many courses, one course has many students.

**Q23.** ✅ How do you resolve a many-to-many relationship in a relational database?  
**Ans:** Create an associative/bridge table (e.g., Enrollment) containing foreign keys from both tables.

**Q24.** 🔁 What is **referential integrity**?  
**Ans:** A rule ensuring that a foreign key value must match an existing primary key value or be NULL.

**Q25.** ⭐ What happens if you try to delete a customer who has existing orders, with a foreign key constraint `ON DELETE RESTRICT`?  
**Ans:** The DELETE fails – you must delete orders first or change the constraint.

**Q26.** ✅ What is the difference between **DELETE CASCADE** and **SET NULL**?  
**Ans:** CASCADE deletes child records; SET NULL sets foreign key to NULL.

**Q27.** ⭐ A `Student` table has `StudentID (PK)`, `Name`, `Email`. `Email` is unique. Can `Email` be a candidate key?  
**Ans:** Yes, it can uniquely identify a student, so it's a candidate key (but not necessarily chosen as primary key).

**Q28.** 🔁 What is a **composite key**? Give example.  
**Ans:** A primary key made of two or more columns. Example: `(OrderID, ProductID)` in OrderItems table.

**Q29.** ✅ What is **functional dependency**?  
**Ans:** When one attribute uniquely determines another. Example: `StudentID → StudentName`.

**Q30.** ⭐ In a `Products` table, `ProductID → ProductName, Price`. Is `Price` functionally dependent on `ProductID`?  
**Ans:** Yes, because each product has one price.

---

## MODULE 3: SQL Operations (Questions 31-50)

**Q31.** 🔁 Write SQL to create a database named `SchoolDB`.  
```sql
CREATE DATABASE SchoolDB;
## SQL Practice Questions (Q33–Q100)

### Q33. Insert a new student
```sql
INSERT INTO Students (StudentID, Name, Age) VALUES (101, 'Ahmed', 20);
```

### Q34. Update Ahmed's age
```sql
UPDATE Students SET Age = 21 WHERE Name = 'Ahmed';
```

### Q35. Delete students older than 25
```sql
DELETE FROM Students WHERE Age > 25;
```

### Q36. Names starting with 'A'
```sql
SELECT * FROM Students WHERE Name LIKE 'A%';
```

### Q37. Students aged 18–22
```sql
SELECT * FROM Students WHERE Age BETWEEN 18 AND 22;
```

### Q38. Count total students
```sql
SELECT COUNT(*) FROM Students;
```

### Q39. Average age
```sql
SELECT AVG(Age) FROM Students;
```

### Q40. Sort by name (DESC)
```sql
SELECT * FROM Students ORDER BY Name DESC;
```

### Q41. Top 3 oldest students
```sql
SELECT * FROM Students ORDER BY Age DESC LIMIT 3;
```

### Q42. WHERE vs HAVING
WHERE filters rows before grouping; HAVING filters after GROUP BY.

### Q43. Count students per age
```sql
SELECT Age, COUNT(*) FROM Students GROUP BY Age;
```

### Q44. Age groups with more than 5 students
```sql
SELECT Age, COUNT(*) FROM Students GROUP BY Age HAVING COUNT(*) > 5;
```

### Q45. Subquery example
```sql
SELECT Name FROM Students WHERE Age > (SELECT AVG(Age) FROM Students);
```

### Q46. Students with no orders
```sql
SELECT * FROM Students 
WHERE StudentID NOT IN (SELECT DISTINCT StudentID FROM Orders);
```

### Q47. INNER JOIN
```sql
SELECT s.Name, o.OrderID 
FROM Students s 
INNER JOIN Orders o ON s.StudentID = o.StudentID;
```

### Q48. LEFT JOIN
```sql
SELECT s.Name, o.OrderID 
FROM Students s 
LEFT JOIN Orders o ON s.StudentID = o.StudentID;
```

### Q49. DISTINCT
Returns unique city names (no duplicates).

### Q50. Remove duplicates
Create a new table using DISTINCT, then replace old table.

---

## MODULE 4: Views

### Q51. View
A virtual table based on a SELECT query.

### Q52. Create view
```sql
CREATE VIEW vw_StudentContact AS 
SELECT Name, Email FROM Students;
```

### Q53. Update via join view
Generally not allowed due to ambiguity.

### Q54. Delete view
```sql
DROP VIEW vw_StudentContact;
```

### Q55. Why use views
Security, simplicity, abstraction.

---

## MODULE 5: Indexing

### Q56. Index
Speeds up data retrieval.

### Q57. Create index
```sql
CREATE INDEX idx_name ON Students(Name);
```

### Q58. Why indexes slow writes
They must also be updated.

### Q59. UNIQUE index
Prevents duplicates.

### Q60. Create unique index
```sql
CREATE UNIQUE INDEX idx_email ON Students(Email);
```

### Q61. When not to use index
Small tables, duplicate-heavy columns.

### Q62. Composite index
Index on multiple columns.

### Q63. Drop index
```sql
DROP INDEX idx_name ON Students;
```

### Q64. Query execution plan
```sql
EXPLAIN SELECT * FROM Students;
```

### Q65. Primary key index
Automatically created.

---

## MODULE 6: Partitioning

### Q66. Partitioning
Dividing large tables.

### Q67. Types
RANGE, LIST, HASH, KEY.

### Q68. Best for dates
RANGE.

### Q69. Rule
Partition column must be in PRIMARY KEY.

### Q70. RANGE partition example
```sql
CREATE TABLE Orders (
    OrderID INT,
    OrderDate DATE,
    PRIMARY KEY (OrderID, OrderDate)
)
PARTITION BY RANGE (YEAR(OrderDate)) (
    PARTITION p2024 VALUES LESS THAN (2025),
    PARTITION p2025 VALUES LESS THAN (2026)
);
```

### Q71. Composite partition
Multiple partition levels.

### Q72. Foreign key restriction
Not allowed with partitioning.

---

## MODULE 7: Security

### Q73. Create user
```sql
CREATE USER 'appuser'@'localhost' IDENTIFIED BY 'pass123';
```

### Q74. Grant privileges
```sql
GRANT SELECT, INSERT ON SchoolDB.* TO 'appuser'@'localhost';
```

### Q75. Revoke privilege
```sql
REVOKE DELETE ON SchoolDB.* FROM 'appuser'@'localhost';
```

### Q76. Apply changes
```sql
FLUSH PRIVILEGES;
```

### Q77. Delete user
```sql
DROP USER 'appuser'@'localhost';
```

### Q78. Show privileges
```sql
SHOW GRANTS FOR 'appuser'@'localhost';
```

### Q79. GRANT ALL vs specific
ALL = full access; specific = limited.

### Q80. Default superuser
root

---

## MODULE 8: Transactions

### Q81. Transaction
Group of SQL statements.

### Q82. Money transfer
```sql
START TRANSACTION;
UPDATE Accounts SET Balance = Balance - 500 WHERE AccountID = 1;
UPDATE Accounts SET Balance = Balance + 500 WHERE AccountID = 2;
COMMIT;
```

### Q83. ROLLBACK after COMMIT
No effect.

### Q84. ACID
Atomicity, Consistency, Isolation, Durability.

### Q85. Atomicity
All or nothing.

### Q86. Dirty read
Reading uncommitted data.

### Q87. Prevent dirty reads
READ COMMITTED.

### Q88. Default isolation
REPEATABLE READ.

### Q89. Backup types
Full vs Incremental.

### Q90. Navicat backup
Right-click → Dump SQL.

### Q91. FOR UPDATE
Locks rows.

### Q92. Lost update
Overwritten updates.

### Q93. Set isolation
```sql
SET SESSION TRANSACTION ISOLATION LEVEL READ COMMITTED;
```

### Q94. TRUNCATE rollback
Not possible.

### Q95. COMMIT vs ROLLBACK
COMMIT saves; ROLLBACK undoes.

---

## LOGICAL QUESTIONS

### Q96. Most expensive product per category
```sql
SELECT CategoryID, MAX(Price) FROM Products GROUP BY CategoryID;
```

### Q97. Customers with >3 orders
```sql
SELECT CustomerID, COUNT(*) 
FROM Orders 
GROUP BY CustomerID 
HAVING COUNT(*) > 3;
```

### Q98. Employee-manager (self join)
```sql
SELECT e.Name AS Employee, m.Name AS Manager
FROM Employees e
LEFT JOIN Employees m 
ON e.ManagerID = m.EmployeeID;
```

### Q99. Second highest price
```sql
SELECT MAX(Price) 
FROM Products 
WHERE Price < (SELECT MAX(Price) FROM Products);
```

### Q100. Orders per month (2025)
```sql
SELECT MONTH(OrderDate), COUNT(*) 
FROM Orders 
WHERE YEAR(OrderDate) = 2025 
GROUP BY MONTH(OrderDate);
```
