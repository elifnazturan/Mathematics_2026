# Exercise 15. Associativity of Multiplication and Different Ways to Compute

**Given:**

$$A = \begin{pmatrix} 1 & 2 & 0 \\\\ 0 & 1 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 0 \\\\ 2 & 1 \\\\ -1 & 3 \end{pmatrix}, \qquad C = \begin{pmatrix} 2 & 1 \\\\ 0 & -1 \end{pmatrix}$$

---

### 1. Compute $(AB)C$ and $A(BC)$.

* **Method and Property Used:** Matrix multiplication is **associative** whenever dimensions are compatible: $(AB)C = A(BC)$. Here $A$ is $2 \times 3$, $B$ is $3 \times 2$, and $C$ is $2 \times 2$, so both parenthesizations are well-defined and yield a $2 \times 2$ matrix.

* **Compute $(AB)C$:**
  * *Main steps:* First compute $AB$ ($2 \times 2$):

$$AB = \begin{pmatrix} 1 & 2 & 0 \\\\ 0 & 1 & 1 \end{pmatrix}\begin{pmatrix} 1 & 0 \\\\ 2 & 1 \\\\ -1 & 3 \end{pmatrix} = \begin{pmatrix} 1(1) + 2(2) + 0(-1) & 1(0) + 2(1) + 0(3) \\\\ 0(1) + 1(2) + 1(-1) & 0(0) + 1(1) + 1(3) \end{pmatrix} = \begin{pmatrix} 5 & 2 \\\\ 1 & 4 \end{pmatrix}$$

  * Next multiply $(AB)$ by $C$ ($2 \times 2$):

$$(AB)C = \begin{pmatrix} 5 & 2 \\\\ 1 & 4 \end{pmatrix}\begin{pmatrix} 2 & 1 \\\\ 0 & -1 \end{pmatrix} = \begin{pmatrix} 5(2) + 2(0) & 5(1) + 2(-1) \\\\ 1(2) + 4(0) & 1(1) + 4(-1) \end{pmatrix}$$

  * *Result:*

$$(AB)C = \begin{pmatrix} 10 & 3 \\\\ 2 & -3 \end{pmatrix}$$

  * *Verification:* Entry $(1, 2)$ of $(AB)C$ is $5(1) + 2(-1) = 3$, and entry $(2, 2)$ is $1(1) + 4(-1) = -3$, matching the full product.

* **Compute $A(BC)$:**
  * *Main steps:* First compute $BC$ ($3 \times 2$):

$$BC = \begin{pmatrix} 1 & 0 \\\\ 2 & 1 \\\\ -1 & 3 \end{pmatrix}\begin{pmatrix} 2 & 1 \\\\ 0 & -1 \end{pmatrix} = \begin{pmatrix} 1(2) + 0(0) & 1(1) + 0(-1) \\\\ 2(2) + 1(0) & 2(1) + 1(-1) \\\\ -1(2) + 3(0) & -1(1) + 3(-1) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\\\ 4 & 1 \\\\ -2 & -4 \end{pmatrix}$$

  * Next multiply $A$ ($2 \times 3$) by $(BC)$ ($3 \times 2$):

$$A(BC) = \begin{pmatrix} 1 & 2 & 0 \\\\ 0 & 1 & 1 \end{pmatrix}\begin{pmatrix} 2 & 1 \\\\ 4 & 1 \\\\ -2 & -4 \end{pmatrix} = \begin{pmatrix} 1(2) + 2(4) + 0(-2) & 1(1) + 2(1) + 0(-4) \\\\ 0(2) + 1(4) + 1(-2) & 0(1) + 1(1) + 1(-4) \end{pmatrix}$$

  * *Result:*

$$A(BC) = \begin{pmatrix} 10 & 3 \\\\ 2 & -3 \end{pmatrix}$$

  * *Verification:* Entry $(1, 1)$ is $1(2) + 2(4) + 0(-2) = 10$, and entry $(2, 1)$ is $0(2) + 1(4) + 1(-2) = 2$, matching every entry of $(AB)C$.

---

### 2. Compare Results and Intermediate Operations, and Explain Associativity Here.

* **Result:** Both grouping orders produce the **exact same matrix**:

$$(AB)C = A(BC) = \begin{pmatrix} 10 & 3 \\\\ 2 & -3 \end{pmatrix}$$

* **Comparison of Intermediate Operations:**
  * In **$(AB)C$**: $AB$ is a $2 \times 2$ product of a $2 \times 3$ and $3 \times 2$ matrix (each of the $4$ entries takes $3$ multiplications and $2$ additions $\implies 12$ multiplications, $8$ additions), and $(AB)C$ multiplies two $2 \times 2$ matrices (each of the $4$ entries takes $2$ multiplications and $1$ addition $\implies 8$ multiplications, $4$ additions). Total: **$20$ scalar multiplications** and **$12$ scalar additions**.
  * In **$A(BC)$**: $BC$ is a $3 \times 2$ product of a $3 \times 2$ and $2 \times 2$ matrix (each of the $6$ entries takes $2$ multiplications and $1$ addition $\implies 12$ multiplications, $6$ additions), and $A(BC)$ multiplies a $2 \times 3$ by a $3 \times 2$ matrix (each of the $4$ entries takes $3$ multiplications and $2$ additions $\implies 12$ multiplications, $8$ additions). Total: **$24$ scalar multiplications** and **$14$ scalar additions**.
  * Thus, **$(AB)C$ uses fewer intermediate scalar operations** ($20$ multiplications vs. $24$, and $12$ additions vs. $14$) for the same final matrix.

* **Explanation and Method Used:** Associativity in this example means that **re-parenthesizing the product does not change the result**, even though changing how factors are grouped changes the intermediate matrices formed along the way and the computational cost (number of scalar operations) required to reach the answer.

* **Verification:** Every entry of $\begin{pmatrix} 10 & 3 \\\\ 2 & -3 \end{pmatrix}$ agrees across both paths, and counting scalar multiplications/additions per dot product confirms $4 \times 3 + 4 \times 2 = 20$ multiplications for $(AB)C$ versus $6 \times 2 + 4 \times 3 = 24$ multiplications for $A(BC)$.


