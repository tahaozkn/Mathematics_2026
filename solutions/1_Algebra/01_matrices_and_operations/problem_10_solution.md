### Exercise 10. Columns of a Matrix Product

## Question

Given

$$
A = \begin{pmatrix}
1 & 2 \\
0 & 0 \\
1 & 1 \\
\end{pmatrix}, \quad B = \begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

Denote the columns of $B$ by $\mathbf{b}_1, \mathbf{b}_2$.

1. Compute $A\mathbf{b}_1$ and $A\mathbf{b}_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $A\mathbf{b}_1$ and $A\mathbf{b}_2$.

## Solution

1. **Computing $A\mathbf{b}_1$ and $A\mathbf{b}_2$:**
   The columns of matrix $B$ are:
   
$$
\mathbf{b}_1 = \begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix}, \quad \mathbf{b}_2 = \begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}
$$

   Multiplying matrix $A$ by each column vector:

$$
A\mathbf{b}_1 = \begin{pmatrix}
1 & 2 \\
0 & 0 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix}
= \begin{pmatrix}
(1)(1) + (2)(-1) \\
(0)(1) + (0)(-1) \\
(1)(1) + (1)(-1) \\
\end{pmatrix}
= \begin{pmatrix}
-1 \\
0 \\
0 \\
\end{pmatrix}
$$

$$
A\mathbf{b}_2 = \begin{pmatrix}
1 & 2 \\
0 & 0 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}
= \begin{pmatrix}
(1)(2) + (2)(0) \\
(0)(2) + (0)(0) \\
(1)(2) + (1)(0) \\
\end{pmatrix}
= \begin{pmatrix}
2 \\
0 \\
2 \\
\end{pmatrix}
$$

2. **Computing the matrix $AB$:**

$$
AB = \begin{pmatrix}
1 & 2 \\
0 & 0 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
(1)(1)+(2)(-1) & (1)(2)+(2)(0) \\
(0)(1)+(0)(-1) & (0)(2)+(0)(0) \\
(1)(1)+(1)(-1) & (1)(2)+(1)(0) \\
\end{pmatrix}
= \begin{pmatrix}
-1 & 2 \\
0 & 0 \\
0 & 2 \\
\end{pmatrix}
$$

3. **Comparison and Explanation:**
   Comparing the columns of the product matrix $AB$ with the computed vector products:
   - The first column of $AB$ is $\begin{pmatrix} -1 & 0 & 0 \end{pmatrix}^T$, which is precisely $A\mathbf{b}_1$.
   - The second column of $AB$ is $\begin{pmatrix} 2 & 0 & 2 \end{pmatrix}^T$, which is precisely $A\mathbf{b}_2$.
   
   **Explanation:** By definition of matrix multiplication, the columns of a product matrix $AB$ are formed by multiplying the matrix $A$ by each individual column of $B$ (i.e., $AB = \begin{pmatrix} A\mathbf{b}_1 & A\mathbf{b}_2 \end{pmatrix}$). Thus, each column of $AB$ is a linear combination of the columns of $A$ weighted by the entries of the corresponding column of $B$.

## Verification

We can verify this property directly from the definition of column-by-column multiplication:

$$
AB = \begin{pmatrix} A\mathbf{b}_1 & A\mathbf{b}_2 \end{pmatrix} = \begin{pmatrix}
\begin{pmatrix} -1 \\ 0 \\ 0 \end{pmatrix} & \begin{pmatrix} 2 \\ 0 \\ 2 \end{pmatrix}
\end{pmatrix} = \begin{pmatrix}
-1 & 2 \\
0 & 0 \\
0 & 2 \\
\end{pmatrix}
$$

The direct matrix product matches the column-wise products identically, fully verifying the relationship.
