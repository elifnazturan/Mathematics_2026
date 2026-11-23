# Exercise 10. Columns of a Matrix Product

**Given:**

$$A = \begin{pmatrix} 1 & 2 & 0 \\\\ 0 & 1 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 2 \\\\ -1 & 0 \\\\ 3 & 1 \end{pmatrix} = \begin{pmatrix} b_1 & b_2 \end{pmatrix}$$

where the columns of $B$ are:

$$b_1 = \begin{pmatrix} 1 \\\\ -1 \\\\ 3 \end{pmatrix}, \qquad b_2 = \begin{pmatrix} 2 \\\\ 0 \\\\ 1 \end{pmatrix}$$

---

### 1. Compute $Ab_1$ and $Ab_2$.

* **Method and Property Used:** Since $A$ is $2 \times 3$ and each column vector $b_1, b_2$ is $3 \times 1$, the inner dimensions match ($3 = 3$), so both matrix-vector products are defined and produce $2 \times 1$ column vectors via row-by-column dot products.

* **Compute $Ab_1$:**
  * *Main steps:* Dot each row of $A$ with $b_1 = \begin{pmatrix} 1 \\\\ -1 \\\\ 3 \end{pmatrix}$:

$$Ab_1 = \begin{pmatrix} 1 & 2 & 0 \\\\ 0 & 1 & 1 \end{pmatrix}\begin{pmatrix} 1 \\\\ -1 \\\\ 3 \end{pmatrix} = \begin{pmatrix} 1(1) + 2(-1) + 0(3) \\\\ 0(1) + 1(-1) + 1(3) \end{pmatrix} = \begin{pmatrix} 1 - 2 + 0 \\\\ 0 - 1 + 3 \end{pmatrix}$$

  * *Result:*

$$Ab_1 = \begin{pmatrix} -1 \\\\ 2 \end{pmatrix}$$

  * *Verification:* Row $1$ gives $1 - 2 + 0 = -1$ and row $2$ gives $0 - 1 + 3 = 2$, matching $\begin{pmatrix} -1 \\\\ 2 \end{pmatrix}$.

* **Compute $Ab_2$:**
  * *Main steps:* Dot each row of $A$ with $b_2 = \begin{pmatrix} 2 \\\\ 0 \\\\ 1 \end{pmatrix}$:

$$Ab_2 = \begin{pmatrix} 1 & 2 & 0 \\\\ 0 & 1 & 1 \end{pmatrix}\begin{pmatrix} 2 \\\\ 0 \\\\ 1 \end{pmatrix} = \begin{pmatrix} 1(2) + 2(0) + 0(1) \\\\ 0(2) + 1(0) + 1(1) \end{pmatrix} = \begin{pmatrix} 2 + 0 + 0 \\\\ 0 + 0 + 1 \end{pmatrix}$$

  * *Result:*

$$Ab_2 = \begin{pmatrix} 2 \\\\ 1 \end{pmatrix}$$

  * *Verification:* Row $1$ gives $2 + 0 + 0 = 2$ and row $2$ gives $0 + 0 + 1 = 1$, matching $\begin{pmatrix} 2 \\\\ 1 \end{pmatrix}$.

---

### 2. Compute the Matrix $AB$.

* **Method and Property Used:** Since $A$ is $2 \times 3$ and $B$ is $3 \times 2$, $AB$ is defined and has size $2 \times 2$, with entry $(i, j)$ equal to the dot product of row $i$ of $A$ with column $j$ of $B$.
* **Main steps:**

$$AB = \begin{pmatrix} 1 & 2 & 0 \\\\ 0 & 1 & 1 \end{pmatrix}\begin{pmatrix} 1 & 2 \\\\ -1 & 0 \\\\ 3 & 1 \end{pmatrix} = \begin{pmatrix} 1(1) + 2(-1) + 0(3) & 1(2) + 2(0) + 0(1) \\\\ 0(1) + 1(-1) + 1(3) & 0(2) + 1(0) + 1(1) \end{pmatrix}$$

* **Result:**

$$AB = \begin{pmatrix} -1 & 2 \\\\ 2 & 1 \end{pmatrix}$$

* **Verification:** Entry $(1, 1)$ is $-1$, entry $(1, 2)$ is $2$, entry $(2, 1)$ is $2$, and entry $(2, 2)$ is $1$, matching the full $2 \times 2$ product.

---

### 3. Compare the Results and Explain Why $Ab_1$ and $Ab_2$ Are the Columns of $AB$.

* **Result:** The first column of $AB$ equals $Ab_1 = \begin{pmatrix} -1 \\\\ 2 \end{pmatrix}$ and the second column of $AB$ equals $Ab_2 = \begin{pmatrix} 2 \\\\ 1 \end{pmatrix}$, so:

$$AB = \begin{pmatrix} Ab_1 & Ab_2 \end{pmatrix}$$

* **Explanation and Method Used:** By definition of matrix multiplication, column $j$ of the product $AB$ is formed by taking dot products of the rows of $A$ with column $j$ of $B$ ($b_j$). Computing the dot products of the rows of $A$ with $b_j$ is **identical** to multiplying the matrix $A$ by the single column vector $b_j$. Therefore, a matrix product $AB$ can be viewed **column by column** as applying $A$ separately to each column of $B$:

$$AB = A\begin{pmatrix} b_1 & b_2 \end{pmatrix} = \begin{pmatrix} Ab_1 & Ab_2 \end{pmatrix}$$

* **Verification:** Comparing column $1$ of $AB$, $\begin{pmatrix} -1 \\\\ 2 \end{pmatrix}$, with $Ab_1 = \begin{pmatrix} -1 \\\\ 2 \end{pmatrix}$ shows they are identical, and comparing column $2$ of $AB$, $\begin{pmatrix} 2 \\\\ 1 \end{pmatrix}$, with $Ab_2 = \begin{pmatrix} 2 \\\\ 1 \end{pmatrix}$ confirms the same equality.

---

> **Purpose of this exercise:** to generalize matrix-vector multiplication to full matrix multiplication by viewing the columns of $AB$ as $A$ acting on each column of $B$.
