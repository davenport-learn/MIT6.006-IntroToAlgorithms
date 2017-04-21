# 2D Peak Finding


Array of `n` rows with `m` columns. 

Given on this row point b - a - d with c above a and e beneath a.
a is a 2D-peek iff a-b, a>=d, a>=c, a>=e

### Greedy Ascent Algorithm

Pick initial direction. 
If is greater follow, if not switch direction, and continue.
If none greater you are at Peak.

**Complexity**

&theta;(nm)  
&theta;(n<sup>2</sup>) if n =m 

### Incorrect - Divide and Conquer

Jam Binary Search into 2-D Version

*   Pick middle column j = m/2.
*   Find a 1D peek at (i, j). 
*   Use (i,j) as a start to find a 1D-peak on row i

### Divide and Conquer #2

*   Pick middle column j = m/2
*   Find global max on column j at (i,j)
*   Compare(i, j-1), (i, j), (i, j +1)
*   Pick left cols if (i, j-1) > (i,j) and Repeat for Right
*   If (i, j) >= (i, j-1), (i, j+1) = (i,j) is a 2D Peak. 

Solves with half the number of columns.
Essentially a Binary Search in 2 Dimensions.
When you have a single column, find the global max <- done.

Complexity:

T(n,m) = T(n, m/2) + &theta;(n)  
T(n,1) = &theta;(n)  
T(n,m) = &theta;(n log<sub>2</sub> m)
