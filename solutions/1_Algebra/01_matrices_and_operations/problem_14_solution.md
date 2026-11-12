### Exercise 14. Rotation Matrices

## Question

The matrix for a rotation through an angle $\theta$ is

$$
R(\theta) = \begin{pmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta \\
\end{pmatrix}
$$

Compute $R(\alpha)R(\beta)$ and, using the angle-sum formulas for sine and cosine, show that $R(\alpha)R(\beta) = R(\alpha+\beta)$. Explain the result geometrically.

## Solution

1. **Computing the Matrix Product $R(\alpha)R(\beta)$:**

$$
R(\alpha)R(\beta) = \begin{pmatrix}
\cos\alpha & -\sin\alpha \\
\sin\alpha & \cos\alpha \\
\end{pmatrix}
\begin{pmatrix}
\cos\beta & -\sin\beta \\
\sin\beta & \cos\beta \\
\end{pmatrix}
$$

Using row-column matrix multiplication, we compute each entry of the resulting matrix:

- **Top-left entry:**
$$
(\cos\alpha)(\cos\beta) + (-\sin\alpha)(\sin\beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta
$$

- **Top-right entry:**
$$
(\cos\alpha)(-\sin\beta) + (-\sin\alpha)(\cos\beta) = -(\sin\alpha\cos\beta + \cos\alpha\sin\beta)
$$

- **Bottom-left entry:**
$$
(\sin\alpha)(\cos\beta) + (\cos\alpha)(\sin\beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta
$$

- **Bottom-right entry:**
$$
(\sin\alpha)(-\sin\beta) + (\cos\alpha)(\cos\beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta
$$

2. **Applying Angle-Sum Formulas:**
   Using the standard trigonometric angle-sum identities:
   - $\cos(\alpha + \beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$
   - $\sin(\alpha + \beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$

   Substituting these identities back into the matrix yields:

$$
R(\alpha)R(\beta) = \begin{pmatrix}
\cos(\alpha + \beta) & -\sin(\alpha + \beta) \\
\sin(\alpha + \beta) & \cos(\alpha + \beta) \\
\end{pmatrix}
= R(\alpha + \beta)
$$

## Geometric Explanation

Geometrically, the product of two rotation matrices $R(\alpha)R(\beta)$ corresponds to the **composition of two successive rotations** about the origin: first rotating by an angle $\beta$, and then subsequently rotating by an angle $\alpha$. 

Applying these two consecutive rotations is equivalent to performing a single, direct rotation by the sum of the two angles, $\alpha + \beta$. This demonstrates the direct consistency between algebraic matrix multiplication and the underlying geometry of spatial rotations.
