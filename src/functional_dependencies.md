# Functional Dependencies

Functional Dependency (FD) is a constraint that determines the `relation of one attribute to another attribute` in a Database Management System (DBMS). 

Functional Dependency helps to maintain the quality of data in the database. 

It plays a vital role to find the difference between good and bad database design.

A functional dependency is denoted by an arrow "→". The functional dependency of X on Y is represented by `A → B`.

![functional dependency](/images/functional_dependencies.png)



### For example :

Suppose there exist a function

`f : A -> B`

* If you have value of alpha(A) you can find value of Beta(B).
* We can only find/search value of Beta and not compute it.

Alpha|Beta|Validity|Alpha|Beta|Validity
-|-|-|-|-|-
a|1|Valid|a|1|Valid
b|2|Valid|`a`|2|Invalid
c|3|Valid|b|3|Valid
d|2|Valid|c|4|Valid

* In above example, when alpha is unique we can find the value of Beta. 
* If alpha values are duplicated, we cannot find the value of Beta as it is ambiguos.
* Beta column can have duplicates.


Definition :
```
Given : 
Suppose R be a Relational Table 

Conditions : 
A ⊆ R , B ⊆ R , A -> B

if t1[A] == t2[A] then
    t1[B] == t2[B]

```



## Types of Functional Dependencies

### 1. Trivial Functional Dependency in DBMS

The Trivial dependency is a set of attributes which are called a trivial `if the set of attributes are included in that attribute`.

So, A -> B is a trivial functional dependency if B is a subset of A. 

For example:
Emp_id|Emp_name
-|-
AS555| 	Harry
AS811 |	George
AS999 |	Kevin

Consider this table of with two columns `Emp_id` and `Emp_name`.

`{Emp_id, Emp_name} -> Emp_id` is a trivial functional dependency as `Emp_id` is a subset of `{Emp_id,Emp_name}`.


### 2. Non Trivial Functional Dependency in DBMS

Functional dependency which also known as a nontrivial dependency occurs when `A->B holds true where B is not a subset of A`. 

In a relationship, if attribute B is not a subset of attribute A, then it is considered as a non-trivial dependency.

Company| 	CEO| 	Age
-|-|-
Microsoft| 	Satya Nadella| 	51
Google |Sundar Pichai|	46
Apple 	|Tim Cook 	|57

Example:

`(Company} -> {CEO}` (if we know the Company, we knows the CEO name)

But CEO is not a subset of Company, and hence it's non-trivial functional dependency. 

### 3. Transitive Dependency in DBMS

A Transitive Dependency is a type of functional dependency which happens when t is indirectly formed by two functional dependencies.

Example:
Company |	CEO| 	Age
-|-|-
Microsoft |	Satya Nadella| 	51
Google 	|Sundar Pichai 	|46
Alibaba |	Jack Ma 	|54


`{Company} -> {CEO}` (if we know the compay, we know its CEO's name)

`{CEO } -> {Age}` If we know the CEO, we know the Age

Therefore according to the rule of rule of transitive dependency:

`{ Company} -> {Age}` should hold, that makes sense because if we know the company name, we can know his age.

Note: You need to remember that transitive dependency can only occur in a relation of three or more attributes. 

### 4. Multivalued Dependency in DBMS

Multivalued dependency occurs in the situation where there are multiple independent multivalued attributes in a single table. 

A multivalued dependency is a complete constraint between two sets of attributes in a relation. 

It requires that certain tuples be present in a relation.

Example:
Car_model |	Maf_year | 	Color
-|-|-
H001 	|2017 	|Metallic
H001 	|2017 	|Green
H005 	|2018 	|Metallic
H005 	|2018 	|Blue
H010 	|2015 	|Metallic
H033 	|2012 	|Gray

In this example, `maf_year` and `color` are independent of each other but dependent on `car_model`. 

In this example, these two columns are said to be multivalue dependent on car_model.

This dependence can be represented like this:

`car_model -> maf_year`

`car_model-> colour` 