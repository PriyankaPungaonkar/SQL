# Boyce Codd Normal Form (BCNF)

* A table is said to be in BCNF if it is already in 3NF and `no attribute is finding a prime attribute`.
* If alpha is not a super key and is finding another alpha, this should be removed.

Example :
```
Relation : R(ABC)

FD : 
    AB -> C
    C -> B

- (AB)+ = ABC
- (AC)+ = ABC
- AB and AC are candidate keys.
```

## How to achieve BCNF

Create a separate table where prime/non orime attribute is finding a prime attribute

2 tables to be created
1. R(ABC)
2. R(CB)