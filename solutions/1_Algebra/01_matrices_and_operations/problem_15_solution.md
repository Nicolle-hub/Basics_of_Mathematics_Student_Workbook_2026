# Exercise 15: Associativity of Multiplication and Different Calculation Paths

### Given:

$$A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix}_{2 \times 3}, \quad B = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}_{3 \times 2}, \quad C = \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix}_{2 \times 2}$$

---

### Step 1: Compute $(AB)C$

**1. First, compute $AB$:**

$$
\begin{aligned}
AB &= \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix} \\
&= \begin{pmatrix} (1)(1)+(2)(2)+(0)(-1) & (1)(0)+(2)(1)+(0)(3) \\ (0)(1)+(1)(2)+(1)(-1) & (0)(0)+(1)(1)+(1)(3) \end{pmatrix} \\
&= \begin{pmatrix} 1 + 4 + 0 & 0 + 2 + 0 \\ 0 + 2 - 1 & 0 + 1 + 3 \end{pmatrix} \\
&= \begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix}_{2 \times 2}
\end{aligned}
$$

**2. Next, compute $(AB)C$:**

$$
\begin{aligned}
(AB)C &= \begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix} \\
&= \begin{pmatrix} (5)(2)+(2)(0) & (5)(1)+(2)(-1) \\ (1)(2)+(4)(0) & (1)(1)+(4)(-1) \end{pmatrix} \\
&= \begin{pmatrix} 10 + 0 & 5 - 2 \\ 2 + 0 & 1 - 4 \end{pmatrix} \\
&= \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}_{2 \times 2}
\end{aligned}
$$

---

### Step 2: Compute $A(BC)$

**1. First, compute $BC$:**

$$
\begin{aligned}
BC &= \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix} \\
&= \begin{pmatrix} (1)(2)+(0)(0) & (1)(1)+(0)(-1) \\ (2)(2)+(1)(0) & (2)(1)+(1)(-1) \\ (-1)(2)+(3)(0) & (-1)(1)+(3)(-1) \end{pmatrix} \\
&= \begin{pmatrix} 2 + 0 & 1 + 0 \\ 4 + 0 & 2 - 1 \\ -2 + 0 & -1 - 3 \end{pmatrix} \\
&= \begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix}_{3 \times 2}
\end{aligned}
$$

**2. Next, compute $A(BC)$:**

$$
\begin{aligned}
A(BC) &= \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix} \\
&= \begin{pmatrix} (1)(2)+(2)(4)+(0)(-2) & (1)(1)+(2)(1)+(0)(-4) \\ (0)(2)+(1)(4)+(1)(-2) & (0)(1)+(1)(1)+(1)(-4) \end{pmatrix} \\
&= \begin{pmatrix} 2 + 8 + 0 & 1 + 2 + 0 \\ 0 + 4 - 2 & 0 + 1 - 4 \end{pmatrix} \\
&= \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}_{2 \times 2}
\end{aligned}
$$

---

### Step 3: Comparison and Explanation

* **Comparison of Results:** 
  Both computation paths yield the exact same final matrix:
  
  $$(AB)C = A(BC) = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}$$

* **Comparison of Arithmetic Operations:**
  * **Path 1: $(AB)C$**
    * $AB$ (multiplying $2 \times 3$ by $3 \times 2$): requires $2 \times 2 \times 3 = 12$ scalar multiplications.
    * $(AB)C$ (multiplying $2 \times 2$ by $2 \times 2$): requires $2 \times 2 \times 2 = 8$ scalar multiplications.
    * **Total:** $12 + 8 = 20$ scalar multiplications.
  * **Path 2: $A(BC)$**
    * $BC$ (multiplying $3 \times 2$ by $2 \times 2$): requires $3 \times 2 \times 2 = 12$ scalar multiplications.
    * $A(BC)$ (multiplying $2 \times 3$ by $3 \times 2$): requires $2 \times 2 \times 3 = 12$ scalar multiplications.
    * **Total:** $12 + 12 = 24$ scalar multiplications.

* **Meaning of Associativity:**
  Associativity states that when multiplying three (or more) matrices, the grouping of the operations does not change the ultimate outcome. However, as demonstrated by the operation counts above, **the choice of grouping can change the computational effort required** to arrive at the result.