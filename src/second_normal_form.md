# Second Normal Form

* Second normal form states that the table should not have `partial dependencies`.
* A table is said to be in 2NF if it is already in 1NF and there is no partial dependency.

Example :
```
Relation : R(ABCD)

FD :
    AB -> D
    B -> C
   
    
    - (AB)+  = ABCD
    - AB is a candidate key.
    - AB are prime attribute as they belong to a candidate key.
    - CD are non prime attribute.
 
    
    Here in second FD, C is not completely dependent on candidate key but dependent on B which is a part of candidate key.
```

When a `non prime attribute is dependent on a part of candidate key` and not entire cadidate key, this type of dependency should be removed in order to achieve 2NF.

## How to achieve 2NF

Create a separate table where non prime attribute is dependent on part of candidate key.

2 tables to be created

1. R(ABD)
2. R(BC)