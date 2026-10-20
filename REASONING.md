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

Id and passed are the names of the two columns, and the data frame has length of 2 as there are 2 columns, then given we have 2 rows, dim is 2x2. The number of rows is from the number of given in the 2 columns, both columns have 2 elements which accounts for the number of rows. As for the type, since data frame is a list of columns, P09 has list as its type, and the value would be data.frame[2x2]{id=[1,2],passed=[TRUE,FALSE]}. 

## P10

R stores matrix by columns, and given that P10 is a matrix with 2 rows, from nrow=2L, and the values given are from 1 to 6, the matrix would first fill up the first column using 1 and 2, then fill the second column with values 3 and 4, and 5 and 6 will fill the last column. From the given number of rows and the values given, column would be 3, hence dim is 2x3. In the addition, 10 and 20 are recycled, and are then added to the values, it happens because 2 is less than 6 thus R repeats on adding the 2 values until the 6 values are added with it. The value is matrix[2x3](11,22,13,24,15,26). The length counts the number of values in the matrix which is 6, while the type of the values is integer as the values 1:6, 10L, and 20L are integers.  

## P11

NA is a missing value and it affects the rest of the values in P11. Moreover mean() function will be able to calculate for the mean when there is no NA or when na.rm is declared as TRUE, which removes NA before the mean is calculated. In this case, NA affects the values 8, and 10 thus it would give the value of [NA]. The type would remain as double from the initial values beside NA. Counting the value, the length is 1 while the dim is none, as there is no dimension. 

## P12

Despite having NA, it is different compared to P11, the na.rm was declared as TRUE, thus mean() returns the value [9] which is the mean of 8 and 10, entirely ignoring NA. The value only has 9, which gives us the length of 1 and a dim of none given there is no dimension in the value. As for the type, it is double after the evaluation of mean(). 

## P13

The x has values 1,2, and 3 then the value of x[2] would be changed to 2.5, so from 2 it becomes 2.5. The change from 2 to 2.5 widens the atomic vector in order to fit 2.5, changing the type from integer to double. Hence, the value would be [1,2.5,3] from x, length is 3, and dim is none. 

## P14 
For the initial 7,NA_real_, 12, and 4, it goes through score transformation. With the first adjusted, it replaces the missing score with 0, while the remaining scores are multiplied by 2  which results to 14,0,24, and 8. After that, the scores which are greater than 15 will be assigned 15 as its new score, the score affected by the second adjustment is 24, which becomes 15. In the final value, [14,0,15,8], double is the type while the length is 4, as there are 4 values, and dim is none, as it has no dimension. 

## P15 

Array, similar to matrices, stores its values in a storage order, which would it fills up the column from top to bottom. In addition, array are atomic vectors with a dim attribute, thus it fills the first dimension first. The array is carrying a dim attribute of [2x2x2]. Given that there is 8 values from 1 to 8, the length would be 8, and the type is the type of the values, integer. For the dim, it uses the given dim of 2x2x2, while the value would be array[2x2x2](1,2,3,4,5,6,7,8). 

## P16 
The following 4L,7L,9L, are integers which has an index of 1-3, however [0L] selects no elements, its length is 0 as there is no selected element, dim is none, and the same atomic type remains. Thus the value is [].