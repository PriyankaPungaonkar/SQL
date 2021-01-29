# Irreducible set of Functional Dependency

Whenever a user updates the database, the system must check whether any of the functional dependencies are getting violated in this process. 

If there is a violation of dependencies in the new database state, the system must roll back. 

Working with a huge set of functional dependencies can cause unnecessary added computational time. This is where the canonical cover comes into play.

A canonical cover of a set of functional dependencies F is a simplified set of functional dependencies that has the same closure as the original set F. 

Example :
```
Relation : R(WXYZ)

FD :
    X -> W
    WZ - > XY
    Y -> WXZ

Step 1 : Apply decomposition rule on FD

    so our new FD becomes :
        X -> W
        WZ -> X
        WZ -> Y
        Y -> W
        Y -> X
        Y -> Z
    
Step 2 : find closure of new FD multiple times for each FD. when finding the closure second time, ignore all the previous FD of same Alpha value.

    X -> W : (X)+  =  XW
    X -> W : (X)+  = X      Therefore X -> W is essential.  


    WZ -> X : (WZ)+ = WZXY
    WZ -> Y : (WZ)+ = WZYX         Therefore WZ -> X is redundant and unnecessary.
    WZ -> Y : (WZ)+ = WZ        tTherefore WZ -> Y is essential.                        

    Y -> W : (Y)+ = WXYZ
    Y -> X : (Y)+ = XZWY         Therefore Y -> W is redundant and unnecessary.
    Y -> Z : (y)+ = YZ           Therefore Y -> Z is essential.


Final FD :

    X -> W
    WZ -> Y
    y -> X
    Y -> Z

```