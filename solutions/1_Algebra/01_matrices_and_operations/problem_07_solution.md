# Exercise 7: Identity Matrix, Zero Matrix, and Powers

### Given Matrix:
$$A = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$$

Let $I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$ (the $2 \times 2$ identity matrix) and $0 = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}$ (the $2 \times 2$ zero matrix).

---

### 1. Compute $AI$ and $IA$

* **$AI$:**
  $$
  AI = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (2)(1)+(1)(0) & (2)(0)+(1)(1) \\ (0)(1)+(2)(0) & (0)(0)+(2)(1) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = A
  $$

* **$IA$:**
  $$
  IA = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} (1)(2)+(0)(0) & (1)(1)+(0)(2) \\ (0)(2)+(1)(0) & (0)(1)+(1)(2) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = A
  $$

---

### 2. Compute $A + 0$

$$
A + 0 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} + \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix} = \begin{pmatrix} 2+0 & 1+0 \\ 0+0 & 2+0 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = A
$$

---

### 3. Compute $A^2$ and $A^3$

* **$A^2 = A \cdot A$:**
  $$
  A^2 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} (2)(2)+(1)(0) & (2)(1)+(1)(2) \\ (0)(2)+(2)(0) & (0)(1)+(2)(2) \end{pmatrix} = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}
  $$

* **$A^3 = A^2 \cdot A$:**
  $$
  A^3 = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} (4)(2)+(4)(0) & (4)(1)+(4)(2) \\ (0)(2)+(4)(0) & (0)(1)+(4)(2) \end{pmatrix} = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}
  $$

---

### 4. Roles of $I$ and $0$, and Pattern in Successive Powers of $A$

* **Role of $I$ (Identity Matrix):** Acts as the **multiplicative identity** (analogous to the number $1$ in scalar arithmetic). Multiplying any compatible matrix by $I$ leaves the matrix unchanged ($AI = IA = A$).
* **Role of $0$ (Zero Matrix):** Acts as the **additive identity** (analogous to the number $0$ in scalar arithmetic). Adding the zero matrix to any matrix leaves the matrix unchanged ($A + 0 = A$).
* **Pattern in Successive Powers of $A$:**
  Observing $A$, $A^2$, and $A^3$:
  * $A^1 = \begin{pmatrix} 2^1 & 1 \cdot 2^0 \\ 0 & 2^1 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$
  * $A^2 = \begin{pmatrix} 2^2 & 2 \cdot 2^1 \\ 0 & 2^2 \end{pmatrix} = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}$
  * $A^3 = \begin{pmatrix} 2^3 & 3 \cdot 2^2 \\ 0 & 2^3 \end{pmatrix} = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}$
  
  In general, for any positive integer $n$:
  $$
  A^n = \begin{pmatrix} 2^n & n \cdot 2^{n-1} \\ 0 & 2^n \end{pmatrix}
  $$