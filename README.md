# LLML

## Ruleset
* One process per line.
* All characters must be UTF-8.
* All processes must be connected.
* If at any given time there is fewer than two processes running, the model is incomplete.
* If at any given time there is more than two processes running, the model contains a logical error.

## Defined characters
```plain
; : begin process
* : instantiate
= : thread
` : include
$ : end process
@ : pointer
& : association
! : dependency
: : parameter
X : satisfied
O : unsatisfied
> : return
< : import
```

## Example:
```
         @QualifierValue
         `*;==========================$
`!@Property:qualifier[1..1]           &A_qualifier_qualifierValue
           `qualifier_attribute       X
`!@InputPin:value[1..1]               &A_value_qualifierValue
           `multiplicity_of_qualifier X
           `type_of_qualifier         X
;=====================================>qualifierValue
```