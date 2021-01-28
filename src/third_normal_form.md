# Third Normal Form

* A table can be said to be in 3NF if it is already in 2nf and there is no `Transitive dependency`.
* `A -> B`  and `B-> C` then `A -> C` is a transitive dependency.
* Non prime atribute find another non prime attribute is transitive dependency.


Example :
```
Relation : R(ABCD)

FD :
    AB -> C
    C -> D

(AB)+ = ABCD
- AB is the candidate key.
- AB is prime attribute
- CD is non prime attribute

```

## How to achieve 3NF

Create separate table where non prime attribute is finding another non prime attribute.

2 tables to be created
1. R(ABC)
2. R(CD) 