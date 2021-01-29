### Example 1 :
```
Relation : R(ABC)
FD :
    A -> B
    B -> C

Closures :

    (A)+ = ABC   
    (B)+ = BC
    (C)+ = c
```

### Example 2 :
```
Relation : R(ABCDEFG)
FD :
    A -> B
    BC -> DE
    AEG -> G
    
Closures of AC :

    (AC)+  = ABCDE

```
### Example 3 :
```
Relation : R(ABCDE)
FD :
    A -> BC
    CD -> E
    B -> D
    E -> A
    
Closures of B :

    (B)+  = BD

```
### Example 4 :
```
Relation : R(ABCDEF)
FD :
    AB -> C
    BC -> AD
    D -> E
    CF -> B
    
Closures of AB :

    (AB)+  = ABCDE

```
### Example 5 :
```
Relation : R(ABCDEFGH)
FD :
    A -> BC
    CD -> E
    E -> C
    D -> AEH
    ABH -> BD
    DH -> BC

Does BCD -> H holds True?

Closure of BCD :

    (BCD)+  = ABCDEH

Answer : yes it is true.     

```




