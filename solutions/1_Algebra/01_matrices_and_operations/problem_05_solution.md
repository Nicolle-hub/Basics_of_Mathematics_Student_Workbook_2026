# Exercise 5: Matrix Times Vector

### Given:
$$A = \begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix}, \quad x = \begin{pmatrix} 4 \\ 2 \end{pmatrix}$$

---

### 1. Compute $Ax$

$$
\begin{aligned}
Ax &= \begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix} \begin{pmatrix} 4 \\ 2 \end{pmatrix} \\
&= \begin{pmatrix} (2)(4) + (-1)(2) \\ (1)(4) + (3)(2) \end{pmatrix} \\
&= \begin{pmatrix} 8 - 2 \\ 4 + 6 \end{pmatrix} \\
&= \begin{pmatrix} 6 \\ 10 \end{pmatrix}
\end{aligned}
$$

---

### 2. Express $Ax$ as a Linear Combination of the Columns of $A$

The columns of $A$ are:
$$
\boldsymbol{a}_1 = \begin{pmatrix} 2 \\ 1 \end{pmatrix}, \quad \boldsymbol{a}_2 = \begin{pmatrix} -1 \\ 3 \end{pmatrix}
$$

Using the coefficients from the vector $x = \begin{pmatrix} 4 \\ 2 \end{pmatrix}$ (where $4$ is the first coefficient and $2$ is the second coefficient), $Ax$ can be written as a linear combination of the columns:

$$
Ax = 4 \begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2 \begin{pmatrix} -1 \\ 3 \end{pmatrix}
$$

**Verification:**
$$
\begin{aligned}
4 \begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2 \begin{pmatrix} -1 \\ 3 \end{pmatrix} &= \begin{pmatrix} 8 \\ 4 \end{pmatrix} + \begin{pmatrix} -2 \\ 6 \end{pmatrix} \\
&= \begin{pmatrix} 8 - 2 \\ 4 + 6 \end{pmatrix} \\
&= \begin{pmatrix} 6 \\ 10 \end{pmatrix}
\end{aligned}
$$