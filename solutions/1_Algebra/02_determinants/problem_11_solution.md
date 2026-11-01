Exercise 11 Solution

Start with matrix A:

(
  1  2  3
  1  3  4
  1  4  6
)

Adding a multiple of one row to another does not change the determinant.

Step 1: Replace row 2 with row 2 - row 1, and row 3 with row 3 - row 1.

The matrix becomes:

(
  1  2  3
  0  1  1
  0  2  3
)

Step 2: Replace row 3 with row 3 - 2 * row 2.

The matrix becomes:

(
  1  2  3
  0  1  1
  0  0  1
)

Both row operations preserve the determinant. The final matrix is upper triangular, so:

determinant of A = 1 * 1 * 1 = 1

Answer: The determinant is 1.