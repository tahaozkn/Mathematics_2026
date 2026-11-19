### Exercise 12. A Parameter Revealed by a Row Operation

## Question

For

$$
A(t) = \begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{pmatrix}
$$

find the values of $t$ for which the matrix is not invertible.

Before computing the determinant, perform the operation $R_2 \leftarrow R_2 - 2R_1$ and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

## Solution

1. **Perform the Specified Row Operation:**
   Apply the row operation $R_2 \leftarrow R_2 - 2R_1$ to matrix $A(t)$:

$$
\begin{pmatrix}
1 & 2 & 3 \\
2 - 2(1) & 4 - 2(2) & t - 2(3) \\
0 & 1 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & t - 6 \\
0 & 1 & 1 \\
\end{pmatrix}
$$

2. **Compute the Determinant:**
   The row operation $R_2 \leftarrow R_2 - 2R_1$ is a row addition, which **preserves the exact value of the determinant**. Therefore, $\det A(t)$ equals the determinant of the transformed matrix:

$$
\det A(t) = \det \begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & t - 6 \\
0 & 1 & 1 \\
\end{pmatrix}
$$

   We can evaluate this determinant by expanding along the first column or by swapping rows 2 and 3. Swapping two rows multiplies the determinant by $-1$:

$$
\det A(t) = -\det \begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & t - 6 \\
\end{pmatrix}
$$

   Since the resulting matrix is upper triangular, its determinant is simply the product of its main diagonal entries:

$$
\det A(t) = -(1)(1)(t - 6) = -(t - 6) = 6 - t
$$

3. **Find the Value of $t$ for Noninvertibility:**
   A square matrix is **not invertible** (singular) if and only if its determinant is zero:

$$
\det A(t) = 0 \implies 6 - t = 0 \implies t = 6
$$

   Thus, the matrix is not invertible when **$t = 6$**.

4. **Explanation of What Happens to the Rows at $t = 6$:**
   Substituting $t = 6$ back into the row-operated matrix gives:

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & 6 - 6 \\
0 & 1 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
$$

   At $t = 6$, the second row becomes an **entire row of zeros** after the row operation. In terms of the original matrix $A(6)$, the second row is $\begin{pmatrix} 2 & 4 & 6 \end{pmatrix}$, which is exactly **twice the first row** ($2\mathbf{r}_1$). This linear dependence among the rows causes the matrix to lose full rank, collapsing 3D space into a lower-dimensional subspace and yielding a determinant of zero.

## Verification

We can verify the determinant calculation by expanding the original matrix $A(t)$ directly along the first column using cofactor expansion:

$$
\det A(t) = 1 \cdot \det \begin{pmatrix}
4 & t \\
1 & 1 \\
\end{pmatrix}
- 2 \cdot \det \begin{pmatrix}
2 & 3 \\
1 & 1 \\
\end{pmatrix}
+ 0 \cdot \det \begin{pmatrix}
2 & 3 \\
4 & t \\
\end{pmatrix}
$$

Evaluating the $2 \times 2$ determinants:
- First term: $1 \cdot (4(1) - t(1)) = 4 - t$
- Second term: $-2 \cdot (2(1) - 3(1)) = -2(2 - 3) = -2(-1) = 2$
- Third term: $0$

Combining the terms:

$$
(4 - t) + 2 = 6 - t
$$

Setting $6 - t = 0$ yields $t = 6$, perfectly confirming our row-operation result.
