# Exercise 14: Rotation Matrices

### Given:

The matrix for a rotation through an angle $\theta$ is given by:

$$R(\theta) = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}$$

---

### Step 1: Compute $R(\alpha)R(\beta)$

Multiply the two rotation matrices using standard matrix multiplication:

$$
\begin{aligned}
R(\alpha)R(\beta) &= \begin{pmatrix} \cos\alpha & -\sin\alpha \\ \sin\alpha & \cos\alpha \end{pmatrix} \begin{pmatrix} \cos\beta & -\sin\beta \\ \sin\beta & \cos\beta \end{pmatrix} \\
&= \begin{pmatrix} 
\cos\alpha\cos\beta - \sin\alpha\sin\beta & -\cos\alpha\sin\beta - \sin\alpha\cos\beta \\ 
\sin\alpha\cos\beta + \cos\alpha\sin\beta & -\sin\alpha\sin\beta + \cos\alpha\cos\beta 
\end{pmatrix}
\end{aligned}
$$

---

### Step 2: Apply Trigonometric Angle-Sum Identities

Using the standard angle-sum formulas for sine and cosine:
* $\cos(\alpha + \beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$
* $\sin(\alpha + \beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$

We can rewrite each entry of the resulting matrix:
* **Top-left entry:** $\cos(\alpha + \beta)$
* **Top-right entry:** $-(\sin\alpha\cos\beta + \cos\alpha\sin\beta) = -\sin(\alpha + \beta)$
* **Bottom-left entry:** $\sin\alpha\cos\beta + \cos\alpha\sin\beta = \sin(\alpha + \beta)$
* **Bottom-right entry:** $\cos\alpha\cos\beta - \sin\alpha\sin\beta = \cos(\alpha + \beta)$

Substituting these back into the matrix yields:

$$
R(\alpha)R(\beta) = \begin{pmatrix} \cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta) \end{pmatrix} = R(\alpha+\beta)
$$

---

### Step 3: Geometric Explanation

* **Geometric Meaning:** 
  Multiplying the rotation matrix $R(\alpha)$ by $R(\beta)$ represents the **composition of two successive rotations**: first rotating a vector by an angle $\beta$, and then rotating the resulting vector by an angle $\alpha$.

* **Conclusion:** 
  Geometrically, applying a rotation of $\beta$ followed by a rotation of $\alpha$ is completely equivalent to performing a **single rotation by the combined angle $\alpha + \beta$**. This demonstrates the perfect consistency between matrix algebra and geometric transformations.