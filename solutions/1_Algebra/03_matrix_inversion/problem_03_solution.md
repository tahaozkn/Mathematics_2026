### Exercise 3. When Does the Inverse Not Exist?

## Question

For

$$
A = \begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

## Solution

1. **Method 1: Using the Determinant**
   - Compute the determinant of $A$ using the $2 \times 2$ determinant formula ($ad - bc$):

$$
\det A = (2)(2) - (4)(1) = 4 - 4 = 0
$$

   - **Explanation:** A square matrix $A$ is invertible if and only if its determinant is non-zero ($\det A \neq 0$). In the explicit $2 \times 2$ inverse formula, the scalar multiplier is $\frac{1}{\det A}$. Because $\det A = 0$, this requires division by zero, which is undefined. Therefore, the inverse matrix $A^{-1}$ does not exist.

2. **Method 2: Using Dependence Between the Rows**
   - Let the rows of $A$ be denoted by $\mathbf{r}_1$ and $\mathbf{r}_2$:

$$
\mathbf{r}_1 = \begin{pmatrix} 2 & 4 \end{pmatrix}, \quad
\mathbf{r}_2 = \begin{pmatrix} 1 & 2 \end{pmatrix}
$$

   - Comparing the two rows, we observe that the first row is a scalar multiple of the second row:

$$
\mathbf{r}_1 = 2\mathbf{r}_2
$$

   - **Explanation:** Because the rows are linearly dependent, the matrix $A$ maps the entire 2D plane onto a 1D line (collapsing area to zero). A matrix transformation that loses dimensional information is not one-to-one (injective), meaning multiple different input vectors produce the same output vector. Consequently, it is impossible to uniquely "undo" the transformation, so no inverse matrix can exist.

## Verification

We can verify that $A$ is singular by showing it maps a non-zero vector to the zero vector. Consider the non-zero vector:

$$
\mathbf{x} = \begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}
$$

Multiply $A$ by $\mathbf{x}$:

$$
A\mathbf{x} = \begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}
= \begin{pmatrix}
2(-2) + 4(1) \\
1(-2) + 2(1) \\
\end{pmatrix}
= \begin{pmatrix}
-4 + 4 \\
-2 + 2 \\
\end{pmatrix}
= \begin{pmatrix}
0 \\
0 \\
\end{pmatrix}
$$

Because a non-zero vector $\mathbf{x}$ is mapped to the zero vector $\mathbf{0}$, no matrix $A^{-1}$ can possibly reverse this operation (since any matrix multiplied by $\mathbf{0}$ yields $\mathbf{0}$, preventing the recovery of $\mathbf{x}$), confirming that $A^{-1}$ does not exist.
