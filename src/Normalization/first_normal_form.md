# First Normal Form 

* First normal form states that every cell should contain `atomic value`.
* Every column must have same domain.

### Example : Below table is not in first normal form

Roll No|Name|Course
-|-|-
101|Rohan|CN, OS
102|Priyanka| DBMS, CO


We can convert above table to 1NF by segregating the course values as below

Roll No|Name|Course
-|-|-
101|Rohan|CN
101|Rohan|OS
102|Priyanka| DBMS
102|Priyanka|CO

Every multivalued attribute should be given a separate table. Here `Course` is a multivalued attribute.