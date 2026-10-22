# Exercise 4: Matrix Multiplication and Noncommutativity

### Given Matrices:
$$A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}, \quad B = \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}$$

---

### 1. Compute $AB$

$$
\begin{aligned}
AB &= \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix} \\
&= \begin{pmatrix} (1)(2) + (2)(3) & (1)(0) + (2)(1) \\ (0)(2) + (1)(3) & (0)(0) + (1)(1) \end{pmatrix} \\
&= \begin{pmatrix} 2 + 6 & 0 + 2 \\ 0 + 3 & 0 + 1 \end{pmatrix} \\
&= \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}
\end{aligned}
$$

---

### 2. Compute $BA$

$$
\begin{aligned}
BA &= \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix} \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} \\
&= \begin{pmatrix} (2)(1) + (0)(0) & (2)(2) + (0)(1) \\ (3)(1) + (1)(0) & (3)(2) + (1)(1) \end{pmatrix} \\
&= \begin{pmatrix} 2 + 0 & 4 + 0 \\ 3 + 0 & 6 + 1 \end{pmatrix} \\
&= \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}
\end{aligned}
$$

---

### 3. Is $AB = BA$?

No, $AB \neq BA$ because:
$$
\begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix} \neq \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}
$$

---

### 4. Explanation: What Noncommutativity Means

In regular arithmetic with real numbers, multiplication is **commutative**, meaning the order does not matter ($a \cdot b = b \cdot a$, e.g., $3 \cdot 5 = 5 \cdot 3 = 15$).

**Noncommutativity of matrix multiplication** means that, in general, changing the order of matrices in a product changes the result:
$$AB \neq BA$$

Because matrix multiplication involves taking the **dot product of rows from the first matrix and columns from the second matrix**, swapping the order changes which rows interact with which columns. Consequently, the position and value of every entry in the resulting matrix change.