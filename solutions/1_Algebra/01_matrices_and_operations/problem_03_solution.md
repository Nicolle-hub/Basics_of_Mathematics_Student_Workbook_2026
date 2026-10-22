# Exercise 3: When Can Matrices Be Multiplied?

### Dimension Compatibility Rule:
For two matrices $M_{m \times n}$ and $N_{p \times q}$, the product $MN$ is **defined** if and only if the number of columns in $M$ equals the number of rows in $N$ ($n = p$). 
If defined, the resulting matrix has size **$m \times q$**.

---

### Given Matrix Sizes:
* $A_{2 \times 3}$
* $B_{3 \times 4}$
* $C_{4 \times 2}$
* $D_{2 \times 2}$

---

### Analysis of Products:

| Product | Inner Dimensions Match? | Defined? | Resulting Size | Justification |
| :--- | :---: | :---: | :---: | :--- |
| **$AB$** | $(2 \times \mathbf{3}) \times (\mathbf{3} \times 4)$ | **Yes** | **$2 \times 4$** | Inner dimensions match ($3 = 3$). |
| **$BA$** | $(3 \times \mathbf{4}) \times (\mathbf{2} \times 3)$ | **No** | **Undefined** | Number of columns in $B$ ($4$) $\neq$ rows in $A$ ($2$). |
| **$BC$** | $(3 \times \mathbf{4}) \times (\mathbf{4} \times 2)$ | **Yes** | **$3 \times 2$** | Inner dimensions match ($4 = 4$). |
| **$CB$** | $(4 \times \mathbf{2}) \times (\mathbf{3} \times 4)$ | **No** | **Undefined** | Number of columns in $C$ ($2$) $\neq$ rows in $B$ ($3$). |
| **$AC$** | $(2 \times \mathbf{3}) \times (\mathbf{4} \times 2)$ | **No** | **Undefined** | Number of columns in $A$ ($3$) $\neq$ rows in $C$ ($4$). |
| **$CA$** | $(4 \times \mathbf{2}) \times (\mathbf{2} \times 3)$ | **Yes** | **$4 \times 3$** | Inner dimensions match ($2 = 2$). |
| **$AD$** | $(2 \times \mathbf{3}) \times (\mathbf{2} \times 2)$ | **No** | **Undefined** | Number of columns in $A$ ($3$) $\neq$ rows in $D$ ($2$). |
| **$DA$** | $(2 \times \mathbf{2}) \times (\mathbf{2} \times 3)$ | **Yes** | **$2 \times 3$** | Inner dimensions match ($2 = 2$). |

---

### Summary of Defined Products:
* **$AB$** is defined with size **$2 \times 4$**
* **$BC$** is defined with size **$3 \times 2$**
* **$CA$** is defined with size **$4 \times 3$**
* **$DA$** is defined with size **$2 \times 3$**