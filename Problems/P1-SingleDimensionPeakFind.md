### 1-Dimensional Peak Finding
|a  |b  |c  |d  |e  |f  |g  |h  |i  | 
|---|---|---|---|---|---|---|---|---|

a-i are numbers.

Position d is a peak iff b >= a and b >=c
Position q is a peek iff i >= h

**Problem: Find a peak if it exists**

Bonus: Argue that any array will have a peak.

### Linear Approach

1.   Start from left
2.   1,2...n/2...n-1,n

Complexity: Look at n/2 elements
Worst case complexity = Theta(n)

### Divide and Conquer

1.   if a\[n/2] < a\[n/2-1] then only look at left half then only look
at left half 1...n/2-1 to look for a peak.
2.   if a\[n/2] > a\[n/2-1] then only look for peak on the right.
3.   else n/2 position is a peek

Formal argument:


Complexity:
 
*  T(n) = Work algorithm does on an input of size n

T(n) = T(n/2)+ &theta;(1)  

T(1) = &theta;(1)  
T(n) = &theta;(log<sub>2</sub> n)