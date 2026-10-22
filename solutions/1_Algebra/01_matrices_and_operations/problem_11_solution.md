# Exercise 11: When Do Matrices Commute?

### Given:
Based on the problem statement[cite: 10]:
$$A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}, \quad B = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$$

---

### Step 1: Compute $AB$

$$
\begin{aligned}
AB &= \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} a & b \\ c & d \end{pmatrix} \\
&= \begin{pmatrix} (1)(a) + (1)(c) & (1)(b) + (1)(d) \\ (0)(a) + (1)(c) & (0)(b) + (1)(d) \end{pmatrix} \\
&= \begin{pmatrix} a + c & b + d \\ c & d \end{pmatrix}
\end{aligned}
$$

---

### Step 2: Compute $BA$

$$
\begin{aligned}
BA &= \begin{pmatrix} a & b \\ c & d \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \\
&= \begin{pmatrix} (a)(1) + (b)(0) & (a)(1) + (b)(1) \\ (c)(1) + (d)(0) & (c)(1) + (d)(1) \end{pmatrix} \\
&= \begin{pmatrix} a & a + b \\ c & c + d \end{pmatrix}
\end{aligned}
$$

---

### Step 3: Find Conditions for $AB = BA$

Set the product matrices equal to each other[cite: 10]:
$$
\begin{pmatrix} a + c & b + d \\ c & d \end{pmatrix} = \begin{pmatrix} a & a + b \\ c & c + d \end{pmatrix}
$$

By equating corresponding entries, we get the following system of equations[cite: 10]:
1. $a + c = a \implies c = 0$[cite: 10]
2. $b + d = a + b \implies d = a$[cite: 10]
3. $c = c$ (automatically satisfies since $c = 0$)[cite: 10]
4. $d = c + d \implies c = 0$ (consistent)[cite: 10]

Thus, the required conditions on the entries are[cite: 10]:
* **$c = 0$**[cite: 10]
* **$d = a$**[cite: 10]
* $a$ and $b$ can be any real numbers (free variables)[cite: 10].

---

### Step 4: General Form of Matrix $B$

Substituting $c = 0$ and $d = a$ back into matrix $B$[cite: 10]:
$$
B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix}
$$

As established, any matrix $B$ that commutes with $A$ must be of this upper-triangular form, where the diagonal entries are equal and the lower-left entry is zero[cite: 10].