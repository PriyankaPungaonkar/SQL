# DROP statement

The DROP TABLE statement allows a table to be removed from a database. This statement deletes the entire structure as well as the content of the table.

DROP TABLE MySQL Command Syntax

To remove a table in MySQL, use the DROP TABLE statement. The basic syntax of the command is as follows:

```
DROP [TEMPORARY] TABLE [IF EXISTS] table_name [, table_name] [RESTRICT | CASCADE];
```
Let’s break down the syntax:
* The DROP TABLE statement deletes a table and its rows permanently.
* The [TEMPORARY] option ensures you remove temporary tables only.
* The [IF EXISTS] option drops a table only if it exists.
* The [RESTRICT] option will be available in future iterations of MySQL. It ensures that a parent row is not deleted if a child row is referencing a value in said parent row.
* The [CASCADE] option ensures that when you delete a row, all rows in related tables that reference that row are deleted as well. This option will be available in future iterations of MySQL.

## Use the DROP Statement to Remove a Table

To permanently remove a table, enter the following statement within the MySQL shell:

```sql
DROP TABLE table1;
```
Replace table1 with the name of the table you want to delete. The output confirms that the table has been removed.

Example :
```sql
mysql> DROP TABLE cities;
Query OK, 0 rows affected (0.02 sec)
```

## Use DROP to Remove Only Existing Tables

MySQL generates an error if you try to drop a table that does not exist. This can be an issue when including the DROP statement in a predefined script.

```sql
mysql> DROP TABLE cities;
ERROR 1051 (42S02): Unknown table 'rohan.cities'
```

Error informing us that the table does not exist.

## To check MySQL if a table exists first:
```sql
DROP TABLE IF EXISTS table1;
```
The IF EXISTS option generates a warning if table1 does not exist.
```sql
mysql> DROP TABLE cities;
ERROR 1051 (42S02): Unknown table 'rohan.cities'
```
Warning if the table to be droped does not exist.

Using this option prevents a script from getting stuck on an error. Display the warning by entering:
```sql
mysql> show warnings;
+-------+------+------------------------------+
| Level | Code | Message                      |
+-------+------+------------------------------+
| Note  | 1051 | Unknown table 'rohan.cities' |
+-------+------+------------------------------+
1 row in set (0.00 sec)
```

## How to DROP Multiple Tables

To drop multiple tables with a single DROP statement:
```sql
DROP TABLE IF EXISTS table1, table2, table3;
```
The `IF EXISTS` option shows one warning as table1 does not exist.

## How to DROP a Temporary Table

Temporary tables are used to generate and store a data set shortly before using it.

For example, you might decide to store the results of a SELECT statement with multiple JOIN statements in a temporary table. Next, query the temporary table with ease.

To remove temporary tables without risking losing regular tables, use the TEMPORARY option:

```sql
DROP TEMPORARY TABLE IF EXISTS table4;
```