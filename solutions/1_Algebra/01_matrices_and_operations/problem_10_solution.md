### Exercise 10. Matrix Operations and Linear Combinations

## Question

Let

$$
A = \begin{pmatrix}
1 & -2 & 3 \\
0 & 4 & -1 \\
\end{pmatrix}, \quad B = \begin{pmatrix}
2 & 1 & 0 \\
-1 & 3 & 2 \\
\end{pmatrix}
$$

Compute $A + B$, $3A - 2B$, and explain whether the product $AB$ is defined.

## Solution

1. **Computing $A + B$:**
   Add corresponding entries of the $2 \times 3$ matrices $A$ and $B$:

$$
A + B = \begin{pmatrix}
1+2 & -2+1 & 3+0 \\
0+(-1) & 4+3 & -1+2 \\
\end{pmatrix}
= \begin{pmatrix}
3 & -1 & 3 \\
-1 & 7 & 1 \\
\end{pmatrix}
$$

2. **Computing $3A - 2B$:**
   First, perform scalar multiplication on each matrix:

$$
3A = \begin{pmatrix}
3(1) & 3(-2) & 3(3) \\
3(0) & 3(4) & 3(-1) \\
\end{pmatrix}
= \begin{pmatrix}
3 & -6 & 9 \\
0 & 12 & -3 \\
\end{pmatrix}
$$

$$
2B = \begin{pmatrix}
2(2) & 2(1) & 2(0) \\
2(-1) & 2(3) & 2(2) \\
\end{pmatrix}
= \begin{pmatrix}
4 & 2 & 0 \\
-2 & 6 & 4 \\
\end{pmatrix}
$$

Then subtract the resulting matrices:

$$
3A - 2B = \begin{pmatrix}
3-4 & -6-2 & 9-0 \\
0-(-2) & 12-6 & -3-4 \\
\end{pmatrix}
= \begin{pmatrix}
-1 & -8 & 9 \\
2 & 6 & -7 \\
\end{pmatrix}
$$

3. **Product $AB$:**
   Matrix $A$ has dimensions $2 \times 3$ and matrix $B$ has dimensions $2 \times 3$. Because the inner dimensions do not match (the number of columns of $A$ is $3$, while the number of rows of $B$ is $2$), the product $AB$ is **not defined**.

## Verification

We verify the matrix addition and scalar operations using column vectors. For $3A - 2B$, checking the first column:

$$
3 \begin{pmatrix}
1 \\
0 \\
\end{pmatrix}
- 2 \begin{pmatrix}
2 \\
-1 \\
\end{pmatrix}
= \begin{pmatrix}
3 \\
0 \\
\end{pmatrix}
- \begin{pmatrix}
4 \\
-2 \\
\end{pmatrix}
= \begin{pmatrix}
-1 \\
2 \\
\end{pmatrix}
$$

This matches the first column of our computed result matrix, fully verifying the calculations.
