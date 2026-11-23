# Exercise 2. Addition and Scalar Multiplication

**Given:**

$$A = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix}, \qquad B = \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}$$

---

### 1. Compute $A + B$, $A - B$, and $3A - 2B$.

* **Method & Properties Used:** Matrix addition, subtraction, and scalar multiplication are performed **entry-by-entry** (elementwise) on matrices of identical dimensions ($2 \times 2$). Scalar multiplication scales each entry by the scalar factor, and subtraction can be viewed as adding the additive inverse ($A - B = A + (-1)B$).

* **$A + B$:**
  * *Main steps:* Add corresponding entries at each position $(i, j)$:
    $$A + B = \begin{pmatrix} 1 + 4 & 2 + (-2) \\ -1 + 0 & 3 + 5 \end{pmatrix}$$
  * *Result:*
    $$A + B = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}$$
  * *Verification:* By commutativity of addition ($A + B = B + A$), adding $B$ to $A$ gives $\begin{pmatrix} 4+1 & -2+2 \\ 0+(-1) & 5+3 \end{pmatrix} = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}$, which matches.

* **$A - B$:**
  * *Main steps:* Subtract each entry of $B$ from the corresponding entry of $A$:
    $$A - B = \begin{pmatrix} 1 - 4 & 2 - (-2) \\ -1 - 0 & 3 - 5 \end{pmatrix}$$
  * *Result:*
    $$A - B = \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}$$
  * *Verification:* Adding the result back to $B$ recovers $A$: $(A - B) + B = \begin{pmatrix} -3 + 4 & 4 + (-2) \\ -1 + 0 & -2 + 5 \end{pmatrix} = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} = A$.

* **$3A - 2B$:**
  * *Main steps:* First apply scalar multiplication ($3A$ and $2B$), then subtract entrywise:
    $$3A - 2B = 3\begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} - 2\begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix} - \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}$$
  * *Result:*
    $$3A - 2B = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}$$
  * *Verification:* Checking entry $(1, 2)$ directly: $3(2) - 2(-2) = 6 + 4 = 10$; checking entry $(2, 1)$ directly: $3(-1) - 2(0) = -3$, matching the resulting $2 \times 2$ matrix.

---

### 2. Explain why addition of matrices is only possible for matrices of the same size.

* **Explanation & Method Used:** Matrix addition is defined **entry-by-entry** (elementwise), meaning the entry in row $i$ and column $j$ of the sum is obtained by adding entry $(i, j)$ of the first matrix to entry $(i, j)$ of the second matrix.
* **Dimension Requirement & Verification:** For every entry $(i, j)$ to have a corresponding partner, both matrices must have the **same number of rows and the same number of columns** (compatible dimensions). If one matrix has a row or column that the other lacks, some entries have no matching position, so the entrywise sum is undefined. For $2 \times 2$ matrices $A$ and $B$, every position $(i, j) \in \{1, 2\} \times \{1, 2\}$ exists in both, so $A + B$ is well-defined and also $2 \times 2$.

---

> **Purpose of this exercise:** to reinforce entrywise operations, scalar multiplication, verification of results, and the requirement of matching matrix dimensions.
