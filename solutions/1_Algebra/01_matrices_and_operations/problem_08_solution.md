# Exercise 8: Row Operations and Their Reversibility

### Given Matrix:
$$A = \begin{pmatrix} 1 & 2 & -1 \\ 2 & 4 & 1 \\ -1 & 1 & 3 \end{pmatrix}$$

---

### 1. Perform the Row Operations in Order

* **Step 1: $R_2 \leftarrow R_2 - 2R_1$**
  Subtract $2$ times Row 1 from Row 2:
  $$
  A_1 = \begin{pmatrix} 1 & 2 & -1 \\ 2 - 2(1) & 4 - 2(2) & 1 - 2(-1) \\ -1 & 1 & 3 \end{pmatrix} = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3 \end{pmatrix}
  $$

* **Step 2: $R_3 \leftarrow R_3 + R_1$**
  Add Row 1 to Row 3 (using the matrix from Step 1):
  $$
  A_2 = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 + 1 & 1 + 2 & 3 + (-1) \end{pmatrix} = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2 \end{pmatrix}
  $$

* **Step 3: Interchange $R_2$ and $R_3$**
  Swap Row 2 and Row 3 (using the matrix from Step 2):
  $$
  A_3 = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 3 \end{pmatrix}
  $$

---

### 2. Reversing Operations

Every elementary row operation is reversible, meaning we can undo its effect to return the matrix to its prior state:

1. **Reversing Step 1 ($R_2 \leftarrow R_2 - 2R_1$):**
   * *Original operation:* Subtracts $2$ times Row 1 from Row 2.
   * *Reverse operation:* **$R_2 \leftarrow R_2 + 2R_1$** (Add $2$ times Row 1 back to Row 2).

2. **Reversing Step 2 ($R_3 \leftarrow R_3 + R_1$):**
   * *Original operation:* Adds Row 1 to Row 3.
   * *Reverse operation:* **$R_3 \leftarrow R_3 - R_1$** (Subtract Row 1 from Row 3).

3. **Reversing Step 3 (Interchange $R_2$ and $R_3$):**
   * *Original operation:* Swaps Row 2 and Row 3.
   * *Reverse operation:* **Interchange $R_2$ and $R_3$ again** (Swapping them a second time restores the original rows).