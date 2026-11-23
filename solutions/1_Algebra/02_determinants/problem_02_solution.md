# Exercise 2. Determinant of a $3 \times 3$ Matrix

**Given:**

$$A = \begin{pmatrix} 1 & 2 & -1 \\\\ 0 & 3 & 4 \\\\ 2 & 1 & 5 \end{pmatrix}$$

---

### 1. Compute $\det(A)$ Using Sarrus's Rule.

* **Method and Property Used:** For a $3 \times 3$ matrix, **Sarrus's rule** computes the determinant by adjoining the first two columns to the right, summing the products along the three main diagonals (going down-right), and subtracting the sum of the products along the three anti-diagonals (going up-right).

* **Main steps:**
  * Main diagonals (down-right):
    * $(1)(3)(5) = 15$
    * $(2)(4)(2) = 16$
    * $(-1)(0)(1) = 0$
    * Sum of down-right products: $15 + 16 + 0 = 31$.

  * Anti-diagonals (up-right):
    * $(2)(3)(-1) = -6$
    * $(1)(4)(1) = 4$
    * $(5)(0)(2) = 0$
    * Sum of up-right products: $-6 + 4 + 0 = -2$.

  * Subtract the anti-diagonal sum from the main-diagonal sum:

$$\det(A) = (15 + 16 + 0) - (-6 + 4 + 0) = 31 - (-2) = 31 + 2$$

* **Result:**

$$\det(A) = 33$$

* **Verification:** Checking each diagonal product separately confirms $1 \cdot 3 \cdot 5 = 15$, $2 \cdot 4 \cdot 2 = 16$, $(-1) \cdot 0 \cdot 1 = 0$, and for the reverse diagonals $2 \cdot 3 \cdot (-1) = -6$, $1 \cdot 4 \cdot 1 = 4$, $5 \cdot 0 \cdot 2 = 0$; $31 - (-2) = 33$.

---

### 2. Perform a Simple Check Using a Chosen Property of Determinants.

* **Method and Property Used:** **Cofactor expansion along the first column** (a standard determinant property/method) states that $\det(A) = a_{11}C_{11} + a_{21}C_{21} + a_{31}C_{31}$. Because $a_{21} = 0$ in the first column, the second term vanishes immediately, giving a fast check without repeating full Sarrus work.

* **Main steps:** Expand along column $1$:

$$\det(A) = 1 \cdot \det\begin{pmatrix} 3 & 4 \\\\ 1 & 5 \end{pmatrix} - 0 \cdot \det\begin{pmatrix} 2 & -1 \\\\ 1 & 5 \end{pmatrix} + 2 \cdot \det\begin{pmatrix} 2 & -1 \\\\ 3 & 4 \end{pmatrix}$$

  * Compute the two nonzero $2 \times 2$ determinants:
    * $\det\begin{pmatrix} 3 & 4 \\\\ 1 & 5 \end{pmatrix} = (3)(5) - (4)(1) = 15 - 4 = 11$
    * $\det\begin{pmatrix} 2 & -1 \\\\ 3 & 4 \end{pmatrix} = (2)(4) - (-1)(3) = 8 + 3 = 11$

  * Combine the terms:

$$\det(A) = 1(11) - 0 + 2(11) = 11 + 22$$

* **Result:**

$$\det(A) = 33$$

* **Verification:** Both Sarrus's rule ($33$) and first-column expansion ($11 + 22 = 33$) give the exact same value, confirming $\det(A) = 33$ and showing $A$ is invertible ($\det(A) \neq 0$).

