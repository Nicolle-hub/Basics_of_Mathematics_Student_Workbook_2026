# Exercise 1 Solution

For a 2x2 matrix

$$
\begin{pmatrix} a & b \\ c & d \end{pmatrix},
$$

the determinant is

$$
\det = ad - bc.
$$

## 1) Compute $\det\begin{pmatrix}3&-2\\5&4\end{pmatrix}$

$$
\det\begin{pmatrix}3&-2\\5&4\end{pmatrix}
= 3\cdot 4 - (-2)\cdot 5
= 12 + 10
= 22.
$$

So this matrix is invertible because its determinant is nonzero.

## 2) Compute $\det\begin{pmatrix}1&7\\2&14\end{pmatrix}$

$$
\det\begin{pmatrix}1&7\\2&14\end{pmatrix}
= 1\cdot 14 - 7\cdot 2
= 14 - 14
= 0.
$$

So this matrix is not invertible because its determinant is zero.

## Conclusion

- $\det\begin{pmatrix}3&-2\\5&4\end{pmatrix} = 22 \neq 0$, so the matrix is invertible.
- $\det\begin{pmatrix}1&7\\2&14\end{pmatrix} = 0$, so the matrix is not invertible.

A square matrix is invertible exactly when its determinant is nonzero.
