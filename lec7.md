## Data Models



2. DAO (Data Access Object)

Definition:

- A design pattern that separates persistence logic from business logic.

- DAO objects provide CRUD operations (Create, Read, Update, Delete).

Characteristics:

- Encapsulates database access in a single class or set of classes.

- Application interacts with DAO, not with SQL directly.

Advantages:

- Easier maintenance and testing.

- Reduces code duplication.

- Allows switching databases with minimal changes.

Limitations:

- Can become verbose (many DAO classes for each entity).

- Needs mapping code between objects and DB tables.


3. DDO (Data Dictionary Object / Direct Data Object)

Definition:

- Refers to database metadata objects or structures that describe data.

- Example: Oracle’s DDOs represent tables, columns, indexes, constraints.

Usage:

- Allows applications to query the database schema itself.

- Useful for building tools (like query builders, schema analyzers).

Advantages:

- Provides structured way to interact with metadata.

- Supports automation (dynamic query generation).

Limitations:

- Vendor-specific (e.g., Oracle DDO vs. SQL Server system tables).

- Not always portable between DBMS.

Example:

- Querying Oracle’s data dictionary: