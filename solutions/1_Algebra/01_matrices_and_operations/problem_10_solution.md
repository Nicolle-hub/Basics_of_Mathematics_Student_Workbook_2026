# Exercise 10: Columns of a Matrix Product

### Given:
$$A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix}, \quad B = \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \end{pmatrix}$$

Let the columns of $B$ be denoted as $\boldsymbol{b}_1$ and $\boldsymbol{b}_2$, where:
$$\boldsymbol{b}_1 = \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix}, \quad \boldsymbol{b}_2 = \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix}$$

---

### 1. Compute $Ab_1$ and $Ab_2$

* **Compute $Ab_1$:**
  $$
  Ab_1 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix} = \begin{pmatrix} (1)(1) + (2)(-1) + (0)(3) \\ (0)(1) + (1)(-1) + (1)(3) \end{pmatrix} = \begin{pmatrix} 1 - 2 + 0 \\ 0 - 1 + 3 \end{pmatrix} = \begin{pmatrix} -1 \\ 2 \end{pmatrix}
  $$

* **Compute $Ab_2$:**
  $$
  Ab_2 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix} = \begin{pmatrix} (1)(2) + (2)(0) + (0)(1) \\ (0)(2) + (1)(0) + (1)(1) \end{pmatrix} = \begin{pmatrix} 2 + 0 + 0 \\ 0 + 0 + 1 \end{pmatrix} = \begin{pmatrix} 2 \\ 1 \end{pmatrix}
  $$

---

### 2. Compute the Matrix $AB$

$$
\begin{aligned}
AB &= \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \end{pmatrix} \\
&= \begin{pmatrix} (1)(1)+(2)(-1)+(0)(3) & (1)(2)+(2)(0)+(0)(1) \\ (0)(1)+(1)(-1)+(1)(3) & (0)(2)+(1)(0)+(1)(1) \end{pmatrix} \\
&= \begin{pmatrix} 1 - 2 + 0 & 2 + 0 + 0 \\ 0 - 1 + 3 & 0 + 0 + 1 \end{pmatrix} \\
&= \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix}
\end{aligned}
$$

---

### 3. Comparison and Explanation

* **Comparison:** Looking at the columns of the resulting matrix $AB$:
  * First column: $\begin{pmatrix} -1 \\ 2 \end{pmatrix}$ (matches $Ab_1$)
  * Second column: $\begin{pmatrix} 2 \\ 1 \end{pmatrix}$ (matches $Ab_2$)
* **Explanation:** By definition of matrix multiplication, multiplying a matrix $A$ by another matrix $B$ is equivalent to multiplying $A$ by each individual column of $B$ successively:
  $$AB = \begin{pmatrix} A\boldsymbol{b}_1 & A\boldsymbol{b}_2 \end{pmatrix}$$
  Therefore, the columns of the product matrix $AB$ are explicitly formed by the vectors $A\boldsymbol{b}_1$ and $A\boldsymbol{b}_2$.