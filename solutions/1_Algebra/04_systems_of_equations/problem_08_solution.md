# Exercise 8. Two Systems with the Same Coefficient Matrix

## Question

We are given two linear systems in two unknowns $(x, y)$ sharing the same coefficient matrix:

**System 1**

$$
\begin{cases}
2x + y = 5, \\
x - y = 1.
\end{cases}
$$

**System 2**

$$
\begin{cases}
2x + y = 1, \\
x - y = 4.
\end{cases}
$$

We need to:
1. Solve both systems by elimination.
2. Compare the successive elimination steps.
3. State which part of the calculation is the same in both cases and explain why.

## Solution

### 1. Solving System 1 by Elimination

Add the first and second equations to eliminate $y$:

$$
(2x + y) + (x - y) = 5 + 1 \implies 3x = 6 \implies x = 2
$$

Substitute $x = 2$ into the second equation $x - y = 1$:

$$
2 - y = 1 \implies y = 1
$$

The solution to System 1 is $(x, y) = (2, 1)$.

### 2. Solving System 2 by Elimination

Add the first and second equations to eliminate $y$:

$$
(2x + y) + (x - y) = 1 + 4 \implies 3x = 5 \implies x = \frac{5}{3}
$$

Substitute $x = \frac{5}{3}$ into the second equation $x - y = 4$:

$$
\frac{5}{3} - y = 4 \implies y = \frac{5}{3} - 4 = -\frac{7}{3}
$$

The solution to System 2 is $(x, y) = \left(\frac{5}{3}, -\frac{7}{3}\right)$.

### 3. Comparison and Shared Calculation

Both systems have the same coefficient matrix

$$
A =
\begin{pmatrix}
2 & 1 \\
1 & -1 \\
\end{pmatrix}
$$

and differ only in the right-hand side vector.

- **Comparison of elimination steps:** In both systems, adding row 1 to row 2 cancels $+y$ and $-y$ immediately, leaving the same left-hand side $3x$ and the same back-substitution relation $y = x - b_2$. Only the right-hand side numerical values change ($6$ vs. $5$, and then $2 - 1 = 1$ vs. $\frac{5}{3} - 4 = -\frac{7}{3}$).
- **What is the same and why:** The left-hand side combinations and elimination multipliers (here, adding row 1 and row 2) are identical because row operations on the left-hand side depend solely on the coefficient matrix $A$, not on the right-hand side vector $b$.
