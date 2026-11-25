
# Exercise 3 – When Can Matrices Be Multiplied?

## Question

The matrix sizes are:

- A: $2 \times 3$
- B: $3 \times 4$
- C: $4 \times 2$
- D: $2 \times 2$

Determine whether the following matrix products are defined. If a product is defined, state the size of the resulting matrix.

$$
AB,\quad BA,\quad BC,\quad CB,
$$

$$
AC,\quad CA,\quad AD,\quad DA
$$

Justify each decision using the dimension compatibility condition.

## Solution

### 1. Condition for Matrix Multiplication

Before checking the products, I use the rule that the number of columns in the first matrix must be equal to the number of rows in the second matrix.

If matrix A has size $m \times n$ and matrix B has size $n \times p$, their product is defined and the result has size $m \times p$.

### 2. Checking Each Product

**1. Product AB**

A has size $2 \times 3$ and B has size $3 \times 4$.

The inner dimensions are both 3, so multiplication is possible.

The result has size $2 \times 4$.

$$
AB: (2 \times 3)(3 \times 4)
\Rightarrow 2 \times 4
$$

**2. Product BA**

B has size $3 \times 4$ and A has size $2 \times 3$.

The inner dimensions are 4 and 2. They are different, so multiplication is not possible.

$$
BA: (3 \times 4)(2 \times 3)
$$

Not defined.

**3. Product BC**

B has size $3 \times 4$ and C has size $4 \times 2$.

The inner dimensions are both 4, so multiplication is possible.

The result has size $3 \times 2$.

$$
BC: (3 \times 4)(4 \times 2)
\Rightarrow 3 \times 2
$$

**4. Product CB**

C has size $4 \times 2$ and B has size $3 \times 4$.

The inner dimensions are 2 and 3. They are different, so multiplication is not possible.

$$
CB: (4 \times 2)(3 \times 4)
$$

Not defined.

**5. Product AC**

A has size $2 \times 3$ and C has size $4 \times 2$.

The inner dimensions are 3 and 4. They are different, so multiplication is not possible.

$$
AC: (2 \times 3)(4 \times 2)
$$

Not defined.

**6. Product CA**

C has size $4 \times 2$ and A has size $2 \times 3$.

The inner dimensions are both 2, so multiplication is possible.

The result has size $4 \times 3$.

$$
CA: (4 \times 2)(2 \times 3)
\Rightarrow 4 \times 3
$$

**7. Product AD**

A has size $2 \times 3$ and D has size $2 \times 2$.

The inner dimensions are 3 and 2. They are different, so multiplication is not possible.

$$
AD: (2 \times 3)(2 \times 2)
$$

Not defined.

**8. Product DA**

D has size $2 \times 2$ and A has size $2 \times 3$.

The inner dimensions are both 2, so multiplication is possible.

The result has size $2 \times 3$.

$$
DA: (2 \times 2)(2 \times 3)
\Rightarrow 2 \times 3
$$

### 3. Summary of Results

| Product | Defined? | Result Size |
|---|---|---|
| AB | Yes | $2 \times 4$ |
| BA | No | Not defined |
| BC | Yes | $3 \times 2$ |
| CB | No | Not defined |
| AC | No | Not defined |
| CA | Yes | $4 \times 3$ |
| AD | No | Not defined |
| DA | Yes | $2 \times 3$ |

## Final Answer

The defined products are:

- $AB$, with size $2 \times 4$.
- $BC$, with size $3 \times 2$.
- $CA$, with size $4 \times 3$.
- $DA$, with size $2 \times 3$.

The products $BA$, $CB$, $AC$, and $AD$ are not defined because their inner dimensions do not match.

The important rule is that the number of columns in the first matrix must equal the number of rows in the second matrix.
