# Exercise 6. Parameter and Invertibility

**Given:**

$$A(t) = \begin{pmatrix} t & 1 \\\\ 2 & t \end{pmatrix}$$

---

### 1. Find All Values of $t$ for Which $A(t)$ Is Not Invertible.

* **Method and Property Used:** A square matrix is **not invertible** (singular) if and only if its determinant equals zero: $\det(A(t)) = 0$. For a $2 \times 2$ matrix $\begin{pmatrix} a & b \\\\ c & d \end{pmatrix}$, $\det = ad - bc$.

* **Main steps:**
  * Compute $\det(A(t))$ as a function of $t$:

$$\det(A(t)) = \det\begin{pmatrix} t & 1 \\\\ 2 & t \end{pmatrix} = (t)(t) - (1)(2) = t^2 - 2$$

  * Set $\det(A(t)) = 0$ and solve for $t$:

$$t^2 - 2 = 0 \implies t^2 = 2 \implies t = \pm\sqrt{2}$$

* **Result:**

$$t = \sqrt{2} \qquad \text{and} \qquad t = -\sqrt{2}$$

* **Verification:** Substituting both values back into $\det(A(t)) = t^2 - 2$:
  * For $t = \sqrt{2}$: $(\sqrt{2})^2 - 2 = 2 - 2 = 0$.
  * For $t = -\sqrt{2}$: $(-\sqrt{2})^2 - 2 = 2 - 2 = 0$.

---

### 2. Explain How the Answer Relates to the Determinant Being Zero.

* **Explanation and Method Used:** The determinant acts as an exact algebraic test for invertibility:
  * When $\det(A(t)) = t^2 - 2 = 0$ (i.e., $t = \pm\sqrt{2}$), the rows (and columns) of $A(t)$ become linearly dependent—specifically, row $2$ is $\sqrt{2}$ times row $1$ for $t = \sqrt{2}$, and $-\sqrt{2}$ times row $1$ for $t = -\sqrt{2}$. Because the matrix collapses two-dimensional space onto a line, no inverse matrix $A(t)^{-1}$ exists (and the $2 \times 2$ inverse formula would require dividing by $\det(A(t)) = 0$).
  * For every other real value $t \notin \{-\sqrt{2}, \sqrt{2}\}$, $\det(A(t)) = t^2 - 2 \neq 0$, so $A(t)$ is invertible.

* **Result:** $A(t)$ fails to be invertible precisely at the roots of the determinant polynomial $\det(A(t)) = t^2 - 2 = 0$, namely $t = \pm\sqrt{2}$.

* **Verification:** Checking $t = \sqrt{2}$ directly in $A(t)$ gives:

$$A(\sqrt{2}) = \begin{pmatrix} \sqrt{2} & 1 \\\\ 2 & \sqrt{2} \end{pmatrix}$$

  Multiplying the first row $\begin{pmatrix} \sqrt{2} & 1 \end{pmatrix}$ by $\sqrt{2}$ gives $\begin{pmatrix} 2 & \sqrt{2} \end{pmatrix}$, which is identical to the second row, confirming linear dependence and non-invertibility.
