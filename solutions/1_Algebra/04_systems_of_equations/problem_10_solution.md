# Exercise 10. A Polynomial Through Three Points

## Question

We want to find a quadratic polynomial

$$
p(x) = ax^2 + bx + c
$$

whose graph passes through the three points $(0, 1)$, $(1, 3)$, and $(2, 9)$.

We need to:
1. Reduce the problem to a linear system of equations in the unknowns $a$, $b$, and $c$.
2. Solve the system to find $p(x)$.
3. Check the result by substituting all three points into $p(x)$.

## Solution

### 1. Reduction to a Linear System

Substitute each given point $(x, p(x))$ into $p(x) = ax^2 + bx + c$:

- For $(0, 1)$: $a(0)^2 + b(0) + c = 1 \implies c = 1$.
- For $(1, 3)$: $a(1)^2 + b(1) + c = 3 \implies a + b + c = 3$.
- For $(2, 9)$: $a(2)^2 + b(2) + c = 9 \implies 4a + 2b + c = 9$.

This gives the linear system

$$
\begin{cases}
c = 1, \\
a + b + c = 3, \\
4a + 2b + c = 9.
\end{cases}
$$

### 2. Solving for $a$, $b$, and $c$

Substitute $c = 1$ into the second and third equations:

$$
\begin{cases}
a + b + 1 = 3 \implies a + b = 2, \\
4a + 2b + 1 = 9 \implies 4a + 2b = 8.
\end{cases}
$$

Divide the second simplified equation by $2$:

$$
2a + b = 4
$$

Subtract $a + b = 2$ from $2a + b = 4$:

$$
(2a + b) - (a + b) = 4 - 2 \implies a = 2
$$

Substitute $a = 2$ into $a + b = 2$:

$$
2 + b = 2 \implies b = 0
$$

With $a = 2$, $b = 0$, and $c = 1$, the polynomial is

$$
p(x) = 2x^2 + 1
$$

### 3. Verification at All Three Points

Evaluate $p(x) = 2x^2 + 1$ at each given $x$-coordinate:

- At $x = 0$: $p(0) = 2(0)^2 + 1 = 1$, which matches $(0, 1)$.
- At $x = 1$: $p(1) = 2(1)^2 + 1 = 3$, which matches $(1, 3)$.
- At $x = 2$: $p(2) = 2(2)^2 + 1 = 9$, which matches $(2, 9)$.

All three points lie on the graph of $p(x) = 2x^2 + 1$.
