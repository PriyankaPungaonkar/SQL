# Types of keys in SQL

A key is a `single or combination of multiple fields` in a table. 

It is used to fetch or retrieve records/data-rows from data table according to the condition/requirement. 

Keys are also used to create a relationship among different database tables or views.

### Example : 
![SQL Keys](/images/sqlkeys.png)


We have following types of keys in SQL which are used to fetch records from tables and to make relationship among tables or views.

## 1. Super Key

Super key is a set of one or more than one keys that can be used to `identify a record uniquely in a table`. **Example:** Primary key, Unique key, Alternate key are a subset of Super Keys.


## 2. Candidate Key

A Candidate Key is a `set of one or more fields/columns that can identify a record uniquely` in a table. There can be multiple Candidate Keys in one table. Each Candidate Key can work as Primary Key.

**Example:** In the above diagram ID, RollNo and EnrollNo are Candidate Keys since all these three fields can be work as Primary Key.


## 3. Primary Key

Primary key is a set of one or more fields/columns of a table that uniquely identify a record in a database table. It can not accept null, duplicate values. Only one Candidate Key can be Primary Key.


## 4. Alternate key

An Alternate key is a key that can be work as a primary key. Basically, `it is a candidate key that currently is not a primary key.`

**Example:** In the above diagram RollNo and EnrollNo become Alternate Keys when we define `ID` as Primary Key.

## 5. Composite/Compound Key

Composite Key is a combination of more than one fields/columns of a table. It can be a Candidate key, Primary key.


## 6. Unique Key

A unique key is a set of one or more fields/columns of a table that uniquely identify a record in a database table. It is like Primary key but it can accept only one null value and it can not have duplicate values. 

## 7. Foreign Key

Foreign Key is a field in a database table that is `Primary key in another table`. It can accept multiple null, duplicate values.

**Example:** We can have a DeptID column in the Employee table which is pointing to a DeptID column in a department table where it a primary key.

[Home](/README.md) | [Prev](/src/Chapter_1/keys_in_sql.md)) | Next](/src/Normalization/functional_dependencies.md)
