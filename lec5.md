## Data Redundancy


- Data redundancy occurs when the same piece of data is stored in multiple places within a database or across systems.

- It can be intentional (controlled) or accidental (uncontrolled).

- Impacts storage, consistency, and performance.

- Balancing redundancy is a key goal of database design.

- Uncontrolled Data Redundancy

- Happens accidentally due to poor database design.

- Typically found in non-normalized databases.

- Same data repeated unnecessarily across multiple tables/files.

### Causes

- Lack of normalization.

- Legacy systems where updates weren’t synchronized.

- Manual duplication by users.

- Poorly defined relationships between tables.

Problems

- Inconsistency: Different copies of data may not match (e.g., customer address updated in one table but not another).

- Wasted storage: Duplicate records increase database size unnecessarily.

- Complex maintenance: Updates, inserts, and deletes become error-prone.