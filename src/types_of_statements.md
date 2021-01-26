# Types of statements in SQL

Basically there are three types of statements in SQL

1. Data definition language (DDL)
2. Data Manipulation Language (DML)
3. Transaction Control Language (TCL)


## 1. Data definition Language 
Data definition language (DDL) statements let you to perform these tasks:

* Create, alter, and drop schema objects
* Grant and revoke privileges and roles
* Analyze information on a table, index, or cluster
* Establish auditing options
* Add comments to the data dictionary

The `CREATE`, `ALTER`, and `DROP` commands require exclusive access to the specified object. For example, an `ALTER TABLE` statement fails if another user has an open transaction on the specified table.

The `GRANT`, `REVOKE`, `ANALYZE`, `AUDIT`, and `COMMENT` commands do not require exclusive access to the specified object. For example, you can analyze a table while other users are updating the table.

Oracle Database implicitly commits the current transaction before and after every DDL statement.

A DDL statement is either blocking or nonblocking, and both types of DDL statements require exclusive locks on internal structures.

### The DDL statements are:

* ALTER 
* ANALYZE
* ASSOCIATE STATISTICS
* AUDIT
* COMMENT
* CREATE
* DISASSOCIATE STATISTICS
* DROP
* FLASHBACK
* GRANT
* NOAUDIT
* PURGE
* RENAME
* REVOKE
* TRUNCATE

## 2. Data Manipulation Language 
Data manipulation language (DML) statements access and manipulate data in existing schema objects. These statements do not implicitly commit the current transaction. The data manipulation language statements are:

* CALL
* DELETE
* EXPLAIN PLAN
* INSERT
* LOCK TABLE
* MERGE
* SELECT
* UPDATE

The `SELECT` statement is a limited form of DML statement in that it can only access data in the database. It cannot manipulate data stored in the database, although it can manipulate the accessed data before returning the results of the query.

## 3. Transaction Control Language

Transaction control statements manage changes made by DML statements. 

The transaction control statements are:

* COMMIT
* ROLLBACK
* SAVEPOINT
* SET TRANSACTION
* SET CONSTRAINT

We will see these in details.
