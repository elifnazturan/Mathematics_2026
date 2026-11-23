# Exercise 5. Row Operations

**Given:**

$$A = \begin{pmatrix} 1 & 2 & 3 \\\\ 2 & 1 & 0 \\\\ -1 & 4 & 2 \end{pmatrix}$$

---

### Compute $\det(A)$ by Simplifying With Row Operations and Track How the Determinant Changes at Each Step.

* **Method and Property Used:** Elementary row operations affect a determinant in well-defined ways:
  * **Adding a multiple of one row to another row** ($R_i \leftarrow R_i + k R_j$, $i \neq j$) leaves the determinant **unchanged**.
  * **Swapping two rows** ($R_i \leftrightarrow R_j$) **flips the sign** of the determinant ($\det \to -\det$).
  * **Scaling a row by a nonzero scalar $k$** ($R_i \leftarrow k R_i$) **multiplies the determinant by $k$** ($\det \to k\det$).

* **Main steps:**
  * **Step 1 — Eliminate entries below the pivot in Column 1:** Apply $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 + R_1$:
    * *Effect on determinant:* **Unchanged** (adding a scalar multiple of one row to another row does not change $\det$).

$$\det(A) = \det\begin{pmatrix} 1 & 2 & 3 \\\\ 2 & 1 & 0 \\\\ -1 & 4 & 2 \end{pmatrix} = \det\begin{pmatrix} 1 & 2 & 3 \\\\ 0 & -3 & -6 \\\\ 0 & 6 & 5 \end{pmatrix}$$

  * **Step 2 — Eliminate the entry below the pivot in Column 2:** Apply $R_3 \leftarrow R_3 + 2R_2$:
    * *Effect on determinant:* **Unchanged** (adding $2 \times \text{Row } 2$ to $\text{Row } 3$ leaves $\det$ unchanged).

$$\det(A) = \det\begin{pmatrix} 1 & 2 & 3 \\\\ 0 & -3 & -6 \\\\ 0 & 0 & -7 \end{pmatrix}$$

  * **Step 3 — Evaluate the resulting upper-triangular determinant:** Multiply the main diagonal entries ($1$, $-3$, and $-7$):
    * *Effect on determinant:* **No row operation is applied**; the determinant of an upper-triangular matrix equals the product of its diagonal entries.

$$\det(A) = (1)(-3)(-7) = 21$$

* **Result:**

$$\det(A) = 21$$

* **Verification:** Check using Sarrus's rule on the original matrix $A$:
  * Down-right products: $(1)(1)(2) + (2)(0)(-1) + (3)(2)(4) = 2 + 0 + 24 = 26$.
  * Up-right products: $(2)(1)(3) + (1)(0)(4) + (2)(2)(-1) = 6 + 0 - 4 = 2$.
  * $\det(A) = 26 - 2 = 24$? Wait — let's check entry $(2,3)$ up-right: main up-right diagonals of $\begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 0 \\ -1 & 4 & 2 \end{pmatrix}$ are:
    * $(-1)(1)(3) = -3$
    * $(4)(0)(1) = 0$
    * $(2)(2)(2) = 8$
  * Sum of up-right products: $-3 + 0 + 8 = 5$.
  * $\det(A) = 26 - 5 = 21$, which matches $(1)(-3)(-7) = 21$ from the row-reduced triangular form.
