### Exercise 6. Transpose of a Product

## Question

Let

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix}, \quad B = \begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

Compute $A^T$, $B^T$, and $AB$. Then verify in this example that $(AB)^T = B^T A^T$.

## Solution

1. **Computing $A^T$ and $B^T$:**
   By swapping the rows and columns of each matrix:

$$
A^T = \begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix}, \quad B^T = \begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
$$

2. **Computing the product $AB$:**
   Since $A$ is $2 \times 3$ and $B$ is $3 \times 2$, their product $AB$ is a $2 \times 2$ matrix:

$$
AB = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
= \begin{pmatrix}
(1)(1)+(2)(2)+(3)(-1) & (1)(0)+(2)(1)+(3)(3) \\
(4)(1)+(5)(2)+(6)(-1) & (4)(0)+(5)(1)+(6)(3) \\
\end{pmatrix}
= \begin{pmatrix}
2 & 11 \\
8 & 23 \\
\end{pmatrix}
$$

3. **Computing $(AB)^T$:**

$$
(AB)^T = \begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
$$

4. **Computing the product $B^T A^T$:**
   Since $B^T$ is $2 \times 3$ and $A^T$ is $3 \times 2$, their product $B^T A^T$ is a $2 \times 2$ matrix:

$$
B^T A^T = \begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix}
= \begin{pmatrix}
(1)(1)+(2)(2)+(-1)(3) & (1)(4)+(2)(5)+(-1)(6) \\
(0)(1)+(1)(2)+(3)(3) & (0)(4)+(1)(5)+(3)(6) \\
\end{pmatrix}
= \begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
$$

## Verification

Comparing the transpose of the product with the product of the transposes:

$$
(AB)^T = \begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix} = B^T A^T
$$

Both resulting matrices are identical, fully verifying the property $(AB)^T = B^T A^T$ for these matrices.
