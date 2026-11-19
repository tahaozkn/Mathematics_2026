### Exercise 11. Shortening the Calculation with Row Operations

## Question

Compute

$$
\det \begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

## Solution

1. **Identify Determinant-Preserving Row Operations:**
   When evaluating determinants, certain elementary row operations preserve the exact value of the determinant:
   - **Adding a scalar multiple of one row to another ($R_i \leftarrow R_i + cR_j$ for $i \neq j$):** This operation does not change the determinant.
   - **Multiplying a row by a non-zero scalar ($R_i \leftarrow cR_i$):** This scales the determinant by $c$, and **interchanging two rows ($R_i \leftrightarrow R_j$)** multiplies the determinant by $-1$. Therefore, to preserve the exact value without scaling factors, we restrict ourselves to row additions.

2. **Perform Row Operations to Create Zeros:**
   Let $A$ be the given matrix. We want to introduce zeros into the first column using the leading $1$ in the top-left corner:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

   Apply $R_2 \leftarrow R_2 - R_1$ and $R_3 \leftarrow R_3 - R_1$. Since these are row-addition operations, the determinant remains completely unchanged:

$$
\det A = \det \begin{pmatrix}
1 & 2 & 3 \\
1 - 1 & 3 - 2 & 4 - 3 \\
1 - 1 & 4 - 2 & 6 - 3 \\
\end{pmatrix}
= \det \begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 2 & 3 \\
\end{pmatrix}
$$

   Next, apply $R_3 \leftarrow R_3 - 2R_2$ to eliminate the entry below the pivot in the second column:

$$
\det A = \det \begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 2 - 2(1) & 3 - 2(1) \\
\end{pmatrix}
= \det \begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

3. **Compute the Determinant:**
   The matrix has been successfully transformed into an **upper triangular matrix**. The determinant of an upper triangular matrix is simply the product of its main diagonal entries:

$$
\det A = (1)(1)(1) = 1
$$

## Verification

We can verify the result by performing a direct cofactor expansion along the first column of the original matrix:

$$
\det \begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
= 1 \cdot \det \begin{pmatrix}
3 & 4 \\
4 & 6 \\
\end{pmatrix}
- 1 \cdot \det \begin{pmatrix}
2 & 3 \\
4 & 6 \\
\end{pmatrix}
+ 1 \cdot \det \begin{pmatrix}
2 & 3 \\
3 & 4 \\
\end{pmatrix}
$$

Evaluating each $2 \times 2$ determinant:
- First term: $1 \cdot ((3)(6) - (4)(4)) = 1 \cdot (18 - 16) = 2$
- Second term: $-1 \cdot ((2)(6) - (3)(4)) = -1 \cdot (12 - 12) = 0$
- Third term: $1 \cdot ((2)(4) - (3)(3)) = 1 \cdot (8 - 9) = -1$

Combining the terms:

$$
2 - 0 + (-1) = 1
$$

Both methods yield the exact same determinant of $1$, confirming our row-operation strategy.
