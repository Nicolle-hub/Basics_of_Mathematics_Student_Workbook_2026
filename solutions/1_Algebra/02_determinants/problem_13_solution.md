Exercise 13 Solution

Start with matrix A:

(
  1  2  3
  2  5  7
  1  0  2
)

Step 1: Replace row 2 with row 2 - 2 * row 1, and row 3 with row 3 - row 1.

These are row replacements, so the determinant is unchanged. The matrix becomes:

(
  1  2  3
  0  1  1
  0 -2 -1
)

Step 2: Replace row 3 with row 3 + 2 * row 2.

This row replacement also leaves the determinant unchanged. The matrix becomes:

(
  1  2  3
  0  1  1
  0  0  1
)

The final matrix is upper triangular. Its determinant is the product of its diagonal entries:

determinant of A = 1 * 1 * 1 = 1

Answer: The determinant is 1. Every row operation preserved its value.