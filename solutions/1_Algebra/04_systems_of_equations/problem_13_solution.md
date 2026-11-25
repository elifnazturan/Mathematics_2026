# Exercise 13. Does Every Equation Add New Information?

## Question

We are given the linear system of three equations in three unknowns $(x_1, x_2, x_3)$:

$$
\begin{cases}
x_1 + x_2 = 10, \\
x_2 + x_3 = 8, \\
x_1 - x_3 = 2.
\end{cases}
$$

We need to:
1. Solve the system and describe its solution set.
2. Check whether all three equations are independently necessary to describe the solution set.
3. If one equation follows from the others, show this explicitly by calculation.

## Solution

### 1. Solving the System

Let $x_3 = t$, where $t \in \mathbb{R}$ is a real parameter. From the second equation $x_2 + x_3 = 8$:

$$
x_2 = 8 - t
$$

Substitute $x_3 = t$ into the third equation $x_1 - x_3 = 2$:

$$
x_1 = 2 + t
$$

Check the first equation $x_1 + x_2 = 10$ with these expressions:

$$
(2 + t) + (8 - t) = 10
$$

The first equation holds identically for every $t \in \mathbb{R}$. Thus, the system has infinitely many solutions, given in parametric form by

$$
\begin{cases}
x_1 = 2 + t, \\
x_2 = 8 - t, \\
x_3 = t, \quad t \in \mathbb{R}.
\end{cases}
$$

### 2. Redundancy and Independence of the Equations

Not all three equations add independent information to the solution set: the third equation is redundant because it can be obtained by combining the first two equations.

### 3. Explicit Calculation Showing One Equation Follows from the Others

Subtract the second equation $(x_2 + x_3 = 8)$ from the first equation $(x_1 + x_2 = 10)$:

$$
(x_1 + x_2) - (x_2 + x_3) = 10 - 8
$$

Simplifying both sides gives:

$$
x_1 - x_3 = 2
$$

This is exactly the third equation. Therefore, any pair $(x_1, x_2, x_3)$ that satisfies the first two equations automatically satisfies the third equation, so the first two equations alone completely determine the solution set.
