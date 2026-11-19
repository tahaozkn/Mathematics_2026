### Exercise 10. Detecting Dependence

## Question

Without carrying out a full determinant calculation, explain why

$$
\det \begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}
= 0.
$$

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

## Solution

1. **Identify the Row Dependence:**
   Let the rows of the matrix be denoted by $\mathbf{r}_1$, $\mathbf{r}_2$, and $\mathbf{r}_3$:

$$
\mathbf{r}_1 = \begin{pmatrix} 1 & 2 & 3 \end{pmatrix}, \quad
\mathbf{r}_2 = \begin{pmatrix} 2 & 4 & 6 \end{pmatrix}, \quad
\mathbf{r}_3 = \begin{pmatrix} 0 & 1 & 5 \end{pmatrix}
$$

   Comparing the first two rows, we observe that the second row is exactly twice the first row:

$$
\mathbf{r}_2 = 2\mathbf{r}_1
$$

   Because one row is a scalar multiple of another, the set of rows is linearly dependent.

2. **Why the Determinant is Zero Without Full Calculation:**
   Using elementary row operations, we can apply $R_2 \leftarrow R_2 - 2R_1$ to eliminate the second row:

$$
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & 1 & 5 \\
\end{pmatrix}
$$

   The resulting matrix has an entire row of zeros ($\mathbf{r}_2 = \mathbf{0}$). A fundamental property of determinants states that if a square matrix contains a row (or column) of zeros, its determinant is strictly $0$. Furthermore, row operations of this type do not change the value of the determinant, so the original matrix must also have a determinant of $0$.

3. **Connection to Noninvertibility:**
   A square matrix is invertible (nonsingular) if and only if its determinant is non-zero ($\det A \neq 0$). Because $\det A = 0$, the matrix is **noninvertible** (singular). 
   
   Geometrically, linear dependence among the rows means the rows (and columns) lie in a lower-dimensional subspace (a plane in $\mathbb{R}^3$ rather than spanning the entire 3D space). Consequently, the linear transformation represented by this matrix collapses space, making it impossible to uniquely reverse the transformation (i.e., no inverse transformation exists).

## Verification

We can confirm $\det A = 0$ by expanding along the second row (which contains zeros) or by cofactor expansion along the first column:

$$
\det \begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}
= 1 \cdot \det \begin{pmatrix}
4 & 6 \\
1 & 5 \\
\end{pmatrix}
- 2 \cdot \det \begin{pmatrix}
2 & 3 \\
1 & 5 \\
\end{pmatrix}
+ 0 \cdot \det \begin{pmatrix}
2 & 3 \\
4 & 6 \\
\end{pmatrix}
$$

Evaluating the $2 \times 2$ determinants:
- First term: $1 \cdot ((4)(5) - (6)(1)) = 1 \cdot (20 - 6) = 14$
- Second term: $-2 \cdot ((2)(5) - (3)(1)) = -2 \cdot (10 - 3) = -14$
- Third term: $0$

Combining the terms:

$$
14 - 14 + 0 = 0
$$

The calculation confirms that $\det A = 0$, perfectly matching our structural analysis.
