# Practice problems on functional dependency

## Question 1 : Which of the following functional dependency is not valid.

Table :
A|B|C|D|E
-|-|-|-|-
a|2|3|4|5
2|a|3|4|5
a|2|3|6|5
a|2|3|6|6

Options : 

1. A -> B
2. DE -> C
3. C -> DE
4. BC -> A

### Answer :
1. `A -> B`  is valid
2. `DE -> C` is valid
3. `C -> DE` is not valid
4. `BC -> A` is valid


## Question 2 : Which of the following functional dependency is valid.

Table :
x|y|z
-|-|-
1|4|2
1|5|3
1|6|3
3|2|2

Options : 

1. xy -> x && z -> y
2. yz -> X && y -> z
3. yz -> x && x -> z
4. xz -> y && y -> z

### Answer :
1. `xy -> x && z -> y` is not valid
2. `yz -> X && y -> z` is valid
3. `yz -> x && x -> z` is not valid
4. `xz -> y && y -> z` is not valid

## Question 3 : Which of the following functional dependency is valid.

Table :
a|b|c
-|-|-
1|2|4
3|5|4
3|7|2
1|4|2

Options : 

1. a -> b && bc -> a
2. c -> b && ca -> b
3. b -> c && ab -> c
4. a -> c && bc -> a

Answer :
1. `a -> b && bc -> a` is not valid
2. `c -> b && ca -> b` is not valid
3. `b -> c && ab -> c` is valid
4. `a -> c && bc -> a` is not valid