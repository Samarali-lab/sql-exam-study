# SQL Database Exam - Complete MCQ Bank

## MODULE 1: Database Basics

1. **What is the main purpose of a database?**
   - a) To create computer hardware
   - b) To store and organize data
   - c) To design networks
   - d) To develop operating systems

2. **Which of the following is NOT a characteristic of a database?**
   - a) Self-describing nature
   - b) Program-data independence
   - c) Multiple views of data
   - d) Fixed and rigid data structures

3. **A Database Management System (DBMS) is:**
   - a) A collection of related data
   - b) Software to manage databases
   - c) Computer hardware
   - d) A programming language

4. **What is metadata?**
   - a) Data about other data
   - b) Actual user data
   - c) Backup copies of data
   - d) Data stored in RAM

5. **Which is an example of a database application?**
   - a) MS Word
   - b) Gmail
   - c) Oracle
   - d) Photoshop

6. **Data redundancy means:**
   - a) Storing data once only
   - b) Storing same data multiple times
   - c) No data at all
   - d) Storing data in RAM only

7. **The three levels of database architecture are:**
   - a) Physical, logical, and view
   - b) Client, server, and user
   - c) Internal, external, and client
   - d) Primary, secondary, and tertiary

8. **Which type of users write database applications?**
   - a) Database administrators
   - b) End users
   - c) Application programmers
   - d) System analysts

9. **MySQL is an example of a:**
   - a) NoSQL database
   - b) Hierarchical database
   - c) Relational DBMS
   - d) File system

10. **The default port number for MySQL is:**
    - a) 1521
    - b) 1433
    - c) 3306
    - d) 8080

11. **Which SQL statement creates a new database?**
    - a) NEW DATABASE testdb
    - b) CREATE DATABASE testdb
    - c) MAKE DATABASE testdb
    - d) ADD DATABASE testdb

12. **Which GUI tool is the official Oracle tool for MySQL?**
    - a) Navicat
    - b) phpMyAdmin
    - c) MySQL Workbench
    - d) Toad

## MODULE 2: Database Design (ERD, Keys, Normalization)

13. **An ER diagram is used to represent:**
    - a) Normal forms
    - b) Data relationships and entities
    - c) SQL queries
    - d) Transaction logs

14. **In relational database design, a primary key is:**
    - a) A field that allows duplicate values
    - b) A field that uniquely identifies each record
    - c) A foreign key linking two tables
    - d) A non-unique index field

15. **Which is NOT a normal form?**
    - a) 1NF
    - b) 2NF
    - c) 3NF
    - d) 6NF

16. **In normalization, 1NF ensures:**
    - a) Each non-key attribute depends on the whole key
    - b) No transitive dependency
    - c) Each cell contains atomic values
    - d) All tables are linked by foreign keys

17. **The main purpose of normalization is to:**
    - a) Reduce redundancy and improve data integrity
    - b) Increase query speed
    - c) Decrease number of tables
    - d) Avoid foreign keys

18. **A foreign key is:**
    - a) A unique identifier within a table
    - b) A key that references a primary key in another table
    - c) An attribute that must not contain NULL
    - d) A surrogate key auto-generated

19. **Which is a many-to-many relationship example?**
    - a) Student – Course
    - b) Customer – Invoice
    - c) Employee – Department
    - d) Country – Capital

20. **In the PetStore example, which table most likely contains foreign keys referencing multiple tables?**
    - a) Pets
    - b) Orders
    - c) Customers
    - d) Products

21. **A candidate key that is not selected as primary key is called:**
    - a) Foreign key
    - b) Alternate key
    - c) Super key
    - d) Composite key

22. **Which normal form removes partial dependencies?**
    - a) 1NF
    - b) 2NF
    - c) 3NF
    - d) BCNF

23. **Which normal form removes transitive dependencies?**
    - a) 1NF
    - b) 2NF
    - c) 3NF
    - d) BCNF

24. **BCNF is stricter than 3NF because:**
    - a) LHS of every FD must be a candidate key
    - b) RHS of every FD must be non-prime
    - c) No multi-valued attributes allowed
    - d) All tables must have a single primary key

25. **A weak entity:**
    - a) Has its own primary key
    - b) Cannot exist without a strong entity
    - c) Always has a surrogate key
    - d) Cannot have foreign keys

26. **Referential integrity ensures:**
    - a) Primary keys are unique
    - b) Foreign key matches primary key or is NULL
    - c) No NULL values in any column
    - d) All tables are normalized

## MODULE 3: SQL Operations (DDL, DML, DQL)

27. **Which SQL statement retrieves data?**
    - a) INSERT
    - b) UPDATE
    - c) SELECT
    - d) DELETE

28. **Which SQL statement adds new rows?**
    - a) INSERT
    - b) UPDATE
    - c) SELECT
    - d) DELETE

29. **Which clause filters rows in a SELECT?**
    - a) GROUP BY
    - b) ORDER BY
    - c) WHERE
    - d) HAVING

30. **Which clause filters groups after aggregation?**
    - a) WHERE
    - b) GROUP BY
    - c) HAVING
    - d) ORDER BY

31. **What does LIKE '%abc%' match?**
    - a) Values ending with 'abc'
    - b) Values starting with 'abc'
    - c) Values containing 'abc' anywhere
    - d) Exact match 'abc'

32. **Which function returns the number of rows?**
    - a) SUM()
    - b) COUNT()
    - c) AVG()
    - d) TOTAL()

33. **An inner join returns:**
    - a) All rows from left table only
    - b) All rows from right table only
    - c) Only matching rows from both tables
    - d) All rows from both tables

34. **A left join returns:**
    - a) Only matching rows
    - b) All rows from left + matching right
    - c) All rows from right + matching left
    - d) Cartesian product

35. **Which SQL keyword removes duplicate rows?**
    - a) UNIQUE
    - b) DISTINCT
    - c) DIFFERENT
    - d) SINGLE

36. **What does SELECT * FROM Products LIMIT 5; do?**
    - a) Returns first 5 columns
    - b) Returns first 5 rows
    - c) Returns rows 5 to 10
    - d) Returns 5 random rows

37. **A subquery is:**
    - a) A query inside another query
    - b) A query with no WHERE clause
    - c) A query that deletes data
    - d) A query that creates tables

38. **Which join returns all combinations of rows?**
    - a) INNER JOIN
    - b) LEFT JOIN
    - c) CROSS JOIN
    - d) RIGHT JOIN

39. **A self join joins:**
    - a) Two different tables
    - b) A table with itself
    - c) Three or more tables
    - d) A table with a view

## MODULE 4: Views

40. **A view is:**
    - a) A physical copy of data
    - b) A virtual table based on a SELECT query
    - c) A backup of a table
    - d) An index structure

41. **Which statement creates a view?**
    - a) MAKE VIEW
    - b) CREATE VIEW
    - c) NEW VIEW
    - d) ADD VIEW

42. **Which statement removes a view?**
    - a) DELETE VIEW
    - b) REMOVE VIEW
    - c) DROP VIEW
    - d) ERASE VIEW

43. **A simple view (single table, no aggregates) is typically:**
    - a) Read-only
    - b) Updatable
    - c) Indexed automatically
    - d) Stored on disk

44. **A view with joins and aggregates is usually:**
    - a) Updatable
    - b) Read-only
    - c) Faster than base tables
    - d) Automatically partitioned

## MODULE 5: Indexing

45. **An index is used to:**
    - a) Slow down queries
    - b) Speed up data retrieval
    - c) Encrypt data
    - d) Compress data

46. **Which index is automatically created on a primary key?**
    - a) Unique index
    - b) Fulltext index
    - c) Primary index
    - d) Composite index

47. **Which index prevents duplicate values?**
    - a) Normal index
    - b) Unique index
    - c) Fulltext index
    - d) Composite index

48. **An index on multiple columns is called:**
    - a) Simple index
    - b) Composite index
    - c) Fulltext index
    - d) Clustered index

49. **Indexes slow down which operations?**
    - a) SELECT only
    - b) INSERT, UPDATE, DELETE
    - c) CREATE DATABASE
    - d) DROP TABLE

50. **Which command removes an index?**
    - a) DELETE INDEX
    - b) REMOVE INDEX
    - c) DROP INDEX
    - d) ERASE INDEX

51. **Which keyword shows how MySQL executes a query?**
    - a) ANALYZE
    - b) EXPLAIN
    - c) DESCRIBE
    - d) SHOW PLAN

## MODULE 6: Partitioning

52. **Partitioning divides a table into:**
    - a) Multiple databases
    - b) Multiple smaller physical pieces
    - c) Multiple indexes
    - d) Multiple views

53. **Which partitioning type uses value ranges?**
    - a) LIST
    - b) HASH
    - c) RANGE
    - d) KEY

54. **Which partitioning type uses specific predefined values?**
    - a) RANGE
    - b) LIST
    - c) HASH
    - d) KEY

55. **Which partitioning distributes data evenly via a hash function?**
    - a) RANGE
    - b) LIST
    - c) HASH
    - d) KEY

56. **Partition column must be part of the:**
    - a) Foreign key
    - b) Primary key
    - c) Unique index
    - d) View definition

57. **Composite partitioning means:**
    - a) One level partitioning
    - b) Two levels of partitioning
    - c) No partitioning
    - d) Indexing only

## MODULE 7: Data Security (Users, Privileges)

58. **Which command creates a new user in MySQL?**
    - a) ADD USER
    - b) CREATE USER
    - c) NEW USER
    - d) MAKE USER

59. **Which privilege allows reading data?**
    - a) INSERT
    - b) UPDATE
    - c) SELECT
    - d) DELETE

60. **Which command gives privileges to a user?**
    - a) GIVE
    - b) GRANT
    - c) ALLOW
    - d) PERMIT

61. **Which command removes privileges?**
    - a) REMOVE
    - b) DELETE
    - c) REVOKE
    - d) DENY

62. **Which command removes a user?**
    - a) DELETE USER
    - b) REMOVE USER
    - c) DROP USER
    - d) ERASE USER

63. **After granting privileges, you should run:**
    - a) SAVE PRIVILEGES
    - b) FLUSH PRIVILEGES
    - c) REFRESH PRIVILEGES
    - d) APPLY PRIVILEGES

## MODULE 8: Backup, Restore & Transactions

64. **A full backup copies:**
    - a) Only changes
    - b) Only the schema
    - c) The entire database
    - d) Only indexes

65. **An incremental backup copies:**
    - a) The entire database
    - b) Only changes since last backup
    - c) Only the log files
    - d) Only primary keys

66. **In Navicat, backup is done via:**
    - a) Export → Dump SQL File
    - b) File → Save As
    - c) Tools → Compress
    - d) View → Backup

67. **A transaction is:**
    - a) A single SQL statement
    - b) A group of SQL statements executed as one unit
    - c) A backup operation
    - d) An index creation

68. **Which property ensures "all or nothing"?**
    - a) Consistency
    - b) Isolation
    - c) Atomicity
    - d) Durability

69. **Which property ensures changes persist after crash?**
    - a) Atomicity
    - b) Consistency
    - c) Isolation
    - d) Durability

70. **Which command saves a transaction permanently?**
    - a) SAVE
    - b) COMMIT
    - c) APPLY
    - d) PERMANENT

71. **Which command undoes a transaction?**
    - a) UNDO
    - b) CANCEL
    - c) ROLLBACK
    - d) REVERT

72. **A dirty read occurs when:**
    - a) Reading committed data
    - b) Reading uncommitted data that may be rolled back
    - c) Reading the same data twice
    - d) Reading encrypted data

73. **Which isolation level prevents dirty reads?**
    - a) READ UNCOMMITTED
    - b) READ COMMITTED
    - c) REPEATABLE READ (also works)
    - d) Both B and C

74. **MySQL default isolation level is:**
    - a) READ UNCOMMITTED
    - b) READ COMMITTED
    - c) REPEATABLE READ
    - d) SERIALIZABLE

75. **Row locking with FOR UPDATE prevents:**
    - a) SELECT on other rows
    - b) Other transactions from updating the same row
    - c) INSERT into the same table
    - d) DROP TABLE

---

## ANSWER KEY

| Q# | Ans | Q# | Ans | Q# | Ans | Q# | Ans | Q# | Ans |
|----|-----|----|-----|----|-----|----|-----|----|-----|
| 1  | B   | 16 | C   | 31 | C   | 46 | C   | 61 | C   |
| 2  | D   | 17 | A   | 32 | B   | 47 | B   | 62 | C   |
| 3  | B   | 18 | B   | 33 | C   | 48 | B   | 63 | B   |
| 4  | A   | 19 | A   | 34 | B   | 49 | B   | 64 | C   |
| 5  | C   | 20 | B   | 35 | B   | 50 | C   | 65 | B   |
| 6  | B   | 21 | B   | 36 | B   | 51 | B   | 66 | A   |
| 7  | A   | 22 | B   | 37 | A   | 52 | B   | 67 | B   |
| 8  | C   | 23 | C   | 38 | C   | 53 | C   | 68 | C   |
| 9  | C   | 24 | A   | 39 | B   | 54 | B   | 69 | D   |
| 10 | C   | 25 | B   | 40 | B   | 55 | C   | 70 | B   |
| 11 | B   | 26 | B   | 41 | B   | 56 | B   | 71 | C   |
| 12 | C   | 27 | C   | 42 | C   | 57 | B   | 72 | B   |
| 13 | B   | 28 | A   | 43 | B   | 58 | B   | 73 | D   |
| 14 | B   | 29 | C   | 44 | B   | 59 | C   | 74 | C   |
| 15 | D   | 30 | C   | 45 | B   | 60 | B   | 75 | B   |

---

## BONUS: Mixed Practice MCQs (Test Yourself)

76. **Which command shows all databases in MySQL?**
    - a) LIST DATABASES
    - b) DISPLAY DATABASES
    - c) SHOW DATABASES
    - d) VIEW DATABASES

77. **Which data type is best for storing exact monetary values?**
    - a) FLOAT
    - b) DOUBLE
    - c) DECIMAL
    - d) REAL

78. **A foreign key constraint with ON DELETE CASCADE does what?**
    - a) Prevents deletion of parent rows
    - b) Automatically deletes child rows when parent is deleted
    - c) Sets child foreign keys to NULL
    - d) Deletes the foreign key constraint

79. **What does UNION do?**
    - a) Joins two tables horizontally
    - b) Combines result sets from multiple SELECT statements vertically
    - c) Creates a new table from two existing ones
    - d) Merges two columns into one

80. **What is the difference between DELETE and TRUNCATE?**
    - a) DELETE is faster, TRUNCATE is slower
    - b) DELETE can have WHERE clause, TRUNCATE cannot
    - c) DELETE resets auto-increment, TRUNCATE does not
    - d) There is no difference
