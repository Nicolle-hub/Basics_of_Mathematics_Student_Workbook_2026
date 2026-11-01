Exercise 12 Solution

Start with matrix A(t):

(
  1  2  3
  2  4  t
  0  1  1
)

First replace row 2 with row 2 - 2 * row 1. This row replacement does not change the determinant.

The new matrix is:

(
  1  2  3
  0  0  t - 6
  0  1  1
)

Expand along the first column. The remaining 2 by 2 determinant is:

0 * 1 - (t - 6) * 1 = 6 - t

Thus, the determinant of A(t) is 6 - t. The matrix is not invertible when:

6 - t = 0
t = 6

When t = 6, the second row of the original matrix is:

(2  4  6)

This is twice the first row, (1  2  3), so the rows are dependent.

Conclusion

The matrix is not invertible when t = 6.