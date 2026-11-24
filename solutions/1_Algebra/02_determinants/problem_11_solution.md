# Exercise 11. Shortening Computation via Row Operations

**Given:**

$$A = \begin{pmatrix} 1 & 2 & 3 \\\\ 1 & 3 & 4 \\\\ 1 & 4 & 6 \end{pmatrix}$$

---

### Compute $\det(A)$ by First Performing Row Operations to Create as Many Zeros as Possible, and State Which Operations Leave the Determinant Unchanged.

* **Method and Property Used:**
  * **Row-replacement invariance:** Adding a scalar multiple of one row to another row ($R_i \leftarrow R_i + k R_j$, $i \neq j$) leaves the determinant **completely unchanged**.
  * **Upper-triangular determinant rule:** Once all entries below the main diagonal are zero, the determinant equals the product of the main diagonal entries.

* **Main steps:**
  * **Step 1 — Create zeros in Column 1 below the $(1,1)$ pivot:** Apply $R_2 \leftarrow R_2 - R_1$ and $R_3 \leftarrow R_3 - R_1$:
    * *Effect on determinant:* **Unchanged**, because each operation adds a multiple ($-1$) of Row $1$ to another row.

$$\det(A) = \det\begin{pmatrix} 1 & 2 & 3 \\\\ 1 & 3 & 4 \\\\ 1 & 4 & 6 \end{pmatrix} = \det\begin{pmatrix} 1 & 2 & 3 \\\\ 0 & 1 & 1 \\\\ 0 & 2 & 3 \end{pmatrix}$$

  * **Step 2 — Create a zero in Column 2 below the $(2,2)$ pivot:** Apply $R_3 \leftarrow R_3 - 2R_2$:
    * *Effect on determinant:* **Unchanged**, because adding $-2 \times \text{Row } 2$ to $\text{Row } 3$ is a row-replacement operation.

$$\det(A) = \det\begin{pmatrix} 1 & 2 & 3 \\\\ 0 & 1 & 1 \\\\ 0 & 0 & 1 \end{pmatrix}$$

  * **Step 3 — Evaluate the resulting upper-triangular matrix:** Multiply the diagonal entries ($1$, $1$, and $1$):

$$\det(A) = (1)(1)(1) = 1$$

* **Result:**

$$\det(A) = 1$$

* **Verification:** Check using Sarrus's rule directly on the original matrix $A$:
  * Down-right products: $(1)(3)(6) + (2)(4)(1) + (3)(1)(4) = 18 + 8 + 12 = 38$.
  * Up-right products: $(1)(3)(3) + (4)(4)(1) + (6)(1)(2) = 9 + 16 + 12 = 37$.
  * $\det(A) = 38 - 37 = 1$, matching the result obtained via row reduction.
