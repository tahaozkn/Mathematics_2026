### Exercise 5. Row Operations

## Question

For

$$
A =
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

## Solution

We reduce $A$ to an upper triangular matrix $U$ using elementary row operations while tracking the effect of each operation on the determinant:

$$
A =
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

**Step 1:** Perform $R_2 \leftarrow R_2 - 2R_1$.
Adding a scalar multiple of one row to another **does not change** the determinant ($\det A_1 = \det A$):

$$
A_1 =
\begin{pmatrix}
1 & 2 & 3 \\
2 - 2(1) & 1 - 2(2) & 0 - 2(3) \\
-1 & 4 & 2 \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

**Step 2:** Perform $R_3 \leftarrow R_3 + R_1$.
Adding a scalar multiple of one row to another **does not change** the determinant ($\det A_2 = \det A_1 = \det A$):

$$
A_2 =
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
-1 + 1 & 4 + 2 & 2 + 3 \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5 \\
\end{pmatrix}
$$

**Step 3:** Perform $R_3 \leftarrow R_3 + 2R_2$.
Adding a scalar multiple of one row to another **does not change** the determinant ($\det U = \det A_2 = \det A$):

$$
U =
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 + 2(-3) & 5 + 2(-6) \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 0 & -7 \\
\end{pmatrix}
$$

Since $U$ is upper triangular, its determinant is the product of its main diagonal entries, and because none of the row replacements altered the determinant:

$$
\det A = \det U = (1)(-3)(-7) = 21
$$

## Verification

We can verify this result independently by applying Sarrus' rule to the original matrix $A$:

$$
\begin{array}{ccc|cc}
1 & 2 & 3 & 1 & 2 \\
2 & 1 & 0 & 2 & 1 \\
-1 & 4 & 2 & -1 & 4 \\
\end{array}
$$

Sum the products of the downward diagonals:

$$
\begin{aligned}
D_{\mathrm{down}} &= (1)(1)(2) + (2)(0)(-1) + (3)(2)(4) \\
&= 2 + 0 + 24 \\
&= 26
\end{aligned}
$$

Sum the products of the upward diagonals:

$$
\begin{aligned}
D_{\mathrm{up}} &= (-1)(1)(3) + (4)(0)(1) + (2)(2)(2) \\
&= -3 + 0 + 8 \\
&= 5
\end{aligned}
$$

Subtracting the upward sum from the downward sum gives:

$$
\det A = D_{\mathrm{down}} - D_{\mathrm{up}} = 26 - 5 = 21
$$

Both methods yield $\det A = 21$, confirming the row reduction steps and final determinant.
