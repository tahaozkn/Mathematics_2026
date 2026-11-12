### Exercise 4. Triangular Matrix

## Question

Without expanding the determinant, compute

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}.
$$

State the rule for an arbitrary triangular matrix and explain it using this example.

## Solution

Let $T$ denote the given upper triangular matrix:

$$
T =
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}
$$

The determinant of $T$ is the product of its main diagonal entries:

$$
\det(T) = (2)(-3)(7) = -42
$$

**Rule for an arbitrary triangular matrix:**
For any $n \times n$ triangular matrix (whether upper triangular, lower triangular, or diagonal), the determinant is equal to the product of the entries on its main diagonal:

$$
\det(T) = t_{11} t_{22} \cdots t_{nn}
$$

**Explanation using this example:**
In the determinant of a $3 \times 3$ matrix, every term in the full expansion is a product of three entries chosen such that exactly one entry comes from each row and each column. In matrix $T$, the third row has only one nonzero entry, $t_{33} = 7$ (in column $3$). Therefore, any nonzero product must select $7$ from row $3$, which leaves only columns $1$ and $2$ available for rows $1$ and $2$. Looking at row $2$, its only nonzero entry in columns $1$ and $2$ is $t_{22} = -3$ (in column $2$). This forces row $1$ to use column $1$, selecting $t_{11} = 2$. All other combinations include at least one zero entry and vanish, leaving only the main diagonal product $(2)(-3)(7)$.

## Verification

We can verify this result by applying Sarrus' rule to $T$:

$$
\begin{array}{ccc|cc}
2 & 4 & 1 & 2 & 4 \\
0 & -3 & 5 & 0 & -3 \\
0 & 0 & 7 & 0 & 0 \\
\end{array}
$$

Sum the products of the downward diagonals:

$$
\begin{aligned}
D_{\mathrm{down}} &= (2)(-3)(7) + (4)(5)(0) + (1)(0)(0) \\
&= -42 + 0 + 0 \\
&= -42
\end{aligned}
$$

Sum the products of the upward diagonals:

$$
\begin{aligned}
D_{\mathrm{up}} &= (0)(-3)(1) + (0)(5)(2) + (7)(0)(4) \\
&= 0 + 0 + 0 \\
&= 0
\end{aligned}
$$

Subtracting the upward sum from the downward sum gives:

$$
\det(T) = D_{\mathrm{down}} - D_{\mathrm{up}} = -42 - 0 = -42
$$

This matches the product of the diagonal entries, confirming $\det(T) = -42$.
