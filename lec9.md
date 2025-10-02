##  SQL Transactions


- **Definition**:
  - A transaction is a logical **unit of work** consisting of one or more SQL statements.
  - Ensures either **all operations succeed (COMMIT)** or **none at all (ROLLBACK)**.

- **Goal**:
  - Guarantee **data consistency and integrity**, especially in multi-user environments.

---

## 2. ACID Properties


- **Atomicity**:
  - "All or nothing": if one operation fails, rollback everything.
- **Consistency**:
  - Database constraints and rules remain valid after execution.
- **Isolation**:
  - Concurrent transactions behave as if executed sequentially.
- **Durability**:
  - Once committed, changes persist even after crashes.

---

## 3. Transaction Control Commands


- **BEGIN / START TRANSACTION**:
  - Opens a new transaction block.
- **COMMIT**:
  - Makes all changes permanent.
- **ROLLBACK**:
  - Cancels changes since the last `BEGIN`.
- **SAVEPOINT**:
  - Creates a checkpoint inside a transaction for partial rollback.
- **SET TRANSACTION**:
  - Defines properties (e.g., isolation level).



## 4. Isolation Levels

- **Read Uncommitted**:
  - Allows dirty reads (rarely used).

- **Read Committed**:
  - Prevents dirty reads; non-repeatable reads may occur.

- **Repeatable Read**:
  - Prevents dirty & non-repeatable reads; phantom reads possible.

- **Serializable**:
  - Strictest isolation; transactions execute as if sequential.

---

## 5. Example: Bank Transfer
```sql
BEGIN;

UPDATE accounts
SET balance = balance - 500
WHERE account_id = 1;

UPDATE accounts
SET balance = balance + 500
WHERE account_id = 2;

COMMIT;
```