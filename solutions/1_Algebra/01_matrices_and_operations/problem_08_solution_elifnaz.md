# Exercise 8. Row Operations and Their Invertibility

**Given:**

$$A = \begin{pmatrix} 1 & 2 & -1 \\\\ 2 & 4 & 1 \\\\ -1 & 1 & 3 \end{pmatrix}$$

---

### 1. Perform the Row Operations in Order and State Each Resulting Matrix.

* **Method and Property Used:** Elementary row operations are controlled transformations of a matrix that preserve the solution set of a corresponding linear system and are **invertible**. Applying a sequence of row operations updates only the specified rows while leaving all other rows unchanged.

* **Step 1: $R_2 \leftarrow R_2 - 2R_1$**
  * *Main steps:* Multiply row $1$, $(1, 2, -1)$, by $2$ to get $(2, 4, -2)$, then subtract it entrywise from row $2$, $(2, 4, 1)$:

$$(2, 4, 1) - 2(1, 2, -1) = (2 - 2,\; 4 - 4,\; 1 - (-2)) = (0, 0, 3)$$

  * *Result:*

$$A^{(1)} = \begin{pmatrix} 1 & 2 & -1 \\\\ 0 & 0 & 3 \\\\ -1 & 1 & 3 \end{pmatrix}$$

  * *Verification:* Recomputing $(2, 4, 1) - (2, 4, -2)$ entrywise gives $(0, 0, 3)$, and rows $1$ and $3$ remain unchanged.

* **Step 2: $R_3 \leftarrow R_3 + R_1$**
  * *Main steps:* Add row $1$ of $A^{(1)}$, $(1, 2, -1)$, entrywise to row $3$, $(-1, 1, 3)$:

$$(-1, 1, 3) + (1, 2, -1) = (-1 + 1,\; 1 + 2,\; 3 + (-1)) = (0, 3, 2)$$

  * *Result:*

$$A^{(2)} = \begin{pmatrix} 1 & 2 & -1 \\\\ 0 & 0 & 3 \\\\ 0 & 3 & 2 \end{pmatrix}$$

  * *Verification:* Adding $(1, 2, -1)$ to $(-1, 1, 3)$ gives $(0, 3, 2)$, and rows $1$ and $2$ remain unchanged.

* **Step 3: Swap $R_2$ and $R_3$ ($R_2 \leftrightarrow R_3$)**
  * *Main steps:* Exchange the second row $(0, 0, 3)$ and the third row $(0, 3, 2)$ of $A^{(2)}$:

  * *Result:*

$$A^{(3)} = \begin{pmatrix} 1 & 2 & -1 \\\\ 0 & 3 & 2 \\\\ 0 & 0 & 3 \end{pmatrix}$$

  * *Verification:* Row $2$ of $A^{(3)}$ equals row $3$ of $A^{(2)}$, row $3$ of $A^{(3)}$ equals row $2$ of $A^{(2)}$, and row $1$ is unchanged.

---

### 2. Inverse (Undoing) Operation for Each of the Three Operations.

* **Method and Property Used:** Every elementary row operation has an **inverse row operation** that restores the previous matrix when applied immediately after it:
  * Adding a multiple of one row to another is undone by **subtracting the same multiple** of that row.
  * Swapping two rows is undone by **swapping the same two rows** again.

* **Inverse of Operation 1 ($R_2 \leftarrow R_2 - 2R_1$):**
  * *Inverse operation:* **$R_2 \leftarrow R_2 + 2R_1$** (add $2$ times row $1$ back to row $2$).
  * *Verification:* Applying $R_2 \leftarrow (0, 0, 3) + 2(1, 2, -1) = (2, 4, 1)$ restores the original row $2$ of $A$.

* **Inverse of Operation 2 ($R_3 \leftarrow R_3 + R_1$):**
  * *Inverse operation:* **$R_3 \leftarrow R_3 - R_1$** (subtract row $1$ from row $3$).
  * *Verification:* Applying $R_3 \leftarrow (0, 3, 2) - (1, 2, -1) = (-1, 1, 3)$ restores row $3$ from $A^{(1)}$.

* **Inverse of Operation 3 ($R_2 \leftrightarrow R_3$):**
  * *Inverse operation:* **$R_2 \leftrightarrow R_3$** (swap rows $2$ and $3$ again).
  * *Verification:* Swapping $(0, 3, 2)$ and $(0, 0, 3)$ back returns $A^{(2)}$.


