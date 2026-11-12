### Exercise 2. Determinant of a $3 \times 3$ Matrix

## Question

For

$$
A =
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix}
$$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

## Solution

To apply Sarrus' rule, we repeat the first two columns of $A$ to the right of the matrix:

$$
\begin{array}{ccc|cc}
1 & 2 & -1 & 1 & 2 \\
0 & 3 & 4 & 0 & 3 \\
2 & 1 & 5 & 2 & 1 \\
\end{array}
$$

Next, we sum the products of the three downward-sloping diagonals (from top-left to bottom-right):

$$
\begin{aligned}
D_{\text{down}} &= (1)(3)(5) + (2)(4)(2) + (-1)(0)(1) \\
&= 15 + 16 + 0 \\
&= 31
\end{aligned}
$$

Then, we sum the products of the three upward-sloping diagonals (from bottom-left to top-right):

$$
\begin{aligned}
D_{\text{up}} &= (2)(3)(-1) + (1)(4)(1) + (5)(0)(2) \\
&= -6 + 4 + 0 \\
&= -2
\end{aligned}
$$

Subtracting the upward sum from the downward sum gives the determinant:

$$
\det A = D_{\text{down}} - D_{\text{up}} = 31 - (-2) = 31 + 2 = 33
$$

## Verification

We can check this result using the property that adding a scalar multiple of one row to another row leaves the determinant unchanged, and the determinant of an upper triangular matrix is the product of its diagonal entries.

Starting with $A$:

$$
A =
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix}
$$

1. Perform $R_3 \leftarrow R_3 - 2R_1$ (determinant unchanged):

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
0 & -3 & 7 \\
\end{pmatrix}
$$

2. Perform $R_3 \leftarrow R_3 + R_2$ (determinant unchanged):

$$
U =
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
0 & 0 & 11 \\
\end{pmatrix}
$$

Since $U$ is upper triangular, its determinant is the product of its main diagonal entries:

$$
\det A = \det U = (1)(3)(11) = 33
$$

This matches the value obtained via Sarrus' rule, confirming $\det A = 33$.
