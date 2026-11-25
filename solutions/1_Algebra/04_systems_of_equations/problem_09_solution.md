# Exercise 9. A System from a Sum Condition

## Question

We are given two linear conditions in two unknowns $x$ and $y$:

$$
\begin{cases}
x + y = 10, \\
2x + 5y = 32.
\end{cases}
$$

We need to:
1. Solve the system for $x$ and $y$.
2. Explain geometrically why the solution is unique.

## Solution

### 1. Solving the System

From the first equation, express $x$ in terms of $y$:

$$
x = 10 - y
$$

Substitute $x = 10 - y$ into the second equation:

$$
2(10 - y) + 5y = 32 \implies 20 - 2y + 5y = 32 \implies 3y = 12 \implies y = 4
$$

Substitute $y = 4$ back into $x = 10 - y$:

$$
x = 10 - 4 = 6
$$

Thus, the unique solution is $(x, y) = (6, 4)$.

### 2. Geometric Interpretation

Each linear equation in two unknowns represents a straight line in the Cartesian plane $\mathbb{R}^2$:

- The first equation $x + y = 10$ can be rewritten as $y = -x + 10$, which is a line with slope $m_1 = -1$.
- The second equation $2x + 5y = 32$ can be rewritten as $y = -\frac{2}{5}x + \frac{32}{5}$, which is a line with slope $m_2 = -\frac{2}{5}$.

Because $m_1 = -1 \neq -\frac{2}{5} = m_2$, the two lines are not parallel and have different directions. Two non-parallel lines in $\mathbb{R}^2$ intersect at exactly one point, which corresponds geometrically to the unique solution $(6, 4)$.
