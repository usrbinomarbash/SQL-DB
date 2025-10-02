# Object–Relational Mapping (ORM)

## 1. Introduction

- **Definition**:
  - ORM is a programming technique that lets developers interact with relational databases using **objects** instead of SQL queries.
  - It maps **tables → classes**, **rows → objects**, and **columns → attributes**.

- **Purpose**:
  - Bridge the gap between **object-oriented programming (OOP)** and **relational databases (RDBMS)**.

- **Popular ORM tools**:
  - Java → Hibernate, JPA
  - Python → SQLAlchemy, Django ORM
  - C#/.NET → Entity Framework
  - Ruby → ActiveRecord

---

## 2. How ORM Works

- **Mapping**:
  - Tables → Classes
  - Rows → Instances
  - Columns → Attributes


- **SQL generation**:
  - Developers call methods (`save`, `delete`, `query`) instead of writing SQL.
  - ORM auto-generates the required SQL.

**Example (Python, SQLAlchemy):**
```python
from sqlalchemy import Column, Integer, String
from sqlalchemy.ext.declarative import declarative_base

Base = declarative_base()

class Student(Base):
    __tablename__ = 'students'
    id = Column(Integer, primary_key=True)
    name = Column(String)
    gpa = Column(Integer)
```