### Exercise 13. Determinant by Elimination

## Question

Compute the determinant

$$
\det \begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

using elimination. Record the effect of every row operation used on the value of the determinant.

## Solution

1. **Set Up the Initial Matrix:**
   Let $A$ be the given matrix:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

2. **Step 1: Eliminate Entries Below the Pivot in Column 1:**
   - Apply $R_2 \leftarrow R_2 - 2R_1$ to eliminate the entry in the second row, first column:
     - New second row: $(2 - 2(1), 5 - 2(2), 7 - 2(3)) = (0, 1, 1)$
     - **Effect on determinant:** Adding a scalar multiple of one row to another **preserves the exact value** of the determinant ($\det(\text{new}) = 1 \cdot \det(\text{old})$).
   - Apply $R_3 \leftarrow R_3 - R_1$ to eliminate the entry in the third row, first column:
     - New third row: $(1 - 1, 0 - 2, 2 - 3) = (0, -2, -1)$
     - **Effect on determinant:** This is another row addition, which also **preserves the exact value** of the determinant.

   After these two operations, the matrix becomes:

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & -2 & -1 \\
\end{pmatrix}
$$

3. **Step 2: Eliminate the Entry Below the Pivot in Column 2:**
   - Apply $R_3 \leftarrow R_3 + 2R_2$ to eliminate the $-2$ in the third row, second column:
     - New third row: $(0 + 2(0), -2 + 2(1), -1 + 2(1)) = (0, 0, 1)$
     - **Effect on determinant:** Adding a multiple of row 2 to row 3 **preserves the exact value** of the determinant.

   The matrix is now in **upper triangular form**:

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

4. **Step 3: Compute the Determinant:**
   Because all performed row operations were row additions (each having a determinant scaling factor of $1$), the determinant of the original matrix equals the determinant of the final upper triangular matrix. The determinant of an upper triangular matrix is the product of its main diagonal entries:

$$
\det A = (1)(1)(1) = 1
$$

## Verification

We can verify the determinant calculation by expanding the original matrix along the first row using cofactor expansion:

$$
\det A = 1 \cdot \det \begin{pmatrix}
5 & 7 \\
0 & 2 \\
\end{pmatrix}
- 2 \cdot \det \begin{pmatrix}
2 & 7 \\
1 & 2 \\
\end{pmatrix}
+ 3 \cdot \det \begin{pmatrix}
2 & 5 \\
1 & 0 \\
\end{pmatrix}
$$

Evaluating each $2 \times 2$ determinant:
- First term: $1 \cdot ((5)(2) - (7)(0)) = 1 \cdot (10 - 0) = 10$
- Second term: $-2 \cdot ((2)(2) - (7)(1)) = -2 \cdot (4 - 7) = -2(-3) = 6$
- Third term: $3 \cdot ((2)(0) - (5)(1)) = 3 \cdot (0 - 5) = -15$

Combining the terms:

$$
10 + 6 + (-15) = 1
$$

Both elimination and cofactor expansion yield a determinant of $1$, confirming our step-by-step reduction.
