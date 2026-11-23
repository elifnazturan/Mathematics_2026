# Exercise 7. Identity Matrix, Zero Matrix, and Powers

**Given:**

$$A = \begin{pmatrix} 2 & 1 \\\\ 0 & 2 \end{pmatrix}, \qquad I = \begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix}, \qquad O = \begin{pmatrix} 0 & 0 \\\\ 0 & 0 \end{pmatrix}$$

---

### 1. Compute $AI$, $IA$, $A + O$, $A^2$, and $A^3$.

* **Method and Property Used:** For $2 \times 2$ square matrices, multiplication and addition are defined. Multiplying by the identity matrix $I$ leaves any compatible matrix unchanged ($AI = IA = A$), adding the zero matrix $O$ leaves any matrix of the same size unchanged ($A + O = A$), and positive integer powers of $A$ are computed via repeated matrix multiplication ($A^2 = AA$, $A^3 = A^2 A$).

* **Compute $AI$ and $IA$:**
  * *Main steps:* Multiply rows of the first matrix by columns of the second matrix:

$$AI = \begin{pmatrix} 2 & 1 \\\\ 0 & 2 \end{pmatrix}\begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 2(1) + 1(0) & 2(0) + 1(1) \\\\ 0(1) + 2(0) & 0(0) + 2(1) \end{pmatrix}$$

$$IA = \begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix}\begin{pmatrix} 2 & 1 \\\\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 1(2) + 0(0) & 1(1) + 0(2) \\\\ 0(2) + 1(0) & 0(1) + 1(2) \end{pmatrix}$$

  * *Result:*

$$AI = \begin{pmatrix} 2 & 1 \\\\ 0 & 2 \end{pmatrix}, \qquad IA = \begin{pmatrix} 2 & 1 \\\\ 0 & 2 \end{pmatrix}$$

  * *Verification:* Both products equal $A$ entrywise, confirming the multiplicative identity property $AI = IA = A$ on this example.

* **Compute $A + O$:**
  * *Main steps:* Add corresponding entries of $A$ and the $2 \times 2$ zero matrix $O$:

$$A + O = \begin{pmatrix} 2 + 0 & 1 + 0 \\\\ 0 + 0 & 2 + 0 \end{pmatrix}$$

  * *Result:*

$$A + O = \begin{pmatrix} 2 & 1 \\\\ 0 & 2 \end{pmatrix}$$

  * *Verification:* Adding $0$ to each entry leaves every entry of $A$ unchanged, confirming $A + O = A$.

* **Compute $A^2$:**
  * *Main steps:* Compute $A^2 = AA$ using row-by-column dot products:

$$A^2 = \begin{pmatrix} 2 & 1 \\\\ 0 & 2 \end{pmatrix}\begin{pmatrix} 2 & 1 \\\\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 2(2) + 1(0) & 2(1) + 1(2) \\\\ 0(2) + 2(0) & 0(1) + 2(2) \end{pmatrix}$$

  * *Result:*

$$A^2 = \begin{pmatrix} 4 & 4 \\\\ 0 & 4 \end{pmatrix}$$

  * *Verification:* Entry $(1, 2)$ is $2(1) + 1(2) = 4$, and both diagonal entries are $2^2 = 4$, matching the product.

* **Compute $A^3$:**
  * *Main steps:* Multiply $A^2$ by $A$ ($A^3 = A^2 A$):

$$A^3 = \begin{pmatrix} 4 & 4 \\\\ 0 & 4 \end{pmatrix}\begin{pmatrix} 2 & 1 \\\\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 4(2) + 4(0) & 4(1) + 4(2) \\\\ 0(2) + 4(0) & 0(1) + 4(2) \end{pmatrix}$$

  * *Result:*

$$A^3 = \begin{pmatrix} 8 & 12 \\\\ 0 & 8 \end{pmatrix}$$

  * *Verification:* Entry $(1, 2)$ is $4(1) + 4(2) = 12$, and both diagonal entries are $2^3 = 8$, matching $A^2 A$.

---

### 2. Roles of $I$ and $O$, and Pattern in Successive Powers of $A$.

* **Roles of $I$ and $O$:**
  * The **identity matrix $I$** acts as the **multiplicative identity** (neutral element for matrix multiplication): multiplying $A$ by $I$ on either side leaves $A$ unchanged ($AI = IA = A$), analogous to multiplying a number by $1$.
  * The **zero matrix $O$** acts as the **additive identity** (neutral element for matrix addition): adding $O$ leaves $A$ unchanged ($A + O = A$), analogous to adding $0$ to a number.
* **Pattern in Successive Powers of $A$:**
  * Looking at $A^1 = \begin{pmatrix} 2 & 1 \\\\ 0 & 2 \end{pmatrix}$, $A^2 = \begin{pmatrix} 4 & 4 \\\\ 0 & 4 \end{pmatrix}$, and $A^3 = \begin{pmatrix} 8 & 12 \\\\ 0 & 8 \end{pmatrix}$, every power remains **upper triangular** with diagonal entries equal to **$2^k$**.
  * The upper-right entry follows the pattern $1 \cdot 2^0 = 1$, $2 \cdot 2^1 = 4$, $3 \cdot 2^2 = 12$, giving the general formula:

$$A^k = \begin{pmatrix} 2^k & k \cdot 2^{k-1} \\\\ 0 & 2^k \end{pmatrix} \qquad (k \ge 1)$$

* **Verification:** Substituting $k = 1$, $k = 2$, and $k = 3$ into the formula gives $\begin{pmatrix} 2 & 1 \\\\ 0 & 2 \end{pmatrix}$, $\begin{pmatrix} 4 & 4 \\\\ 0 & 4 \end{pmatrix}$, and $\begin{pmatrix} 8 & 12 \\\\ 0 & 8 \end{pmatrix}$, matching all computed powers.

