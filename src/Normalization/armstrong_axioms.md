
# Closure set of attributes

Attribute closure of an attribute set 'A' can be defined as a set of attributes which can be functionally determined from it. Denoted by `(F)+` (plus sign is superscript)

For example :
```
Relation : 
    R(ABCDEF)
FD      :
    A -> B
    C -> DE        
    AC ->F
    D -> AF
    E ->CF

Closures of all FD :

    (A)+    = AB
    (C)+    = CDEAF
    (AC)+   = ABCDEF
    (D)+    = ABDF
    (E)+    = ABCDEF

```

# Armstrong Axioms 

Axiom is a statement that is taken to be true, and serve as a premise or starting point for further arguments.

Armstrong axims holds on every RDBMS and can be used to generate closure set.

## Rules

### Primary Rules 
Rule|Definition
-|-
Reflexivity| if `y ⊆ x` then `x -> y`
Augmentation | if `x -> y` then `xz -> yz`
Transitivity | if `x -> y` and `y -> z` then `x -> z`

### Secondary Rules 
Rule|Definition
-|-
Union| if `x -> y` && `x -> z` then `x -> yz`
Decomposition | if `x -> yz` then `x -> y` && `x -> z`
Pseudo Transitivity | if `x -> y` && `wy -> z` then `xw -> z`
Composition | if `x -> y` && `z -> w` then `xz -> yw`

