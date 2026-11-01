Exercise 14 Solution

The coefficient matrix is:

(
  1  2
  k  4
)

Its determinant is:

determinant of A = 1 * 4 - 2 * k = 4 - 2k

The system has exactly one solution for every right-hand side when the matrix is invertible, which requires a nonzero determinant:

4 - 2k != 0
k != 2

Therefore, the system has exactly one solution for every b when k is not 2.

When k = 2, the equations are:

x1 + 2 * x2 = b1
2 * x1 + 4 * x2 = b2

The left side of the second equation is twice the left side of the first.

Example with infinitely many solutions:

Choose b =
(
  1
  2
)

Both equations reduce to x1 + 2 * x2 = 1. Let x2 = s. Then x1 = 1 - 2 * s for any real s, so there are infinitely many solutions.

Example with no solution:

Choose b =
(
  1
  3
)

Doubling the first equation gives 2 * x1 + 4 * x2 = 2, which contradicts the second equation 2 * x1 + 4 * x2 = 3. Therefore, there is no solution.