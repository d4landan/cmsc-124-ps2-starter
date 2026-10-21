# Vector and Scalar Evaluation

Replace this paragraph after your checks pass. Trace one input, including the
missing value, through `clean_scores_vector()` and `clean_scores_scalar()`.
Compare the two evaluation models, identify where recycling would change the
answer, and explain which implementation you would keep in an R program.

The sample input passed to both functions, clean_scores_vector(), and clean_scores_scalar(), is c(7,NA_real_,12,4). In the first adjustment in clean_scores_vector(), the NA values are converted to 0, while the rest are multiplied by 2. In the second adjustment, all the values greater than 20 would be converted to the max value 20, whereas the other values remain the same. Passing the same input through clean_scores_scalar() gives the same result of [1] 14 0 20 8. The [1] is an R's index marker to indicate the position of the first value in that line, although the naming would become different if the name is already given inside the input such as c(a=7, b=5). The names remain the same, while a is paired with 14, and b is paired with 10. 

As for recycling, the clean_scores_scalar() manage repetition with a for loop, thus no recycling occurs. While clean_scores_vector() relies on recycling the 2 in scores*2. As every score is multiplied by 2, the same could be said with 0 and 20. For the current input, recycling does not change answers however once the recycled value is no longer a one vector, then R would repeat by position and it might change answers. 
