Exercise 2 Solution

Matrix A is:

(
  1  2  -1
  0  3   4
  2  1   5
)

Sarrus' rule: add the products on the downward diagonals and subtract the products on the upward diagonals.

Downward products:

1 * 3 * 5 = 15
2 * 4 * 2 = 16
(-1) * 0 * 1 = 0

Sum of downward products = 15 + 16 + 0 = 31

Upward products:

(-1) * 3 * 2 = -6
1 * 4 * 1 = 4
2 * 0 * 5 = 0

Sum of upward products = -6 + 4 + 0 = -2

Therefore:

determinant of A = 31 - (-2) = 33

Check by expanding along the first row:

determinant of A = 1 * (3 * 5 - 4 * 1)
                   - 2 * (0 * 5 - 4 * 2)
                   + (-1) * (0 * 1 - 3 * 2)
                 = 11 + 16 + 6
                 = 33

The check confirms that the determinant is 33.