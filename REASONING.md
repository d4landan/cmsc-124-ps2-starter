# Reasoning Before Execution

Write the rule behind each case before you commit your predictions. Replace
every placeholder line below with one to three sentences that name the rule
producing that case's value, type, length, and dimensions. One rule is enough.
After you run and find a miss, add a short correction entry under that case in a
later commit.

## P01
The coercion ladder runs logical, integer, double, character. Since 3.5 is a double, the logical and integer values are converted to double. The value is [1,2,3.5] with length three and no dimensions.

## P02
The coercion ladder makes character the final type when a character value is included. The integer and logical values become strings, so the value is ["1","2","TRUE"] with length three and no dimensions.

## P03
R recycles the shorter vector to match the longer one during addition. The value is [11L,22L,31L,42L] with integer type, length four, and no dimensions.

## P04
Positive indexing selects the third and first elements in that order. The original names are preserved, so the value is [third=9L,first=8L] with integer type, length two, and no dimensions.

## P05
Negative indexing removes the second element from the vector. The value is [4L,9L] with integer type, length two, and no dimensions.

## P06
The condition selects values that are missing or greater than 10. The missing integer is included because is.na() detects it, so the value is [NA,12L] with integer type, length two, and no dimensions.

## P07
A factor stores its category labels using integer codes internally. The value is [1L,2L,1L] with integer type, length three, and no dimensions.

## P08
A list can store elements with different types without coercing them into one common type. The value is [scores=[3L,5L],label="A"] with list type, length two, and no dimensions.

## P09
Replace this line with the rule that decides this case.

## P10
Replace this line with the rule that decides this case.

## P11
Replace this line with the rule that decides this case.

## P12
Replace this line with the rule that decides this case.

## P13
Replace this line with the rule that decides this case.

## P14
Replace this line with the rule that decides this case.

## P15
Replace this line with the rule that decides this case.

## P16
Replace this line with the rule that decides this case.
