# Exercise 3. Swapping Two Rows

**Given:**

$$A = \begin{pmatrix} 1 & 2 & 0 \\\\ 0 & 3 & 1 \\\\ 2 & 1 & 1 \end{pmatrix}$$

---

### 1. Compute $\det(A)$ and Form $B$ by Swapping Rows $1$ and $2$ of $A$.

* **Method and Property Used:** The determinant of a $3 \times 3$ matrix can be computed by Sarrus's rule or cofactor expansion along a sparse row/column. Swapping two rows of a matrix produces a new matrix with the same rows in permuted order.

* **Compute $\det(A)$:**
  * *Main steps:* Expanding along the first column (which contains a zero in the second entry) gives:

$$\det(A) = 1 \cdot \det\begin{pmatrix} 3 & 1 \\\\ 1 & 1 \end{pmatrix} - 0 \cdot \det\begin{pmatrix} 2 & 0 \\\\ 1 & 1 \end{pmatrix} + 2 \cdot \det\begin{pmatrix} 2 & 0 \\\\ 3 & 1 \end{pmatrix}$$

    Evaluate the $2 \times 2$ determinants:
    * $\det\begin{pmatrix} 3 & 1 \\\\ 1 & 1 \end{pmatrix} = (3)(1) - (1)(1) = 3 - 1 = 2$
    * $\det\begin{pmatrix} 2 & 0 \\\\ 3 & 1 \end{pmatrix} = (2)(1) - (0)(3) = 2 - 0 = 2$

    Combine terms:

$$\det(A) = 1(2) - 0 + 2(2) = 2 + 4$$

  * *Result:*

$$\det(A) = 6$$

  * *Verification:* Using Sarrus's rule on $A$:
    * Down-right products: $(1)(3)(1) + (2)(1)(2) + (0)(0)(1) = 3 + 4 + 0 = 7$.
    * Up-right products: $(2)(3)(0) + (1)(1)(1) + (1)(0)(2) = 0 + 1 + 0 = 1$.
    * $\det(A) = 7 - 1 = 6$, matching cofactor expansion.

* **Form $B$ by Swapping Row $1$ and Row $2$ of $A$:**
  * *Result:*

$$B = \begin{pmatrix} 0 & 3 & 1 \\\\ 1 & 2 & 0 \\\\ 2 & 1 & 1 \end{pmatrix}$$

  * *Verification:* Row $1$ of $B$ equals row $2$ of $A$ $\begin{pmatrix} 0 & 3 & 1 \end{pmatrix}$, row $2$ of $B$ equals row $1$ of $A$ $\begin{pmatrix} 1 & 2 & 0 \end{pmatrix}$, and row $3$ remains $\begin{pmatrix} 2 & 1 & 1 \end{pmatrix}$.

---

### 2. Predict $\det(B)$ Using a Determinant Property, Then Verify by Computation.

* **Method and Property Used:** **Swapping any two rows of a square matrix flips the sign of its determinant**: if $B$ is obtained by swapping two rows of $A$, then $\det(B) = -\det(A)$.

* **Prediction:**
  * *Result:* Since $\det(A) = 6$, we predict:

$$\det(B) = -\det(A) = -6$$

* **Verification by Direct Computation:**
  * *Main steps:* Expand $\det(B)$ along the first row (which has $0$ in the first entry):

$$\det(B) = 0 \cdot \det\begin{pmatrix} 2 & 0 \\\\ 1 & 1 \end{pmatrix} - 3 \cdot \det\begin{pmatrix} 1 & 0 \\\\ 2 & 1 \end{pmatrix} + 1 \cdot \det\begin{pmatrix} 1 & 2 \\\\ 2 & 1 \end{pmatrix}$$

    Evaluate the $2 \times 2$ determinants:
    * $\det\begin{pmatrix} 1 & 0 \\\\ 2 & 1 \end{pmatrix} = (1)(1) - (0)(2) = 1$
    * $\det\begin{pmatrix} 1 & 2 \\\\ 2 & 1 \end{pmatrix} = (1)(1) - (2)(2) = 1 - 4 = -3$

    Combine terms:

$$\det(B) = 0 - 3(1) + 1(-3) = -3 - 3$$

  * *Result:*

$$\det(B) = -6$$

  * *Verification:* Direct calculation gives $\det(B) = -6$, which matches the predicted value $-\det(A) = -6$ exactly.
