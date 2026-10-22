Here is the step-by-step solution based on the exercise in the image, formatted in clear markdown without any LaTeX dollar signs.

---

### **1. Compute the Powers of Matrix A**

Let the matrix $A$ be:
[ 1 1 ]
[ 0 1 ]

#### **Computing $A^2$:**

$A^2 = A \times A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (1 \cdot 1 + 1 \cdot 0) & (1 \cdot 1 + 1 \cdot 1) \\ (0 \cdot 1 + 1 \cdot 0) & (0 \cdot 1 + 1 \cdot 1) \end{pmatrix} = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}$

#### **Computing $A^3$:**

$A^3 = A^2 \times A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (1 \cdot 1 + 2 \cdot 0) & (1 \cdot 1 + 2 \cdot 1) \\ (0 \cdot 1 + 1 \cdot 0) & (0 \cdot 1 + 1 \cdot 1) \end{pmatrix} = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}$

#### **Computing $A^4$:**

$A^4 = A^3 \times A = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (1 \cdot 1 + 3 \cdot 0) & (1 \cdot 1 + 3 \cdot 1) \\ (0 \cdot 1 + 1 \cdot 0) & (0 \cdot 1 + 1 \cdot 1) \end{pmatrix} = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}$

---

### **2. Formulate the Conjecture for $A^n$**

Based on the pattern observed from computing $A^2$, $A^3$, and $A^4$, the top-right entry increases matching the power $n$, while the diagonal elements remain $1$ and the bottom-left remains $0$. Therefore, the conjecture is:

$A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$

---

### **3. Proof by Induction (Inductive Step)**

* **Assume the formula is true for some positive integer $n$:**
$A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$

* **Multiply by $A$ to find the formula for $n + 1$:**
$A^{n+1} = A^n \times A$


$A^{n+1} = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$

* **Perform the matrix multiplication:**
$A^{n+1} = \begin{pmatrix} (1 \cdot 1 + n \cdot 0) & (1 \cdot 1 + n \cdot 1) \\ (0 \cdot 1 + 1 \cdot 0) & (0 \cdot 1 + 1 \cdot 1) \end{pmatrix}$


$A^{n+1} = \begin{pmatrix} 1 & 1 + n \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & n + 1 \\ 0 & 1 \end{pmatrix}$


This matches the conjectured formula for $n + 1$, completing the explanation.