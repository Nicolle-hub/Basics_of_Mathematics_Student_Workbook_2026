# Exercise 2: Addition and Scalar Multiplication

### Given Matrices:
$$A = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix}, \quad B = \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}$$

---

### 1. Compute $A + B$

$$
\begin{aligned}
A + B &= \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} + \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} \\
&= \begin{pmatrix} 1+4 & 2+(-2) \\ -1+0 & 3+5 \end{pmatrix} \\
&= \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}
\end{aligned}
$$

---

### 2. Compute $A - B$

$$
\begin{aligned}
A - B &= \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} - \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} \\
&= \begin{pmatrix} 1-4 & 2-(-2) \\ -1-0 & 3-5 \end{pmatrix} \\
&= \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}
\end{aligned}
$$

---

### 3. Compute $3A - 2B$

**Step 1: Scalar multiplication**
* $3A = 3 \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix}$
* $2B = 2 \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}$

**Step 2: Subtraction**
$$
\begin{aligned}
3A - 2B &= \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix} - \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix} \\
&= \begin{pmatrix} 3-8 & 6-(-4) \\ -3-0 & 9-10 \end{pmatrix} \\
&= \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}
\end{aligned}
$$

---

### Explanation: Why Matrix Addition Requires Same Dimensions

Matrix addition is performed **entry-by-entry** (element-wise). This means each element in position $(i, j)$ of the first matrix is added to the corresponding element in position $(i, j)$ of the second matrix.

If two matrices have different dimensions:
* There will not be a 1-to-1 matching entry for every element.
* For example, adding a $2 \times 2$ matrix to a $2 \times 3$ matrix leaves the 3rd column of the second matrix with no matching elements to pair with in the first matrix. 

Therefore, matrix addition is **undefined** unless both matrices have the exact same number of rows and columns.