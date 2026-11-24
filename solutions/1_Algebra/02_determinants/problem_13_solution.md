# Exercise 13. Determinant by Elimination

**Given:**

$$A = \begin{pmatrix} 1 & 2 & 3 \\\\ 2 & 5 & 7 \\\\ 1 & 0 & 2 \end{pmatrix}$$

---

### Compute $\det(A)$ Using Elimination and Record the Effect of Each Row Operation on the Value of the Determinant.

* **Method and Property Used:**
  * **Gaussian elimination (row reduction to upper-triangular form):**
    * **Row replacement** ($R_i \leftarrow R_i + k R_j$, $i \neq j$) leaves the determinant **unchanged** ($\det \to \det$).
    * **Row swap** ($R_i \leftrightarrow R_j$) **flips the sign** of the determinant ($\det \to -\det$).
    * **Row scaling** ($R_i \leftarrow k R_i$, $k \neq 0$) **multiplies the determinant by $k$** ($\det \to k\det$).
  * **Upper-triangular determinant rule:** For an upper-triangular matrix $U$, $\det(U) = u_{11} u_{22} u_{33}$.

* **Main steps:**
  * **Step 1 — Eliminate entries below the $(1,1)$ pivot:** Apply $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$:
    * *Effect on determinant:* **Unchanged** (both are row-replacement operations).

$$\det(A) = \det\begin{pmatrix} 1 & 2 & 3 \\\\ 2 & 5 & 7 \\\\ 1 & 0 & 2 \end{pmatrix} = \det\begin{pmatrix} 1 & 2 & 3 \\\\ 0 & 1 & 1 \\\\ 0 & -2 & -1 \end{pmatrix}$$

  * **Step 2 — Eliminate the entry below the $(2,2)$ pivot:** Apply $R_3 \leftarrow R_3 + 2R_2$:
    * *Effect on determinant:* **Unchanged** (adding $2 \times \text{Row } 2$ to $\text{Row } 3$ is a row-replacement operation).

$$\det(A) = \det\begin{pmatrix} 1 & 2 & 3 \\\\ 0 & 1 & 1 \\\\ 0 & 0 & 1 \end{pmatrix}$$

  * **Step 3 — Compute the determinant of the upper-triangular matrix:** Multiply the main diagonal entries ($1$, $1$, and $1$):
    * *Effect on determinant:* **No row operation performed**; the determinant equals the product of the diagonal entries.

$$\det(A) = (1)(1)(1) = 1$$

* **Result:**

$$\det(A) = 1$$

* **Verification:** Check using Sarrus's rule directly on the original matrix $A$:
  * Down-right products: $(1)(5)(2) + (2)(7)(1) + (3)(2)(0) = 10 + 14 + 0 = 24$.
  * Up-right products: $(1)(5)(3) + (0)(7)(1) + (2)(2)(2) = 15 + 0 + 8 = 23$.
  * $\det(A) = 24 - 23 = 1$, matching the value obtained via elimination.
