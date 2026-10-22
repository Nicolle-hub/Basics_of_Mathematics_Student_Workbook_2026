# Exercise 9: Composing Transformations

### Given:
* Scaling matrix: $S = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}$ (describes nonuniform scaling)[cite: 8]
* Rotation matrix: $R = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}$ (describes a $90^\circ$ counterclockwise rotation)[cite: 8]
* Vector: $x = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$[cite: 8]

---

### 1. Compute $RSx$

**Step 1: Compute $Sx$**
$$
Sx = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} (2)(1) + (0)(2) \\ (0)(1) + (1)(2) \end{pmatrix} = \begin{pmatrix} 2 \\ 2 \end{pmatrix}
$$

**Step 2: Compute $R(Sx)$**
$$
RSx = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 2 \\ 2 \end{pmatrix} = \begin{pmatrix} (0)(2) + (-1)(2) \\ (1)(2) + (0)(2) \end{pmatrix} = \begin{pmatrix} -2 \\ 2 \end{pmatrix}
$$

---

### 2. Compute $SRx$

**Step 1: Compute $Rx$**
$$
Rx = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} (0)(1) + (-1)(2) \\ (1)(1) + (0)(2) \end{pmatrix} = \begin{pmatrix} -2 \\ 1 \end{pmatrix}
$$

**Step 2: Compute $S(Rx)$**
$$
SRx = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} -2 \\ 1 \end{pmatrix} = \begin{pmatrix} (2)(-2) + (0)(1) \\ (0)(-2) + (1)(1) \end{pmatrix} = \begin{pmatrix} -4 \\ 1 \end{pmatrix}
$$

---

### 3. Comparison and Geometric Explanation

* **Results:** $RSx = \begin{pmatrix} -2 \\ 2 \end{pmatrix}$ and $SRx = \begin{pmatrix} -4 \\ 1 \end{pmatrix}$. Comparing the results, $RSx \neq SRx$[cite: 8].
* **Geometric Meaning:** 
  * In **$RSx$**, the vector $x$ is first scaled horizontally by a factor of 2 to become $\begin{pmatrix} 2 \\ 2 \end{pmatrix}$, and then that scaled result is rotated $90^\circ$ counterclockwise to arrive at $\begin{pmatrix} -2 \\ 2 \end{pmatrix}$.
  * In **$SRx$**, the vector $x$ is first rotated $90^\circ$ counterclockwise to $\begin{pmatrix} -2 \\ 1 \end{pmatrix}$, and then that *rotated* vector is scaled horizontally by a factor of 2, resulting in $\begin{pmatrix} -4 \\ 1 \end{pmatrix}$. 
  
  Because matrix transformations are non-commutative, the order matters because applying the first transformation changes the spatial orientation or dimensions of the vector before the second transformation takes place[cite: 8].