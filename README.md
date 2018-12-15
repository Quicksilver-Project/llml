
1 process per line (ladder logic)
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

Example:
         @QualifierValue
         `*;==========================$
`!@Property:qualifier[1..1]           &A_qualifier_qualifierValue
           `qualifier_attribute       X
`!@InputPin:value[1..1]               &A_value_qualifierValue
           `multiplicity_of_qualifier X
           `type_of_qualifier         X
;=====================================>qualifierValue
