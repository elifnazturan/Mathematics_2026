# Exercise 14. A Small Change in the Right-Hand Side

## Question

We compare two linear systems in two unknowns $(x, y)$:

**System 1**

$$
\begin{cases}
x + y = 2, \\
2x - y = 1, \\
3x = 3.
\end{cases}
$$

**System 2**

$$
\begin{cases}
x + y = 2, \\
2x - y = 1, \\
3x = 3.1.
\end{cases}
$$

We need to:
1. Check the consistency of each system.
2. Explain why a small change in a single right-hand side number can change the type of the system.

## Solution

### 1. Consistency of System 1

Add the first two equations of System 1:

$$
(x + y) + (2x - y) = 2 + 1 \implies 3x = 3 \implies x = 1
$$

Substitute $x = 1$ into the first equation $x + y = 2$:

$$
1 + y = 2 \implies y = 1
$$

Check all three equations at $(x, y) = (1, 1)$:
- First equation: $1 + 1 = 2$ (holds).
- Second equation: $2(1) - 1 = 1$ (holds).
- Third equation: $3(1) = 3$ (holds).

Because $(1, 1)$ satisfies every equation simultaneously, **System 1 is consistent** with the unique solution $(x, y) = (1, 1)$.

### 2. Consistency of System 2

From the first two equations of System 2, adding them again gives:

$$
(x + y) + (2x - y) = 2 + 1 \implies 3x = 3 \implies x = 1
$$

However, the third equation of System 2 requires:

$$
3x = 3.1 \implies x = \frac{3.1}{3} = \frac{31}{30}
$$

No real number $x$ can simultaneously satisfy $3x = 3$ and $3x = 3.1$ (eliminating $x$ gives $0 = 0.1$, a contradiction). Therefore, **System 2 is inconsistent** and has no solution.

### 3. Why a Small Change in One Number Changes the System Type

The left-hand side of the third equation ($3x$) is already determined as a linear combination of the first two equations: adding $(x + y)$ and $(2x - y)$ yields $3x$, which for the first two right-hand sides $2$ and $1$ equals $2 + 1 = 3$.

- In **System 1**, the third right-hand side equals $3$, so the third condition agrees with the combination of the first two equations and all three lines meet at $(1, 1)$.
- In **System 2**, changing $3$ slightly to $3.1$ makes the third equation incompatible with the linear combination $3x = 3$ implied by the first two equations. Geometrically, the third line $x = \frac{31}{30}$ no longer passes through the intersection $(1, 1)$ of the first two lines, shifting a consistent system with a unique solution into an inconsistent system with no solution.
