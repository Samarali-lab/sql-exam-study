# 📘 MySQL Course – Exam Important Long Questions

## Exam Importance Guide

| Symbol | Meaning |
|--------|--------|
| ✅ | MUST know – appears in almost every exam |
| ⭐ | Application-based – tests understanding |
| 🔁 | Frequently repeated question |
| 📝 | Diagram required |

---

## MODULE 1: Database Basics

### LQ1. ✅🔁 File System vs DBMS

| Aspect | File System | DBMS |
|--------|------------|------|
| Data Storage | Separate files | Centralized |
| Redundancy | High | Low |
| Consistency | Difficult | Maintained |
| Security | Limited | Strong |
| Sharing | Difficult | Easy |
| Dependence | High | Low |
| Backup | Manual | Automated |

---

### LQ2. ✅ Advantages of DBMS

- Reduces redundancy  
- Maintains consistency  
- Improves security  
- Supports concurrent access  
- Backup & recovery  
- Data independence  
- Data integrity  

---

### LQ3. 🔁 Three-Level Architecture

| Level | Name | Description |
|------|------|------------|
| 1 | Physical | Storage level |
| 2 | Logical | Structure |
| 3 | View | User perspective |

---

### LQ4. ✅ MySQL Installation Steps

1. Download installer  
2. Run setup  
3. Choose setup type  
4. Install components  
5. Configure server  
6. Set root password  
7. Test connection  

---

## MODULE 2: Database Design

### LQ5. ✅🔁📝 Normalization (1NF → 3NF)

**1NF:** Atomic values  
**2NF:** No partial dependency  
**3NF:** No transitive dependency  

---

### LQ6. ✅📝 ER Diagram (Library)

**Entities:** Reader, Book, Publisher, Borrowing  
**Relationships:**  
- Reader ↔ Book (M:N)  
- Book → Publisher (M:1)  

---

### LQ7. ✅ Types of Keys

| Key | Description |
|-----|------------|
| Primary | Unique identifier |
| Candidate | Possible PK |
| Alternate | Not selected |
| Foreign | Reference |
| Composite | Multiple columns |
| Unique | No duplicates |

---

### LQ8. 🔁 Functional Dependency

- X → Y means X determines Y  

**Types:**  
- Trivial  
- Non-trivial  
- Full  
- Partial  
- Transitive  

---

### LQ9. ✅ Referential Integrity

- FK must match PK  

**Rules:**  
- Insert valid FK  
- No delete if referenced  
- No update breaking relation  

---

## MODULE 3: SQL Operations

### LQ10. ✅🔁 SQL Joins

- INNER JOIN → matching rows  
- LEFT JOIN → all left  
- RIGHT JOIN → all right  
- CROSS JOIN → all combinations  

---

### LQ11. ✅ Library SQL Queries

```sql
SELECT * FROM Books WHERE Author='Ramez Elmasri';

SELECT MemberID, COUNT(*) 
FROM Borrowings 
GROUP BY MemberID 
HAVING COUNT(*) > 3;

SELECT m.Name, b.Title
FROM Members m
JOIN Borrowings br ON m.MemberID=br.MemberID
JOIN Books b ON br.BookID=b.BookID;
```

---

### LQ12. 🔁 GROUP BY & HAVING

- GROUP BY → groups data  
- HAVING → filters groups  

---

### LQ13. ✅ Subqueries

```sql
SELECT Name FROM Members
WHERE MemberID IN (SELECT MemberID FROM Borrowings);

SELECT Title FROM Books
WHERE Price > (SELECT AVG(Price) FROM Books);
```

---

## MODULE 4: Views

### LQ14. ✅🔁 Views

```sql
CREATE VIEW v AS SELECT Name FROM Students;
SELECT * FROM v;
DROP VIEW v;
```

**Advantages:** Security, simplicity, abstraction  

---

## MODULE 5: Indexing

### LQ15. ✅🔁 Indexing

```sql
CREATE INDEX idx_name ON Students(Name);
CREATE UNIQUE INDEX idx_email ON Students(Email);
EXPLAIN SELECT * FROM Students;
```

**Use:** Fast queries  
**Avoid:** Small tables, duplicate-heavy columns  

---

## MODULE 6: Partitioning

### LQ16. ✅ Partitioning Types

- RANGE  
- LIST  
- HASH  
- KEY  

```sql
PARTITION BY RANGE (YEAR(date))
```

---

## MODULE 7: Security

### LQ17. ✅🔁 User Management

```sql
CREATE USER 'user'@'localhost' IDENTIFIED BY 'pass';
GRANT SELECT ON db.* TO 'user'@'localhost';
REVOKE DELETE ON db.* FROM 'user'@'localhost';
DROP USER 'user'@'localhost';
```

---

## MODULE 8: Transactions

### LQ18. ✅🔁 ACID Properties

- Atomicity → all or nothing  
- Consistency → valid state  
- Isolation → no interference  
- Durability → permanent  

---

### LQ19. ✅ Concurrency Problems

- Lost update  
- Dirty read  
- Non-repeatable read  

**Solution:** Isolation levels  

---

### LQ20. 🔁 Transaction Example

```sql
START TRANSACTION;

INSERT INTO Borrowings VALUES (...);

UPDATE Inventory 
SET AvailableCopies = AvailableCopies - 1;

COMMIT;
-- OR
ROLLBACK;
```

---

## 📊 Summary

- Must memorize SQL syntax  
- Practice JOINs  
- Draw ERD & normalization  
- Understand ACID  
- Know WHERE vs HAVING  
- Practice transactions  
