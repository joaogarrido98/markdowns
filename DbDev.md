# Database development

> A quick guide through database development and SQL

## Relational Database

Data is organised in **tables**.
Each table has a **schema**.
All elements in a column are of the same datatype.

Example Table -> **Table name**

| Attribute | Attribute | Attribute |
| --------- | --------- | --------- |
| Data      | Data      | Data      |

All tables have:

- **Attributes** also called columns
- **Rows** also called tuple

### SQL

Relational databases are accessed using **SQL** (Standart Query Language)

#### SQL Parts

**Data Definition Language** (DDL)

- Create
- Alter
- Delete

Databases, tables and their attributes

**Data Manipulation Language** (DML)

- Add
- Remove
- Update
- Query

Rows in tables

**Transact-SQL**

- Intuitively do a sequence of SQL statements

### SQL DDL

> Words in SQL are not case sensitive

**Create a database**
Template:
`CREATE DATABASE _databasename_`

```sql
CREATE DATABASE comp207
```

**Create a table**
Template:

```
CREATE TABLE _Tablename_(
column1 datatype,
column2 datatype,
column 3 datatype
)
```

```sql
CREATE TABLE people(
id INT,
name VARCHAR(20),
birth DATE
)
```

**Delete tables**

```sql
DROP TABLE people
```

**Delete database**

```sql
DROP DATABASE comp207
```

**Modifying tables Add new column**

```sql
ALTER TABLE people ADD email VARCHAR(5)
```

**Modifying tables Modify column**

```sql
ALTER TABLE people MODIFY email VARCHAR(255)
```

**Modifying tables Delete column**

```sql
ALTER TABLE people DROP COLUMN email
```

#### Unique

> **Unique** in a table means that for each value, there is **at most one** row in the table where the attribute/set of attributes take that value

```sql
CREATE TABLE Employees(
    birthday DATE,
    name VARCHAR(100),
    surname VARCHAR(100),
    CONSTRAINT UC_Employees UNIQUE(birthday, name)
)
```

This means that we could have two employees with the same name but not the same name and same birthday

#### Primary Key

> **Primary keys** must be unique (in the same sense as the **unique** constraint) and there can only be 1 primary key per table (there can be many unique attributes/sets of attributes)

```sql
CREATE TABLE Employees(
    id INT,
    birthday DATE,
    name VARCHAR(100),
    surname VARCHAR(100),
    CONSTRAINT PK_Employees PRIMARY KEY (id)
)
```

#### Foreign Key

> A **foreign key** is used to link two tables together explicitly

```sql
CREATE TABLE Employees(
    id INT,
    birthday DATE,
    name VARCHAR(100),
    surname VARCHAR(100),
    CONSTRAINT PK_Employees PRIMARY KEY (id)
)
```

```sql
CREATE TABLE Transaction(
    emp INT,
    CONSTRAINT FK_Transactions FOREIGN KEY (emp) REFERENCES Employees(id)
)
```

### Datatypes

- INT => Integers
- FLOAT => Decimal Numbers
- CHAR(x) => x is an integer, fixed length string
- VARCHAR(x) => x is an integer, variable length string
- DATE => Dates, YYYY-MM-DD
- DATETIME => Time and dates
- XML => XML files
- BLOB => Binary files

### SQL DML

> Data manipulation language

- Insert
- Delete
- Update
- Query

#### Insert

**Basic insert**

```sql
INSERT INTO Students VALUES('Name', birthday);
```

**Column Insert**

```sql
INSERT INTO Students(name) VALUES('Name');
```

#### Delete

**Basic Delete**

```sql
DELETE FROM Students WHERE name = "Name";
```

```sql
DELETE FROM Students WHERE name IN ('john', 'sebastian');
```

### Update

**Basic Update**

```sql
UPDATE Students set name = "joao" WHERE name = "sebastian";
```

#### Conditions in WHERE clauses

- **AND**
  - `WHERE name = "oliver" AND day = 45`
- **OR**
  - `WHERE name = "oliver" OR day = 45`
- **NOT**
  - `WHERE NOT name = "oliver"`
- **BETWEEN**
  - `WHERE day BETWEEN 1 AND 10`
- **LIKE**
  - `WHERE name LIKE ‘O%r’`

## QUERIES

> Queries in SQL have required and optional forms

**Required**

- SELECT
- FROM

**Optional**

- WHERE
- GROUP BY
- HAVING
- ORDER BY

### Types of query

**Selects everything from table students**

```sql
SELECT * FROM Students;
```

**Selects specific column**

```sql
SELECT name FROM Students;
```

**DISTINCT - Selects all different values of the same column**

```sql
SELECT DISTINCT name FROM Students;
```

**AS - Renames a column selected**

```sql
SELECT name AS fullname FROM Students;
```

**Creating new columns**

```sql
SELECT name, price * number AS total_cost FROM Students;
```

**NATURAL JOIN**

```sql
SELECT * FROM Students NATURAL JOIN Grades;
```
