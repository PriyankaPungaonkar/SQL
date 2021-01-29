## CREATE statement

There are two CREATE statements available in SQL:

1. CREATE DATABASE
2. CREATE TABLE

### 1. `CREATE DATABASE`

A Database is defined as a structured set of data. So, in SQL the very first step to store the data in a well structured manner is to create a database. The CREATE DATABASE statement is used to create a new database in SQL.

Syntax:
```sql
CREATE DATABASE database_name;
```
```
here, 
database_name: name of the database.
```

While naming the database, it is suggested to follow below standards.
* Use lowercase characters.
* Separate words and prefixes with underlines, never use spaces.
* Avoid using numbers.
* Keep it brief up to 8 characters.
* separate words by underscores.

Example : 
```sql
CREATE DATABASE my_database;
```
Once DATABASE is created, it can be used to store TABLES and VIEWS.

To check all the present databases, you can use `SHOW DATABASES`(in mysql) statement.

To select created DATABASE, you need to use `USE` command.

Example :
```sql
USE my_database;
```

### 2. CREATE TABLE
We have learned above about creating databases. Now to store the data we need a table to do that. 

The CREATE TABLE statement is used to create a table in SQL. 

We know that a table comprises of rows and columns. So while creating tables we have to provide all the information to SQL about the names of the columns, type of data to be stored in columns, size of the data etc

Syntax :
```
CREATE TABLE table_name
(
column1 data_type(size),
column2 data_type(size),
column3 data_type(size),
....
);

table_name:  name of the table.
column1 name of the first column.

data_type: Type of data we want to store in the particular column. 
            For example,int for integer data.

size: Size of the data we can store in a particular column. For example if for
a column we specify the data_type as int and size as 10 then this column can store an integer number of maximum 10 BYTES. 
```

Example :
```sql
CREATE TABLE Students
(
ROLL_NO int(3),
NAME varchar(20),
SUBJECT varchar(20),
);
```

## Adding constraints while creating a table

We can add [constraints](/Chapter_1/constraints.md) to fields while creating a table as follows.

Example :
```sql
CREATE TABLE Students
(
ROLL_NO int(3) NOT NULL,
STUDENT_NAME varchar(20) NOT NULL,
AGE SMALLINT(1) NOT NULL CHECK (AGE >= 18 AND AGE <=105),
SUBJECT varchar(20) UNIQUE NOT NULL ,
PRIMARY KEY(ROLL_NO)
);
```

To check the structure of created table , You can use `DESC` command in MySQL.

Example :
```
mysql> DESC Students;
+---------+-------------+------+-----+---------+-------+
| Field   | Type        | Null | Key | Default | Extra |
+---------+-------------+------+-----+---------+-------+
| ROLL_NO | int         | NO   | PRI | NULL    |       |
| NAME    | varchar(20) | NO   |     | NULL    |       |
| AGE     | smallint    | NO   |     | NULL    |       |
| SUBJECT | varchar(20) | NO   | UNI | NULL    |       |
+---------+-------------+------+-----+---------+-------+
4 rows in set (0.00 sec)

mysql>
```

For examples and practice questions, please click [Examples](/Examples/CREATE_table_examples.md)


