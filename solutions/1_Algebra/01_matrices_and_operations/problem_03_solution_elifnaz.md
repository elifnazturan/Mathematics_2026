# Exercise 3. When Can Matrices Be Multiplied?

**Given:**

$$A_{2\times 3}, \qquad B_{3\times 4}, \qquad C_{4\times 2}, \qquad D_{2\times 2}$$

---

### Method and Dimension Compatibility Rule

* **Method / Property Used:** A matrix product $X_{m\times n} Y_{p\times q}$ is **defined** if and only if the number of columns of the first matrix equals the number of rows of the second matrix ($n = p$, i.e., **inner dimensions match**). When defined, the resulting product matrix has size $m \times q$ (determined by the **outer dimensions**). If $n \neq p$, the product is **undefined** because the row lengths of $X$ do not match the column lengths of $Y$ for dot products.

---

### Evaluation of Each Product

* **$AB$:**
  * *Main steps:* Compare inner dimensions of $A_{2\times 3}$ and $B_{3\times 4}$: $3 = 3$; take outer dimensions $2$ and $4$.
  * *Result:* **Defined**, size is **$2 \times 4$**.
  * *Verification:* Each row of $A$ has $3$ entries and each column of $B$ has $3$ entries, so every entry $(i, j)$ in a $2 \times 4$ matrix is well-defined.

* **$BA$:**
  * *Main steps:* Compare inner dimensions of $B_{3\times 4}$ and $A_{2\times 3}$: $4 \neq 2$.
  * *Result:* **Undefined**.
  * *Verification:* Each row of $B$ has $4$ entries while each column of $A$ has only $2$ entries, so entrywise pairing for multiplication is impossible.

* **$BC$:**
  * *Main steps:* Compare inner dimensions of $B_{3\times 4}$ and $C_{4\times 2}$: $4 = 4$; take outer dimensions $3$ and $2$.
  * *Result:* **Defined**, size is **$3 \times 2$**.
  * *Verification:* Each row of $B$ has $4$ entries and each column of $C$ has $4$ entries, yielding a $3 \times 2$ product matrix.

* **$CB$:**
  * *Main steps:* Compare inner dimensions of $C_{4\times 2}$ and $B_{3\times 4}$: $2 \neq 3$.
  * *Result:* **Undefined**.
  * *Verification:* Each row of $C$ has $2$ entries whereas each column of $B$ has $3$ entries, failing the inner-dimension match.

* **$AC$:**
  * *Main steps:* Compare inner dimensions of $A_{2\times 3}$ and $C_{4\times 2}$: $3 \neq 4$.
  * *Result:* **Undefined**.
  * *Verification:* Each row of $A$ has $3$ entries while each column of $C$ has $4$ entries, so no product is defined.

* **$CA$:**
  * *Main steps:* Compare inner dimensions of $C_{4\times 2}$ and $A_{2\times 3}$: $2 = 2$; take outer dimensions $4$ and $3$.
  * *Result:* **Defined**, size is **$4 \times 3$**.
  * *Verification:* Each row of $C$ has $2$ entries and each column of $A$ has $2$ entries, producing a $4 \times 3$ result.

* **$AD$:**
  * *Main steps:* Compare inner dimensions of $A_{2\times 3}$ and $D_{2\times 2}$: $3 \neq 2$.
  * *Result:* **Undefined**.
  * *Verification:* Each row of $A$ has $3$ entries while each column of $D$ has $2$ entries, so inner dimensions do not match.

* **$DA$:**
  * *Main steps:* Compare inner dimensions of $D_{2\times 2}$ and $A_{2\times 3}$: $2 = 2$; take outer dimensions $2$ and $3$.
  * *Result:* **Defined**, size is **$2 \times 3$**.
  * *Verification:* Each row of $D$ has $2$ entries and each column of $A$ has $2$ entries, yielding a $2 \times 3$ product matrix.

