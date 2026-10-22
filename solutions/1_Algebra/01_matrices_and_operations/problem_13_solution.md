# Exercise 13: A Recurrence Written in Matrix Form

### Given:

$$F = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}$$

---

### Step 1: Compute $F^2$, $F^3$, $F^4$, and $F^5$

**1. Compute $F^2 = F \cdot F$:**

$$
F^2 = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (1)(1) + (1)(1) & (1)(1) + (1)(0) \\ (1)(1) + (0)(1) & (1)(1) + (0)(0) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}
$$

**2. Compute $F^3 = F^2 \cdot F$:**

$$
F^3 = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (2)(1) + (1)(1) & (2)(1) + (1)(0) \\ (1)(1) + (1)(1) & (1)(1) + (1)(0) \end{pmatrix} = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}
$$

**3. Compute $F^4 = F^3 \cdot F$:**

$$
F^4 = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (3)(1) + (2)(1) & (3)(1) + (2)(0) \\ (2)(1) + (1)(1) & (2)(1) + (1)(0) \end{pmatrix} = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}
$$

**4. Compute $F^5 = F^4 \cdot F$:**

$$
F^5 = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (5)(1) + (3)(1) & (5)(1) + (3)(0) \\ (3)(1) + (2)(1) & (3)(1) + (2)(0) \end{pmatrix} = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}
$$

---

### Step 2: Comparison with the Fibonacci Sequence

Comparing the matrix entries with the sequence $0, 1, 1, 2, 3, 5, 8, \dots$ (the Fibonacci sequence $F_0=0, F_1=1, F_2=1, F_3=2, F_4=3, F_5=5, F_6=8, \dots$), we observe:

* $F^1 = \begin{pmatrix} F_2 & F_1 \\ F_1 & F_0 \end{pmatrix} = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}$
* $F^2 = \begin{pmatrix} F_3 & F_2 \\ F_2 & F_1 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}$
* $F^3 = \begin{pmatrix} F_4 & F_3 \\ F_3 & F_2 \end{pmatrix} = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}$
* $F^4 = \begin{pmatrix} F_5 & F_4 \\ F_4 & F_3 \end{pmatrix} = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}$
* $F^5 = \begin{pmatrix} F_6 & F_5 \\ F_5 & F_4 \end{pmatrix} = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}$

In general, the matrix power $F^n$ contains consecutive Fibonacci numbers:

$$
F^n = \begin{pmatrix} F_{n+1} & F_n \\ F_n & F_{n-1} \end{pmatrix}
$$

---

### Step 3: Multiplying by a State Vector

Computing the product of $F$ with the vector $\begin{pmatrix} a \\ b \end{pmatrix}$:

$$
F \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} (1)(a) + (1)(b) \\ (1)(a) + (0)(b) \end{pmatrix} = \begin{pmatrix} a + b \\ a \end{pmatrix}
$$

* **Explanation of the Recurrence Step:** 
  If $a$ and $b$ represent two consecutive terms in the sequence (where $a$ is the current term and $b$ is the previous term), multiplying by $F$ updates the state vector. The new top entry becomes $a + b$ (the next term in the sequence), while the bottom entry becomes $a$ (which shifts down to become the previous term for the subsequent step).