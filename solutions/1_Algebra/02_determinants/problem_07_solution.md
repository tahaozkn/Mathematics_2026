### Exercise 7. Using Properties Instead of Recomputing

## Question

Suppose that for a $3 \times 3$ matrix $A$, $\det A = -4$. Compute

$$
\det(2A), \qquad \det(A^T), \qquad \det(A^2), \qquad \det(-A).
$$

Justify each answer using the appropriate property.

## Solution

Given that $A$ is an $n \times n$ matrix with $n = 3$ and $\det A = -4$, we apply standard determinant properties to compute each expression:

1. **Computing $\det(2A)$:**
   For any $n \times n$ matrix $A$ and scalar $c$, multiplying the entire matrix by $c$ scales each of the $n$ rows by $c$, which multiplies the determinant by $c^n$:

   $$
   \det(cA) = c^n \det A
   $$

   With $n = 3$ and $c = 2$:

   $$
   \det(2A) = 2^3 \det A = 8(-4) = -32
   $$

2. **Computing $\det(A^T)$:**
   The determinant of the transpose of a square matrix is equal to the determinant of the original matrix:

   $$
   \det(A^T) = \det A = -4
   $$

3. **Computing $\det(A^2)$:**
   By the multiplicative property of determinants, $\det(AB) = (\det A)(\det B)$ for any two $n \times n$ matrices $A$ and $B$. Setting $B = A$ gives $\det(A^2) = (\det A)^2$:

   $$
   \det(A^2) = (\det A)^2 = (-4)^2 = 16
   $$

4. **Computing $\det(-A)$:**
   Writing $-A = (-1)A$ and applying the scalar multiplication property $\det(cA) = c^n \det A$ with $n = 3$ and $c = -1$:

   $$
   \det(-A) = (-1)^3 \det A = (-1)(-4) = 4
   $$

## Verification

We can verify these four results using a concrete $3 \times 3$ diagonal matrix whose determinant is $-4$:

$$
A =
\begin{pmatrix}
-4 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

Here, $\det A = (-4)(1)(1) = -4$. Constructing each transformed matrix directly and taking the product of its diagonal entries gives:

1. **For $2A$:**

$$
2A =
\begin{pmatrix}
-8 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2 \\
\end{pmatrix}
\implies \det(2A) = (-8)(2)(2) = -32
$$

2. **For $A^T$:**

$$
A^T =
\begin{pmatrix}
-4 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}
\implies \det(A^T) = (-4)(1)(1) = -4
$$

3. **For $A^2$:**

$$
A^2 =
\begin{pmatrix}
(-4)^2 & 0 & 0 \\
0 & 1^2 & 0 \\
0 & 0 & 1^2 \\
\end{pmatrix}
=
\begin{pmatrix}
16 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}
\implies \det(A^2) = (16)(1)(1) = 16
$$

4. **For $-A$:**

$$
-A =
\begin{pmatrix}
4 & 0 & 0 \\
0 & -1 & 0 \\
0 & 0 & -1 \\
\end{pmatrix}
\implies \det(-A) = (4)(-1)(-1) = 4
$$

All four direct calculations match the values obtained via determinant properties.
