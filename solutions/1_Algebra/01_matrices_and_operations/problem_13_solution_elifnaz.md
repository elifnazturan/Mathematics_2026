# Exercise 13. A Recurrence Written in Matrix Form

**Given:**

$$F = \begin{pmatrix} 1 & 1 \\\\ 1 & 0 \end{pmatrix}$$

and the Fibonacci sequence:

$$0,\; 1,\; 1,\; 2,\; 3,\; 5,\; 8,\; \dots$$

---

### 1. Compute $F^2$, $F^3$, $F^4$, and $F^5$, and Compare the Numbers With the Sequence.

* **Method and Property Used:** Positive integer powers of $F$ are computed via repeated matrix multiplication ($F^k = F^{k-1}F$). Because each multiplication adds two consecutive terms and shifts the previous term down, consecutive Fibonacci numbers appear directly inside the entries of $F^n$.

* **Compute $F^2$, $F^3$, $F^4$, and $F^5$:**
  * *Main steps:* Multiply step by step using row-by-column dot products:

$$F^2 = \begin{pmatrix} 1 & 1 \\\\ 1 & 0 \end{pmatrix}\begin{pmatrix} 1 & 1 \\\\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 1(1) + 1(1) & 1(1) + 1(0) \\\\ 1(1) + 0(1) & 1(1) + 0(0) \end{pmatrix}$$

$$F^3 = F^2 F = \begin{pmatrix} 2 & 1 \\\\ 1 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\\\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 2(1) + 1(1) & 2(1) + 1(0) \\\\ 1(1) + 1(1) & 1(1) + 1(0) \end{pmatrix}$$

$$F^4 = F^3 F = \begin{pmatrix} 3 & 2 \\\\ 2 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\\\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 3(1) + 2(1) & 3(1) + 2(0) \\\\ 2(1) + 1(1) & 2(1) + 1(0) \end{pmatrix}$$

$$F^5 = F^4 F = \begin{pmatrix} 5 & 3 \\\\ 3 & 2 \end{pmatrix}\begin{pmatrix} 1 & 1 \\\\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 5(1) + 3(1) & 5(1) + 3(0) \\\\ 3(1) + 2(1) & 3(1) + 2(0) \end{pmatrix}$$

  * *Result:*

$$F^2 = \begin{pmatrix} 2 & 1 \\\\ 1 & 1 \end{pmatrix}, \qquad F^3 = \begin{pmatrix} 3 & 2 \\\\ 2 & 1 \end{pmatrix}, \qquad F^4 = \begin{pmatrix} 5 & 3 \\\\ 3 & 2 \end{pmatrix}, \qquad F^5 = \begin{pmatrix} 8 & 5 \\\\ 5 & 3 \end{pmatrix}$$

* **Comparison With the Sequence ($0, 1, 1, 2, 3, 5, 8, \dots$):**
  * The numbers appearing in $F^2, F^3, F^4, F^5$ are $1, 2, 3, 5, 8$, which are exact terms of the Fibonacci sequence ($F_1 = 1, F_2 = 1, F_3 = 2, F_4 = 3, F_5 = 5, F_6 = 8, \dots$).
  * Specifically, for $n \ge 1$, the powers follow the structure:

$$F^n = \begin{pmatrix} F_{n+1} & F_n \\\\ F_n & F_{n-1} \end{pmatrix} \qquad (\text{with } F_0 = 0,\; F_1 = 1)$$

* **Verification:** For $n = 2$, $\begin{pmatrix} F_3 & F_2 \\\\ F_2 & F_1 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\\\ 1 & 1 \end{pmatrix}$; for $n = 5$, $\begin{pmatrix} F_6 & F_5 \\\\ F_5 & F_4 \end{pmatrix} = \begin{pmatrix} 8 & 5 \\\\ 5 & 3 \end{pmatrix}$, matching every computed matrix.

---

### 2. Compute $F\begin{pmatrix} a \\ b \end{pmatrix}$ and Explain How It Performs a Recurrence Step.

* **Method and Property Used:** Multiplying the $2 \times 2$ matrix $F$ by a $2 \times 1$ column vector $\begin{pmatrix} a \\ b \end{pmatrix}$ computes two dot products: the first row dots with $\begin{pmatrix} a \\ b \end{pmatrix}$ to form the sum $a + b$, and the second row dots with $\begin{pmatrix} a \\ b \end{pmatrix}$ to keep $a$.

* **Main steps:**

$$F\begin{pmatrix} a \\\\ b \end{pmatrix} = \begin{pmatrix} 1 & 1 \\\\ 1 & 0 \end{pmatrix}\begin{pmatrix} a \\\\ b \end{pmatrix} = \begin{pmatrix} 1(a) + 1(b) \\\\ 1(a) + 0(b) \end{pmatrix}$$

* **Result:**

$$F\begin{pmatrix} a \\\\ b \end{pmatrix} = \begin{pmatrix} a + b \\\\ a \end{pmatrix}$$

* **Explanation of the Recurrence Step:**
  * If $a$ and $b$ represent two consecutive terms of a recurrence sequence (for example, $a = F_k$ and $b = F_{k-1}$), the top entry $a + b$ forms the **sum of two consecutive terms** ($F_{k+1} = F_k + F_{k-1}$), while the bottom entry **retains one of those terms** ($a = F_k$) to be used in the next step.
  * Repeating this multiplication advances the state vector by one index step:

$$F\begin{pmatrix} F_k \\\\ F_{k-1} \end{pmatrix} = \begin{pmatrix} F_{k+1} \\\\ F_k \end{pmatrix}$$

* **Verification:** Taking $a = 1$ and $b = 1$ gives $F\begin{pmatrix} 1 \\\\ 1 \end{pmatrix} = \begin{pmatrix} 2 \\\\ 1 \end{pmatrix}$; applying $F$ once more gives $F\begin{pmatrix} 2 \\\\ 1 \end{pmatrix} = \begin{pmatrix} 3 \\\\ 2 \end{pmatrix}$, generating the next Fibonacci numbers step by step.

---

> **Purpose of this exercise:** to connect matrix powers with a simple numerical recurrence relation and see how a single matrix-vector multiplication advances a two-term recurrence by one step.
