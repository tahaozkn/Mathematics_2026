### Exercise 12. Finding Inverses Without Starting from Scratch

## Question

It is known that

$$
A^{-1} = \begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}.
$$

Without finding $A$, compute $(3A)^{-1}$, $(A^T)^{-1}$, and $(A^2)^{-1}$. Justify each result using the appropriate property.

## Solution

1. **Compute $(3A)^{-1}$:**
   - **Property:** For any invertible matrix $A$ and any non-zero scalar $c \neq 0$, the inverse of a scalar multiple is given by:

$$
(cA)^{-1} = \frac{1}{c} A^{-1}
$$

     This holds because $(cA)\left(\frac{1}{c}A^{-1}\right) = \left(c \cdot \frac{1}{c}\right)(AA^{-1}) = 1 \cdot I = I$.
   - **Calculation:** Using $c = 3$:

$$
\begin{aligned}
(3A)^{-1} &= \frac{1}{3} A^{-1} \\
&= \frac{1}{3} \begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{2}{3} & -\frac{1}{3} \\
-1 & \frac{2}{3} \\
\end{pmatrix}
\end{aligned}
$$

2. **Compute $(A^T)^{-1}$:**
   - **Property:** For any invertible matrix $A$, the inverse of the transpose equals the transpose of the inverse:

$$
(A^T)^{-1} = (A^{-1})^T
$$

     This holds because taking the transpose of $AA^{-1} = I$ reverses the product order: $(A^{-1})^T A^T = I^T = I$.
   - **Calculation:** Transpose the given matrix $A^{-1}$ by swapping its rows and columns:

$$
\begin{aligned}
(A^T)^{-1} &= (A^{-1})^T \\
&= \begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}^T \\
&= \begin{pmatrix}
2 & -3 \\
-1 & 2 \\
\end{pmatrix}
\end{aligned}
$$

3. **Compute $(A^2)^{-1}$:**
   - **Property:** For any invertible matrix $A$ and positive integer $k$, the inverse of a matrix power equals the power of the inverse:

$$
(A^k)^{-1} = (A^{-1})^k
$$

     For $k = 2$, applying the inverse-of-a-product property gives $(A^2)^{-1} = (AA)^{-1} = A^{-1}A^{-1} = (A^{-1})^2$.
   - **Calculation:** Multiply $A^{-1}$ by itself:

$$
\begin{aligned}
(A^2)^{-1} &= (A^{-1})^2 \\
&= \begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2(2) + (-1)(-3) & 2(-1) + (-1)(2) \\
(-3)(2) + 2(-3) & (-3)(-1) + 2(2) \\
\end{pmatrix} \\
&= \begin{pmatrix}
4 + 3 & -2 - 2 \\
-6 - 6 & 3 + 4 \\
\end{pmatrix} \\
&= \begin{pmatrix}
7 & -4 \\
-12 & 7 \\
\end{pmatrix}
\end{aligned}
$$

## Verification

We can verify each result by explicitly recovering $A = (A^{-1})^{-1}$ and checking that each derived inverse multiplies with its corresponding matrix to yield the identity matrix $I$:

1. **Recover $A$ from $A^{-1}$:**
   With $\det(A^{-1}) = (2)(2) - (-1)(-3) = 4 - 3 = 1$:

$$
A = (A^{-1})^{-1} = \frac{1}{1} \begin{pmatrix}
2 & 1 \\
3 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
2 & 1 \\
3 & 2 \\
\end{pmatrix}
$$

2. **Check $(3A)(3A)^{-1} = I$:**
   With $3A = \begin{pmatrix} 6 & 3 \\ 9 & 6 \\ \end{pmatrix}$:

$$
(3A)(3A)^{-1} = \begin{pmatrix}
6 & 3 \\
9 & 6 \\
\end{pmatrix}
\begin{pmatrix}
\frac{2}{3} & -\frac{1}{3} \\
-1 & \frac{2}{3} \\
\end{pmatrix}
= \begin{pmatrix}
4 - 3 & -2 + 2 \\
6 - 6 & -3 + 4 \\
\end{pmatrix}
= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
= I
$$

3. **Check $A^T (A^T)^{-1} = I$:**
   With $A^T = \begin{pmatrix} 2 & 3 \\ 1 & 2 \\ \end{pmatrix}$:

$$
A^T (A^T)^{-1} = \begin{pmatrix}
2 & 3 \\
1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & -3 \\
-1 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
4 - 3 & -6 + 6 \\
2 - 2 & -3 + 4 \\
\end{pmatrix}
= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
= I
$$

4. **Check $A^2 (A^2)^{-1} = I$:**
   First compute $A^2 = \begin{pmatrix} 2 & 1 \\ 3 & 2 \\ \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 3 & 2 \\ \end{pmatrix} = \begin{pmatrix} 7 & 4 \\ 12 & 7 \\ \end{pmatrix}$:

$$
A^2 (A^2)^{-1} = \begin{pmatrix}
7 & 4 \\
12 & 7 \\
\end{pmatrix}
\begin{pmatrix}
7 & -4 \\
-12 & 7 \\
\end{pmatrix}
= \begin{pmatrix}
49 - 48 & -28 + 28 \\
84 - 84 & -48 + 49 \\
\end{pmatrix}
= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
= I
$$

All three products equal the identity matrix $I$, confirming the property-based results.
