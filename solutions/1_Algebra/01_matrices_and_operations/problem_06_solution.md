### Exercise 6. Transpose

## Question

For

$$A = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ \end{pmatrix}$$

and

$$B = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \\ \end{pmatrix}$$

compute $A^T$, $B^T$, and $AB$. Then verify in this example that

$$(AB)^T = B^T A^T.$$

## Solution

The transpose of a matrix is obtained by swapping its rows and columns. 

For $A$ (size $2 \times 3$), its transpose $A^T$ (size $3 \times 2$) is:

$$A^T = \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \\ \end{pmatrix}$$

For $B$ (size $3 \times 2$), its transpose $B^T$ (size $2 \times 3$) is:

$$B^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \\ \end{pmatrix}$$

Next, we compute the product $AB$:

$$\begin{aligned} AB &= \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \\ \end{pmatrix} \\ &= \begin{pmatrix} 1\cdot 1 + 2\cdot 2 + 3\cdot (-1) & 1\cdot 0 + 2\cdot 1 + 3\cdot 3 \\ 4\cdot 1 + 5\cdot 2 + 6\cdot (-1) & 4\cdot 0 + 5\cdot 1 + 6\cdot 3 \\ \end{pmatrix} \\ &= \begin{pmatrix} 1 + 4 - 3 & 0 + 2 + 9 \\ 4 + 10 - 6 & 0 + 5 + 18 \\ \end{pmatrix} \\ &= \begin{pmatrix} 2 & 11 \\ 8 & 23 \\ \end{pmatrix} \end{aligned}$$

## Verification

To verify the property $(AB)^T = B^T A^T$, we compute both sides independently.

First, transposing the product $AB$ gives:

$$(AB)^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \\ \end{pmatrix}$$

Second, we compute the product $B^T A^T$:  $$
\begin{aligned}
B^T A^T &=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1\cdot 1 + 2\cdot 2 + (-1)\cdot 3 & 1\cdot 4 + 2\cdot 5 + (-1)\cdot 6 \\
