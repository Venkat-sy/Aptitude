# Database Management Systems (DBMS)

## Part 1: Quick Short Notes (Fundamentals)

### 1. DBMS Fundamentals
*   **Database:** Organized collection of structured data.
*   **DBMS:** Software that interacts with end-users, applications, and the database itself to capture and analyze the data (e.g., MySQL, Oracle, MongoDB).
*   **Advantages over File System:** Data independence, efficient data access, data integrity and security, concurrent access, crash recovery.
*   **Data Models:** Relational (Tables), Hierarchical (Tree), Network (Graph), Object-Oriented.
*   **Schemas:** Overall design of the database (Physical, Logical, View level).
*   **Instances:** The data stored in the database at a particular moment in time.

### 2. ER Model (Entity-Relationship)
*   **Entity:** A real-world object (e.g., Student, Course). Represented by a Rectangle.
*   **Attribute:** Properties of an entity (e.g., Roll No, Name). Represented by an Oval.
    *   *Key Attribute:* Unique identifier (underlined).
    *   *Multivalued Attribute:* Can have multiple values (double oval).
    *   *Derived Attribute:* Derived from other attributes (dashed oval).
*   **Relationship:** Association between entities. Represented by a Diamond.
*   **Cardinality:** One-to-One (1:1), One-to-Many (1:N), Many-to-One (N:1), Many-to-Many (M:N).

### 3. Relational Databases
*   **Relation (Table):** Collection of rows and columns.
*   **Tuple (Row/Record):** A single entry in a table.
*   **Attribute (Column/Field):** A property of the relation.
*   **Domain:** Set of permitted values for an attribute.
*   **Degree:** Number of attributes in a relation.
*   **Cardinality (of a relation):** Number of tuples in a relation.

### 4. Keys & Constraints
*   **Super Key:** A set of one or more attributes that uniquely identify a tuple.
*   **Candidate Key:** A minimal Super Key (no redundant attributes).
*   **Primary Key:** A Candidate Key chosen by the database designer to identify tuples uniquely.
*   **Foreign Key:** An attribute in one table that refers to the Primary Key in another table (maintains referential integrity).
*   **Alternate Key:** Candidate keys that are not selected as the Primary Key.
*   **Constraints:** Rules enforced on data (NOT NULL, UNIQUE, CHECK, DEFAULT).

### 5. Normalization
*   **Goal:** Reduce data redundancy and improve data integrity. Eliminates insertion, update, and deletion anomalies.
*   **1NF:** All attributes must be atomic (no multi-valued attributes).
*   **2NF:** Must be in 1NF + no partial dependency (non-prime attributes must depend on the *entire* candidate key).
*   **3NF:** Must be in 2NF + no transitive dependency (non-prime attributes must not depend on other non-prime attributes).
*   **BCNF (Boyce-Codd NF):** Stricter version of 3NF. For every functional dependency $X \rightarrow Y$, $X$ must be a super key.

### 6. SQL Queries
*   **DDL (Data Definition Language):** CREATE, ALTER, DROP, TRUNCATE.
*   **DML (Data Manipulation Language):** INSERT, UPDATE, DELETE.
*   **DQL (Data Query Language):** SELECT.
*   **DCL (Data Control Language):** GRANT, REVOKE.
*   **TCL (Transaction Control Language):** COMMIT, ROLLBACK, SAVEPOINT.
*   **Order of Execution:** FROM $\rightarrow$ WHERE $\rightarrow$ GROUP BY $\rightarrow$ HAVING $\rightarrow$ SELECT $\rightarrow$ ORDER BY.

### 7. Joins
*   **INNER JOIN:** Returns records that have matching values in both tables.
*   **LEFT (OUTER) JOIN:** Returns all records from the left table, and matched records from the right table.
*   **RIGHT (OUTER) JOIN:** Returns all records from the right table, and matched records from the left table.
*   **FULL (OUTER) JOIN:** Returns all records when there is a match in either left or right table.
*   **CROSS JOIN:** Returns the Cartesian product of the two tables.
*   **NATURAL JOIN:** An INNER JOIN that automatically joins on all columns with the same name.

### 8. Transactions & ACID Properties
*   **Transaction:** A logical unit of work that consists of one or more SQL statements.
*   **ACID Properties:**
    *   **Atomicity:** "All or nothing". The transaction completes entirely or not at all.
    *   **Consistency:** The database must remain in a consistent state before and after the transaction.
    *   **Isolation:** Concurrent transactions execute without interfering with each other.
    *   **Durability:** Once a transaction is committed, changes are permanent, even in case of system failure.

### 9. Indexing
*   **Purpose:** Data structure that improves the speed of data retrieval operations on a database table.
*   **Drawback:** Slower writes (INSERT/UPDATE/DELETE) because the index must also be updated.
*   **Clustered Index:** Alters the physical arrangement of data rows in the table. A table can have only ONE clustered index (usually the Primary Key).
*   **Non-Clustered Index:** Creates a separate object that points to the original data rows. A table can have multiple non-clustered indexes.
*   **B-Trees:** The most common data structure used for database indexes.

---

## Part 2: Placement-Related MCQs

1. Which of the following is the highest level of abstraction in a Database Management System?

A) Physical Level

B) Logical Level

C) View Level

D) Conceptual Level

**Answer:** Option **C**

**Explanation:**

The View Level is the highest level of abstraction. It describes only part of the entire database and is concerned with how users interact with the system. It hides the complexity of the Logical and Physical levels from the end-user.

---

2. In an ER Model, a weak entity set is represented by:

A) A single rectangle

B) A double rectangle

C) A dashed rectangle

D) A diamond

**Answer:** Option **B**

**Explanation:**

In an Entity-Relationship (ER) diagram, a strong entity is represented by a single rectangle, whereas a weak entity (an entity that cannot be uniquely identified by its attributes alone and depends on a strong entity) is represented by a double rectangle.

---

3. Which of the following normal forms removes transitive dependencies?

A) First Normal Form (1NF)

B) Second Normal Form (2NF)

C) Third Normal Form (3NF)

D) Boyce-Codd Normal Form (BCNF)

**Answer:** Option **C**

**Explanation:**

Transitive dependency occurs when a non-prime attribute depends on another non-prime attribute rather than depending directly on the primary key. Third Normal Form (3NF) specifically dictates that there should be no transitive dependencies.

---

4. Which SQL command is used to remove all records from a table, including all spaces allocated for the records, but keeps the table structure intact?

A) DROP

B) DELETE

C) TRUNCATE

D) REMOVE

**Answer:** Option **C**

**Explanation:**

TRUNCATE is a DDL command that quickly removes all records from a table and resets auto-incrementing identities. Unlike DELETE (a DML command), it does not log individual row deletions, making it much faster. DROP removes the table structure entirely.

---

5. A transaction must either complete entirely or not at all. Which ACID property does this describe?

A) Atomicity

B) Consistency

C) Isolation

D) Durability

**Answer:** Option **A**

**Explanation:**

Atomicity ensures that a transaction is treated as a single, indivisible logical unit of work. If any part of the transaction fails, the entire transaction fails, and the database state is left unchanged ("All or nothing").

---

6. Which type of Join returns all rows from the left table and the matched rows from the right table?

A) INNER JOIN

B) LEFT OUTER JOIN

C) RIGHT OUTER JOIN

D) FULL OUTER JOIN

**Answer:** Option **B**

**Explanation:**

A LEFT OUTER JOIN (or simply LEFT JOIN) returns all records from the left table, and the matched records from the right table. If there is no match, the result is NULL on the right side.

---

7. Which of the following is true regarding a Clustered Index?

A) A table can have multiple clustered indexes.

B) It determines the physical order of data in a table.

C) It is stored completely separate from the actual data.

D) It is generally slower for range queries than a non-clustered index.

**Answer:** Option **B**

**Explanation:**

A clustered index physically sorts and stores the data rows in the table or view based on their key values. Because the data rows can be stored in only one physical order, a table can only have one clustered index.

---

8. In a relational database, what is a Candidate Key?

A) An attribute that can be NULL.

B) A minimal set of attributes that uniquely identifies a tuple.

C) Any set of attributes that uniquely identifies a tuple.

D) A key that establishes a relationship between two tables.

**Answer:** Option **B**

**Explanation:**

A Candidate Key is a minimal Super Key. It is a set of attributes that uniquely identifies a tuple, but from which no attribute can be removed without losing the uniqueness property.

---

9. What is the primary difference between the WHERE and HAVING clauses in SQL?

A) WHERE is used with SELECT, HAVING is used with UPDATE.

B) WHERE filters rows before aggregation, HAVING filters groups after aggregation.

C) HAVING filters rows before aggregation, WHERE filters groups after aggregation.

D) There is no difference; they can be used interchangeably.

**Answer:** Option **B**

**Explanation:**

The WHERE clause applies conditions to individual rows before the GROUP BY clause groups them. The HAVING clause applies conditions to the aggregated groups created by the GROUP BY clause.

---

10. What is a Deadlock in a database system?

A) When the database server crashes and shuts down.

B) When a transaction takes too long to execute and times out.

C) When two or more transactions are waiting for locks held by each other, causing a cycle of dependencies.

D) When a user forgets to COMMIT a transaction.

**Answer:** Option **C**

**Explanation:**

A deadlock is a situation where transaction A holds a lock on Resource 1 and is waiting for Resource 2, while transaction B holds a lock on Resource 2 and is waiting for Resource 1. Neither can proceed, resulting in a permanent block.

---

11. Which SQL command is part of the Data Control Language (DCL)?

A) UPDATE

B) GRANT

C) COMMIT

D) CREATE

**Answer:** Option **B**

**Explanation:**

Data Control Language (DCL) includes commands like GRANT and REVOKE, which are used to give or take away user permissions and privileges on database objects.

---

12. In the ER Model, a derived attribute is represented by:

A) A dashed oval

B) A double oval

C) A rectangle

D) An underlined oval

**Answer:** Option **A**

**Explanation:**

A derived attribute is one whose value can be derived from the values of other related attributes or entities (e.g., calculating Age from Date of Birth). It is represented by a dashed oval in an ER diagram.

---

13. What is the purpose of the Foreign Key in a relational database?

A) To uniquely identify a record in the same table.

B) To maintain referential integrity between two tables.

C) To automatically increment a counter for new records.

D) To index the table for faster searching.

**Answer:** Option **B**

**Explanation:**

A foreign key is a column or a group of columns in a relational database table that provides a link between data in two tables. It acts as a cross-reference between tables because it references the primary key of another table, thereby maintaining referential integrity.

---

14. Which property of a transaction ensures that concurrent transactions execute without interfering with each other?

A) Atomicity

B) Consistency

C) Isolation

D) Durability

**Answer:** Option **C**

**Explanation:**

Isolation ensures that the concurrent execution of transactions leaves the database in the same state that would have been obtained if the transactions were executed sequentially.

---

15. What type of anomaly occurs when deleting a row in a table results in the loss of other important, unrelated data?

A) Insertion Anomaly

B) Deletion Anomaly

C) Update Anomaly

D) Normalization Anomaly

**Answer:** Option **B**

**Explanation:**

A deletion anomaly occurs when the deletion of a record to remove certain information unexpectedly causes the loss of other entirely different and unrelated information because they are stored together in the same unnormalized table.

---

16. Which SQL clause is used to sort the result set in ascending or descending order?

A) GROUP BY

B) HAVING

C) ORDER BY

D) SORT BY

**Answer:** Option **C**

**Explanation:**

The ORDER BY clause is used to sort the result-set in ascending (ASC) or descending (DESC) order based on one or more columns.

---

17. If a table has a primary key consisting of multiple columns, it is called a:

A) Foreign Key

B) Composite Key

C) Alternate Key

D) Super Key

**Answer:** Option **B**

**Explanation:**

A composite key is a primary key that consists of two or more columns to uniquely identify a row in a table.

---

18. In SQL, the LIKE operator is used for:

A) Finding exact numeric matches

B) Pattern matching using wildcards

C) Comparing dates

D) Joining two tables

**Answer:** Option **B**

**Explanation:**

The LIKE operator is used in a WHERE clause to search for a specified pattern in a column, using wildcards such as '%' (zero or more characters) and '_' (a single character).

---

19. Which normal form dictates that all attributes in a relation must be atomic?

A) First Normal Form (1NF)

B) Second Normal Form (2NF)

C) Third Normal Form (3NF)

D) Boyce-Codd Normal Form (BCNF)

**Answer:** Option **A**

**Explanation:**

First Normal Form (1NF) requires that the values in each column of a table are atomic (indivisible). There can be no multi-valued attributes or repeating groups.

---

20. A B-Tree index is most efficient for which type of queries?

A) Exact match queries only

B) Range queries (e.g., BETWEEN, >, <)

C) Full-text search

D) Boolean queries

**Answer:** Option **B**

**Explanation:**

Because B-Trees store data in a sorted order, they are extremely efficient for both exact match queries and range queries (like retrieving all records where age is between 20 and 30).
