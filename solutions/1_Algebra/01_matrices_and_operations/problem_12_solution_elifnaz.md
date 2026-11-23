# Exercise 12. Matrix Power Formula

**Given:**

$$A = \begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix}$$

---

### 1. Compute $A^2$, $A^3$, and $A^4$, and Conjecture a Formula for $A^n$.

* **Method and Property Used:** Positive integer powers of a square matrix are computed by repeated matrix multiplication ($A^k = A^{k-1}A$). Recognizing how a specific entry grows across successive powers lets us generalize from concrete calculations to a closed-form pattern for any integer $n \ge 1$.

* **Compute $A^2$, $A^3$, and $A^4$:**
  * *Main steps:* Multiply step by step using row-by-column dot products:

$$A^2 = \begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(1) + 1(0) & 1(1) + 1(1) \\\\ 0(1) + 1(0) & 0(1) + 1(1) \end{pmatrix}$$

$$A^3 = A^2 A = \begin{pmatrix} 1 & 2 \\\\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(1) + 2(0) & 1(1) + 2(1) \\\\ 0(1) + 1(0) & 0(1) + 1(1) \end{pmatrix}$$

$$A^4 = A^3 A = \begin{pmatrix} 1 & 3 \\\\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(1) + 3(0) & 1(1) + 3(1) \\\\ 0(1) + 1(0) & 0(1) + 1(1) \end{pmatrix}$$

  * *Result:*

$$A^2 = \begin{pmatrix} 1 & 2 \\\\ 0 & 1 \end{pmatrix}, \qquad A^3 = \begin{pmatrix} 1 & 3 \\\\ 0 & 1 \end{pmatrix}, \qquad A^4 = \begin{pmatrix} 1 & 4 \\\\ 0 & 1 \end{pmatrix}$$

  * *Verification:* Each multiplication keeps the diagonal entries equal to $1$, the lower-left entry equal to $0$, and increases the upper-right entry by $1$ per step ($1 \to 2 \to 3 \to 4$).

* **Conjecture for $A^n$ ($n \ge 1$):**
  * *Result:*

$$A^n = \begin{pmatrix} 1 & n \\\\ 0 & 1 \end{pmatrix}$$

  * *Verification:* Plugging $n = 2$, $n = 3$, and $n = 4$ into $\begin{pmatrix} 1 & n \\\\ 0 & 1 \end{pmatrix}$ reproduces the exact matrices found above.

---

### 2. Assume the Formula Holds for $n$, Multiply by $A$, and Explain Why It Yields $n + 1$.

* **Method and Property Used:** Using the inductive step of mathematical proof, assuming $A^n = \begin{pmatrix} 1 & n \\\\ 0 & 1 \end{pmatrix}$ and computing $A^{n+1} = A^n A$ shows algebraically why the upper-right entry increases by $1$ while all other entries stay fixed (geometrically, a horizontal shear by $n$ units followed by a horizontal shear by $1$ unit equals a horizontal shear by $n + 1$ units).

* **Main steps:** Multiply $A^n$ on the right by $A$:

$$A^{n+1} = A^n A = \begin{pmatrix} 1 & n \\\\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(1) + n(0) & 1(1) + n(1) \\\\ 0(1) + 1(0) & 0(1) + 1(1) \end{pmatrix}$$

* **Result:**

$$A^{n+1} = \begin{pmatrix} 1 & n + 1 \\\\ 0 & 1 \end{pmatrix}$$

* **Explanation and Verification:**
  * Entry $(1, 1)$ is $1 \cdot 1 + n \cdot 0 = 1$.
  * Entry $(1, 2)$ is $1 \cdot 1 + n \cdot 1 = n + 1$, so adding one more factor of $A$ adds $1$ to the previous upper-right entry $n$.
  * Entry $(2, 1)$ is $0 \cdot 1 + 1 \cdot 0 = 0$.
  * Entry $(2, 2)$ is $0 \cdot 1 + 1 \cdot 1 = 1$.
  * Because the resulting matrix matches the conjectured formula with $n$ replaced by $n + 1$, the formula holds for $n + 1$ whenever it holds for $n$.

---

> **Purpose of this exercise:** to practice spotting a pattern across matrix powers, forming a general conjecture, and seeing algebraically why multiplying by $A$ advances the formula from $n$ to $n + 1$.
