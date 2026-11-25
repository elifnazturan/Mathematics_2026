# Exercise 6. A System with a Parameter - Which Cases Actually Occur?

## Question

We are given the linear system in two unknowns $(x, y)$ depending on the real parameter $a$:

$$
\begin{cases}
x + y = 2, \\
ax + ay = 4.
\end{cases}
$$

We need to:
1. Analyze the system depending on the parameter $a$.
2. Among the three possibilities — **exactly one solution**, **infinitely many solutions**, and **no solution** — determine which cases actually occur and for which values of $a$.
3. If any case cannot occur, explain why.

## Solution

### 1. Elimination and Case Analysis

Write the augmented matrix for the system:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
a & a & \mid & 4 \\
\end{pmatrix}
$$

Eliminate $x$ from the second row by applying $R_2 \leftarrow R_2 - aR_1$:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 4 - 2a \\
\end{pmatrix}
$$

The second row corresponds to the equation

$$
0x + 0y = 4 - 2a
$$

We examine the possible values of $a \in \mathbb{R}$:

- **Case $a = 2$:** The second row becomes $(0 \; 0 \mid 0)$, which gives $0 = 0$. The system reduces to the single equation $x + y = 2$, so setting $y = t$ ($t \in \mathbb{R}$) gives $x = 2 - t$. Thus, for $a = 2$, there are **infinitely many solutions**.
- **Case $a \neq 2$:** Here $4 - 2a \neq 0$, so the second row gives $0 = 4 - 2a$, which is a contradiction. Thus, for every $a \neq 2$, there is **no solution** (the system is inconsistent).

### 2. Which Cases Actually Occur and Why One Case Is Impossible

- **Infinitely many solutions:** Occurs for $a = 2$.
- **No solution:** Occurs for all $a \in \mathbb{R}$ with $a \neq 2$.
- **Exactly one solution:** **Never occurs** for any value of $a$.

**Why a unique solution cannot occur:** Notice that the second equation is $a(x + y) = 4$. Since the first equation fixes $x + y = 2$, substituting this into the second equation forces $2a = 4$, i.e., $a = 2$. Because the coefficient vector $(a, a)$ of the second equation is always a scalar multiple $a$ of the first equation's coefficient vector $(1, 1)$, the rank of the coefficient matrix is at most $1$ (whereas there are $2$ unknowns). A linear system with fewer pivots than unknowns can never have a unique solution.
