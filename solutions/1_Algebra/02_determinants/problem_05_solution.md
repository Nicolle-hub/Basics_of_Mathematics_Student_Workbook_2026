Exercise 5 Solution

Start with matrix A:

(
   1  2  3
   2  1  0
  -1  4  2
)

Adding a multiple of one row to another does not change the determinant.

Step 1: Replace row 2 with row 2 - 2 * row 1, and replace row 3 with row 3 + row 1.

The determinant is unchanged. The matrix becomes:

(
  1   2   3
  0  -3  -6
  0   6   5
)

Step 2: Replace row 3 with row 3 + 2 * row 2.

The determinant is unchanged. The matrix becomes:

(
  1   2   3
  0  -3  -6
  0   0  -7
)

This matrix is upper triangular, so:

determinant of A = 1 * (-3) * (-7) = 21

Answer: determinant of A is 21. Both row operations preserved the determinant.