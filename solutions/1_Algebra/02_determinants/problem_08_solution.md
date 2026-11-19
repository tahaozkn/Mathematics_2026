### Exercise 8. Determinant of a Product

## Question

Let $A, B$ be square matrices such that $\det A = 3$ and $\det B = -5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB \neq BA$.

## Solution

1. **Compute $\det(AB)$:**
   By the multiplicative property of determinants, for any two square matrices $A$ and $B$ of the same size $n \times n$, the determinant of their product equals the product of their determinants:

$$
\det(AB) = (\det A)(\det B)
$$

   Substituting the given values $\det A = 3$ and $\det B = -5$:

$$
\det(AB) = 3 \cdot (-5) = -15
$$

2. **Compute $\det(BA)$:**
   Applying the same multiplicative property in reverse order:

$$
\det(BA) = (\det B)(\det A)
$$

   Substituting the given values:

$$
\det(BA) = (-5) \cdot 3 = -15
$$

3. **Determine Existence and Compute $\det(A^{-1}B)$:**
   - **Existence:** A square matrix $A$ is invertible if and only if $\det A \neq 0$. Since $\det A = 3 \neq 0$, the inverse matrix $A^{-1}$ exists, and consequently the product $A^{-1}B$ is well-defined.
   - **Calculation:** Using the determinant property of an inverse matrix, $\det(A^{-1}) = (\det A)^{-1} = \frac{1}{\det A}$. Applying the multiplicative property of determinants:

$$
\begin{aligned}
\det(A^{-1}B) &= \det(A^{-1}) \det B \\
              &= \frac{1}{\det A} \cdot \det B \\
              &= \frac{1}{3} \cdot (-5) \\
              &= -\frac{5}{3}
\end{aligned}
$$

4. **Why $\det(AB) = \det(BA)$ Even Though Usually $AB \neq BA$:**
   Although matrix multiplication is not commutative in general ($AB \neq BA$ as arrays of numbers), the determinant maps each $n \times n$ matrix to a single **real scalar** ($\det A, \det B \in \mathbb{R}$). Because multiplication of real numbers is commutative ($ab = ba$), we have:

$$
\det(AB) = (\det A)(\det B) = (\det B)(\det A) = \det(BA)
$$

   Geometrically, $|\det A|$ and $|\det B|$ represent the volume scaling factors of the linear transformations $A$ and $B$, while their signs indicate whether orientation is preserved ($+$) or reversed ($-$). Applying transformation $B$ followed by $A$ scales volume by $|3| \cdot |-5| = 15$ and flips orientation once, producing the exact same net volume scaling and orientation change as applying $A$ followed by $B$.

## Verification

We can verify these properties using a concrete pair of $2 \times 2$ matrices with $\det A = 3$ and $\det B = -5$, such as:

$$
A = \begin{pmatrix}
3 & 0 \\
0 & 1 \\
\end{pmatrix}, \quad
B = \begin{pmatrix}
1 & 2 \\
3 & 1 \\
\end{pmatrix}
$$

- **Verify Determinants of $A$ and $B$:**
  - $\det A = (3)(1) - (0)(0) = 3$
  - $\det B = (1)(1) - (2)(3) = 1 - 6 = -5$

- **Verify $AB \neq BA$ and $\det(AB) = \det(BA) = -15$:**

$$
AB = \begin{pmatrix}
3 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
3 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
3 & 6 \\
3 & 1 \\
\end{pmatrix}
\implies \det(AB) = (3)(1) - (6)(3) = 3 - 18 = -15
$$

$$
BA = \begin{pmatrix}
1 & 2 \\
3 & 1 \\
\end{pmatrix}
\begin{pmatrix}
3 & 0 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
3 & 2 \\
9 & 1 \\
\end{pmatrix}
\implies \det(BA) = (3)(1) - (2)(9) = 3 - 18 = -15
$$

  Notice that $AB \neq BA$, yet both determinants equal $-15$.

- **Verify $\det(A^{-1}B) = -\frac{5}{3}$:**

$$
A^{-1} = \begin{pmatrix}
\frac{1}{3} & 0 \\
0 & 1 \\
\end{pmatrix}
\implies A^{-1}B = \begin{pmatrix}
\frac{1}{3} & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
3 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{3} & \frac{2}{3} \\
3 & 1 \\
\end{pmatrix}
$$

$$
\det(A^{-1}B) = \left(\frac{1}{3}\right)(1) - \left(\frac{2}{3}\right)(3) = \frac{1}{3} - 2 = -\frac{5}{3}
$$

All results match the derived values identically.
