## Exercise 13. A Recurrence Written in Matrix Form



### Problem Statement

Let

$$F = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}$$

Compute $F^2$, $F^3$, $F^4$, and $F^5$. Compare the numbers obtained with the sequence

$$0, 1, 1, 2, 3, 5, 8, \dots$$

and describe the relationship you observe. Then compute

$$F \begin{pmatrix} a \\ b \end{pmatrix}$$

and explain how this multiplication performs one recurrence step: it creates the sum of two consecutive terms and keeps one of them for the next step.

---

### Solution

#### 1. Computing Matrix Powers

Given the matrix $F = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}$:

* **Compute $F^2$:**

$$F^2 = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (1\cdot 1 + 1\cdot 1) & (1\cdot 1 + 1\cdot 0) \\ (1\cdot 1 + 0\cdot 1) & (1\cdot 1 + 0\cdot 0) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}$$


* **Compute $F^3$:**

$$F^3 = F^2 \cdot F = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (2\cdot 1 + 1\cdot 1) & (2\cdot 1 + 1\cdot 0) \\ (1\cdot 1 + 1\cdot 1) & (1\cdot 1 + 1\cdot 0) \end{pmatrix} = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}$$


* **Compute $F^4$:**

$$F^4 = F^3 \cdot F = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (3\cdot 1 + 2\cdot 1) & (3\cdot 1 + 2\cdot 0) \\ (2\cdot 1 + 1\cdot 1) & (2\cdot 1 + 1\cdot 0) \end{pmatrix} = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}$$


* **Compute $F^5$:**

$$F^5 = F^4 \cdot F = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (5\cdot 1 + 3\cdot 1) & (5\cdot 1 + 3\cdot 0) \\ (3\cdot 1 + 2\cdot 1) & (3\cdot 1 + 2\cdot 0) \end{pmatrix} = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}$$



---

#### 2. Comparing with the Fibonacci Sequence

The given sequence is the Fibonacci sequence:


$$F_0 = 0, \; F_1 = 1, \; F_2 = 1, \; F_3 = 2, \; F_4 = 3, \; F_5 = 5, \; F_6 = 8, \dots$$

Observing the powers of matrix $F$, we notice that general powers of $F$ contain consecutive Fibonacci numbers:


$$F^n = \begin{pmatrix} F_{n+1} & F_n \\ F_n & F_{n-1} \end{pmatrix}$$

Specifically:

* $F^2 = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} = \begin{pmatrix} F_3 & F_2 \\ F_2 & F_1 \end{pmatrix}$
* $F^3 = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix} = \begin{pmatrix} F_4 & F_3 \\ F_3 & F_2 \end{pmatrix}$
* $F^4 = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix} = \begin{pmatrix} F_5 & F_4 \\ F_4 & F_3 \end{pmatrix}$
* $F^5 = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix} = \begin{pmatrix} F_6 & F_5 \\ F_5 & F_4 \end{pmatrix}$

---

#### 3. Matrix-Vector Multiplication and Recurrence Step

Computing the product of $F$ with a column vector $\begin{pmatrix} a \\ b \end{pmatrix}$:

$$F \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} 1\cdot a + 1\cdot b \\ 1\cdot a + 0\cdot b \end{pmatrix} = \begin{pmatrix} a + b \\ a \end{pmatrix}$$

**Explanation:**

* **The top entry ($a + b$):** Creates the sum of the two consecutive terms ($a$ and $b$), representing the next term in the recurrence sequence.


* **The bottom entry ($a$):** Keeps the previous term ($a$) so it can move down to become the secondary term in the subsequent recurrence step.