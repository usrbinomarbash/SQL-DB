### POSTGRES+SQL FUNDAMENTALS ... SU 63526

#### DATA TYPES IN PSQL

- bigserial(integer which autoincrements)
- bit [n]
- bit varying [ (n) ]
- boolean
- box
- cidr
- circle
- inet
- interval [ fields ] [ (p) ]
- json
- jsonb
- line
- lseg
- macaddr
- macaddr8
- money

- path
- pg_len
- point
- polygon

- smallserial
- serial
- text

- tsquery
- tsvector
- txid_snapshot
- uid
- xml

### Numeric Data Types:

- bit
- tinyint
- bool
- boolean
- smallint
- mediumint
- int
- integer
- bigint
- float
- numeric [ (p,s) ]
- double
- double precision
- decimal
- dec


### DATE/TIME Data Types:

- datetime
- date
- time
- timestamp
- year


### BINARY Data Types:

- binary
- varbinary
- varbinary(max)
- year


### String Data Types:

- CHAR
- varchar
- binary: argument is the column length
- varbinary: same as varchar but stores byte strings
- text(n): holds a string of length n 
- numeric [ (p,s) ]
- float
- real




#### How To Create A Table
```sql
CREATE TABLE nelanisacobollover(column_name + data_type + constraints)
```



### Creating A Table With Some Constraints
```sql
CREATE TABLE fortran32(
first_name VARCHAR(50),
last_name VARCHAR(50),
loves_cobol BOOLEAN,
day_he_discovered_ftn TIMESTAMP,)
```

### How To Create A Table
```sql
CREATE TABLE cobolfb(id int, first_name VARCHAR(50), last_name VARCHAR(50), gender VARCHAR(6), date_of_birth TIMESTAMP);
```



### Correct Way to Create a Table With Constraints
```sql
CREATE TABLE nelanftn56837(
id BIGSERIAL NOT NULL PRIMARY KEY,
first_name VARCHAR(50) NOT NULL,
last_name VARCHAR(50) NOT NULL,
loves_cobol BOOLEAN NOT NULL,
day_he_discovered_ftn TIMESTAMP NOT NULL,
email VARCHAR(50));
```


### How To Delete A Table
```sql
DROP TABLE tablename;
```

#### In My CASE
```sql
DROP TABLE nelanftn56837;
```

#### BIG SERIAL
- This is an autoincremented number


#### How To Insert Data in Record Without An Email
```sql
INSERT INTO fortran32(first_name, last_name, loves_cobol, day_he_discovered_ftn)
VaLUES("42932", "765262632", `TRUE`, DATE `2016-08-08`);
```

#### How To Insert Data in Record With An Email
```sql
INSERT INTO fortran32(first_name, last_name, loves_cobol, day_he_discovered_ftn, email)
VaLUES("42932", "765262632", `TRUE`, DATE `2016-08-08`, `chensung56837@gmail.com`);
```

#### How To Insert Records in Table Data Insert Into
```sql
INSERT INTO fortran32(first_name, last_name, loves_cobol, day_he_discovered_ftn)
VaLUES("Nelan", "Pascalfb", `TRUE`, DATE `2016-08-08`);
```

#### Selecting All Columns in My DB Table
```sql
SELECT * from mytable
```

#### Selecting Fname and City Columns in My DB
```sql
SELECT Fname,City from mytable
```


### My Table

| ClientId |  ClientUsername | ClientName | Address |City|Zip Code|Country|
|--------|--------|----------|----------|----------|----------|----------|
|1   |marjones2|Maria Jones|801 W 27th St|Dallas|78172|USA
|2   |andrewb1|Andrew Baker|922E Howard Lane|PflugervilleTX|78660|USA
|3   |mikesmith007|Michael Smith|Potsdamer Platz Str. 7|Berlin|10785 |Germany|
|4   |joedwards777|Joey Edwards|Spandauer Str. 2|Berlin|10178 |Germany|
|5   |roberto88|Roberto Lane|14 E 69th St  |New York, NY| 10021|USA|  
|6   |marianamarufo|Mariana Marufo| 279 E 15th St |Austin,TX|78778 |USA|


#### Update The Data
```sql
UPDATE Clients
SET ClientName = 'Mariana Perez', City= 'Brooklyn,NY'
WHERE ClientId = 6;
```

### How to modify the table and add a field

```sql
ALTER TABLE students ADD email VARCHAR(100);
```

#### Deleting A User From The Table
```sql
DELETE FROM Client WHERE ClientName='Mariana Marufo';
```

#### Sorting Data
```sql
SELECT * from fortran32 ORDER BY first_name ASC;
```

## Primary Keys
- A Column in the Table which uniquely identifies the a record in our table




### Sorting 

#### Sort by id

```sql
SELECT * from students ORDER BY id;
```


## Operators

#### 1 Is Not Equal To 2
```sql
SELECT 1 <> 2
```

#### Select the very first N people after a certain row thanks to the offset keyword
```sql
SELECT * from fortran32 OFFSET 5 LIMIT 5;
```

### Starting from the nth person query to the very end
```sql
SELECT * from fortran32 OFFSET 5;
```

### View only specific columns

```sql
SELECT name,major from students;
```

### List All the Databases
```sql
\l
```


### How To Create A Database(PREFERRED)
```sql
CREATE DATABASE nelanisacobol32;
```

### 2nd Way How To Create A Database
```sql
create database nelanisacobol32;
```


### 1st Way How To Connect To A Database using a username default port is 5432
```sql
psql -h localhost -p 5432 -u nelanslovecs nelanisacobol32;
```


### Show the list of roles of users in the db

```sql
\du
```

### Add Role to user

```sql
ALTER ROLE omarb REPLICATION;
```

### Give role to create DB

```sql
ALTER ROLE omarb CREATEDB;
```


### Give role to become super user

```sql
ALTER ROLE omarb SUPERUSER;
```


### Defining the primary key and foreign key

```sql
CREATE TABLE students(
    id SERIAL PRIMARY KEY,
    name VARCHAR(50),
    major VARCHAR(30),
    gpa NUMERIC(3,2),
    enrollment_yr INT
);
```


### View al the tables in the db

```sql
\dt
```

### Add elements to database STEP 1

```sql
INSERT INTO students(name,major, gpa, enrollment)
```

### Add the values to columns STEP 2

```
VALUES("Youssef","GE", 3.7,2024);
```


### Update

```sql
UPDATE students
SET GPA = 2.9
WHERE name = 'Josephine';
```