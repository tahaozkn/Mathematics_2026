### Exercise 3. Swapping Two Rows

## Question

For

$$
A =
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.

First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

## Solution

We compute $\det A$ using Sarrus' rule by repeating the first two columns of $A$ to the right:

$$
\begin{array}{ccc|cc}
1 & 2 & 0 & 1 & 2 \\
0 & 3 & 1 & 0 & 3 \\
2 & 1 & 1 & 2 & 1 \\
\end{array}
$$

Sum the products of the downward diagonals:

$$
\begin{aligned}
D_{\mathrm{down}} &= (1)(3)(1) + (2)(1)(2) + (0)(0)(1) \\
&= 3 + 4 + 0 \\
&= 7
\end{aligned}
$$

Sum the products of the upward diagonals:

$$
\begin{aligned}
D_{\mathrm{up}} &= (2)(3)(0) + (1)(1)(1) + (1)(0)(2) \\
&= 0 + 1 + 0 \\
&= 1
\end{aligned}
$$

Subtracting the upward sum from the downward sum gives:

$$
\det A = D_{\mathrm{down}} - D_{\mathrm{up}} = 7 - 1 = 6
$$

**Forming $B$ and predicting $\det B$:**
Swapping the first and second rows of $A$ gives the matrix:

$$
B =
\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

By the alternating property of determinants, interchanging two rows of a square matrix reverses the sign of its determinant. Since $\det A = 6$, we predict:

$$
\det B = -\det A = -6
$$

## Verification

We verify our prediction by computing $\det B$ directly using Sarrus' rule:

$$
\begin{array}{ccc|cc}
0 & 3 & 1 & 0 & 3 \\
1 & 2 & 0 & 1 & 2 \\
2 & 1 & 1 & 2 & 1 \\
\end{array}
$$

Sum the products of the downward diagonals:

$$
\begin{aligned}
D_{\mathrm{down}} &= (0)(2)(1) + (3)(0)(2) + (1)(1)(1) \\
&= 0 + 0 + 1 \\
&= 1
\end{aligned}
$$

Sum the products of the upward diagonals:

$$
\begin{aligned}
D_{\mathrm{up}} &= (2)(2)(1) + (1)(0)(0) + (1)(1)(3) \\
&= 4 + 0 + 3 \\
&= 7
\end{aligned}
$$

Subtracting the upward sum from the downward sum yields:

$$
\det B = D_{\mathrm{down}} - D_{\mathrm{up}} = 1 - 7 = -6
$$

This matches our prediction of $-6$, confirming the sign-reversal property of row swaps.
