# Exercise 12: Formula for a Matrix Power

### Given:
Based on the problem statement[cite: 6]:
$$A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$$

---

### Step 1: Compute $A^2$, $A^3$, and $A^4$[cite: 6]

* **Compute $A^2 = A \cdot A$:**
  $$
  A^2 = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (1)(1)+(1)(0) & (1)(1)+(1)(1) \\ (0)(1)+(1)(0) & (0)(1)+(1)(1) \end{pmatrix} = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}
  $$

* **Compute $A^3 = A^2 \cdot A$:**
  $$
  A^3 = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (1)(1)+(2)(0) & (1)(1)+(2)(1) \\ (0)(1)+(1)(0) & (0)(1)+(1)(1) \end{pmatrix} = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}
  $$

* **Compute $A^4 = A^3 \cdot A$:**
  $$
  A^4 = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (1)(1)+(3)(0) & (1)(1)+(3)(1) \\ (0)(1)+(1)(0) & (0)(1)+(1)(1) \end{pmatrix} = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}
  $$

---

### Step 2: Formulate a Conjecture for $A^n$[cite: 6]

Observing the pattern from our computations:
* $A^1 = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$
* $A^2 = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}$
* $A^3 = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}$
* $A^4 = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}$

We can formulate the general conjecture for any positive integer $n$[cite: 6]:
$$
A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}
$$

---

### Step 3: Verify via Multiplication ($n$ to $n + 1$)[cite: 6]

Assume the formula holds true for some arbitrary power $n$, so $A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$[cite: 6]. 

To find $A^{n+1}$, multiply this expression by $A$[cite: 6]:
$$
\begin{aligned}
A^{n+1} &= A^n \cdot A \\
&= \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \\
&= \begin{pmatrix} (1)(1) + (n)(0) & (1)(1) + (n)(1) \\ (0)(1) + (1)(0) & (0)(1) + (1)(1) \end{pmatrix} \\
&= \begin{pmatrix} 1 & 1 + n \\ 0 & 1 \end{pmatrix} \\
&= \begin{pmatrix} 1 & n + 1 \\ 0 & 1 \end{pmatrix}
\end{aligned}
$$

This result yields **exactly** the original formula with $n$ replaced by $n + 1$, thereby confirming that the pattern holds for all positive integers $n$[cite: 6].