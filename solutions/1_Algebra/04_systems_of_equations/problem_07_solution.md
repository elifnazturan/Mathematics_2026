# Exercise 7. Choosing a Method Deliberately

## Question

We consider three situations involving linear systems and must choose an appropriate solution method for each based on its structure and the number of right-hand sides, without solving every system completely:

1. One system with an upper-triangular coefficient matrix:

$$
\begin{cases}
2x - y = 3, \\
4y = 8.
\end{cases}
$$

2. Three systems $Ax = b_i$ ($i = 1, 2, 3$) sharing the same invertible coefficient matrix $A$, where $A^{-1}$ is already known.
3. One $3 \times 3$ linear system for which $A^{-1}$ is not given and the goal is only to find one solution vector.

We need to:
- Select the method that best fits each situation and justify the choice using matrix structure and the number of right-hand sides.
- For situation 1, carry out the chosen method completely.
- For situations 2 and 3, describe the plan and state which computations are reusable or unnecessary.

## Solution

### 1. System with a Triangular Coefficient Matrix

**Chosen method and justification:** Back substitution directly on the upper-triangular system. The coefficient matrix is already upper-triangular and there is only one right-hand side vector, so row elimination is unnecessary.

**Complete solution:** From the second equation, divide by $4$:

$$
4y = 8 \implies y = 2
$$

Substitute $y = 2$ into the first equation:

$$
2x - 2 = 3 \implies 2x = 5 \implies x = \frac{5}{2}
$$

The unique solution is $(x, y) = \left(\frac{5}{2}, 2\right)$.

### 2. Three Systems $Ax = b_i$ with Known $A^{-1}$

**Chosen method and justification:** Direct matrix-vector multiplication $x_i = A^{-1}b_i$ for each of the three right-hand sides. Because $A^{-1}$ is already known and there are multiple right-hand sides sharing the same matrix $A$, computing $A^{-1}$ via row reduction or inversion is unnecessary, and repeating elimination from scratch for each $b_i$ would duplicate work.

**Plan and reusable/unnecessary parts:**
- **Reusable:** The inverse matrix $A^{-1}$ is computed once and reused across all three right-hand sides $b_1, b_2, b_3$.
- **Unnecessary:** Performing Gaussian elimination on three separate augmented matrices $(A \mid b_1)$, $(A \mid b_2)$, and $(A \mid b_3)$ or inverting $A$ again.
- **Execution plan:** Compute $x_1 = A^{-1}b_1$, $x_2 = A^{-1}b_2$, and $x_3 = A^{-1}b_3$.

### 3. Single $3 \times 3$ System Without $A^{-1}$ for One Solution Vector

**Chosen method and justification:** Gaussian elimination on the augmented matrix $(A \mid b)$ followed by back substitution. There is only one right-hand side vector, $A^{-1}$ is not provided, and only one solution vector is needed.

**Plan and reusable/unnecessary parts:**
- **Reusable:** The row-echelon reduction steps transform $(A \mid b)$ into an upper-triangular system in a single forward pass.
- **Unnecessary:** Computing $A^{-1}$ or Gauss-Jordan reduction to full reduced row-echelon form / identity matrix, since a single right-hand side only requires one back-substitution pass rather than a general inverse operator.
- **Execution plan:** Form $(A \mid b)$, apply forward elimination to obtain an upper-triangular system, and solve for the unknowns via back substitution.
