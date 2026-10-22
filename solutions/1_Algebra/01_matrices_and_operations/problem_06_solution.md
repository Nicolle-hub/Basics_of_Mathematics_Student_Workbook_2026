# Exercise 6: Transpose

### Given Matrices:
$$A = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix}_{2 \times 3}, \quad B = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}_{3 \times 2}$$

---

### 1. Compute $A^T$ and $B^T$

To find the transpose of a matrix, switch its rows and columns:

* **$A^T$** (size $3 \times 2$):
  $$
  A^T = \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}
  $$

* **$B^T$** (size $2 \times 3$):
  $$
  B^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix}
  $$

---

### 2. Compute $AB$

$$
\begin{aligned}
AB &= \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix} \\
&= \begin{pmatrix} (1)(1)+(2)(2)+(3)(-1) & (1)(0)+(2)(1)+(3)(3) \\ (4)(1)+(5)(2)+(6)(-1) & (4)(0)+(5)(1)+(6)(3) \end{pmatrix} \\
&= \begin{pmatrix} 1 + 4 - 3 & 0 + 2 + 9 \\ 4 + 10 - 6 & 0 + 5 + 18 \end{pmatrix} \\
&= \begin{pmatrix} 2 & 11 \\ 8 & 23 \end{pmatrix}
\end{aligned}
$$

---

### 3. Verify that $(AB)^T = B^T A^T$

* **Left Side: $(AB)^T$**
  Taking the transpose of $AB = \begin{pmatrix} 2 & 11 \\ 8 & 23 \end{pmatrix}$:
  $$
  (AB)^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}
  $$

* **Right Side: $B^T A^T$**
  $$
  \begin{aligned}
  B^T A^T &= \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix} \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix} \\
  &= \begin{pmatrix} (1)(1)+(2)(2)+(-1)(3) & (1)(4)+(2)(5)+(-1)(6) \\ (0)(1)+(1)(2)+(3)(3) & (0)(4)+(1)(5)+(3)(6) \end{pmatrix} \\
  &= \begin{pmatrix} 1 + 4 - 3 & 4 + 10 - 6 \\ 0 + 2 + 9 & 0 + 5 + 18 \end{pmatrix} \\
  &= \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}
  \end{aligned}
  $$

Since both sides yield $\begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}$, the property $(AB)^T = B^T A^T$ is **verified**.