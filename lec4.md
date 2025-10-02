# Lecture Notes: Queries and Introduction to SQL

## 1. Introduction to SQL
- **What is SQL?**
  - SQL = *Structured Query Language*
  - Standard language for interacting with **Relational Database Management Systems (RDBMS)**
  - Used for:
    - Data definition
    - Data manipulation
    - Data retrieval (queries)
    - Data control

- **Core Components of SQL**
  - **DDL (Data Definition Language)** → `CREATE`, `ALTER`, `DROP`
  - **DML (Data Manipulation Language)** → `INSERT`, `UPDATE`, `DELETE`
  - **DQL (Data Query Language)** → `SELECT`
  - **DCL (Data Control Language)** → `GRANT`, `REVOKE`
  - **TCL (Transaction Control Language)** → `COMMIT`, `ROLLBACK`, `SAVEPOINT`

---

## 2. Queries in SQL

- **Definition**:
  - A *query* is a request for data or information from a database table or combination of tables.
  - Written primarily using the `SELECT` statement.

- **Basic Query Structure**:

  ```sql
  SELECT column1, column2,
  FROM table_name
  WHERE condition
  ORDER BY column;
```


```sql
SELECT first_name, last_name
FROM students
WHERE gpa > 3.5
ORDER BY last_name ASC;
```




