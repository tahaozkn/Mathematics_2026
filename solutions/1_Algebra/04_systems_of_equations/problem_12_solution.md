### Exercise 12. Homogeneous System

## Question

Solve

$$
\begin{cases}
x + 2y - z = 0, \\
2x + 4y - 2z = 0, \\
x - y + 2z = 0.
\end{cases}
$$

Give all solutions in parametric form and explain why $(0, 0, 0)$ always satisfies a homogeneous system.

## Solution

1. **Set up the Augmented Matrix:**
   Write the homogeneous system in augmented matrix form:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
2 & 4 & -2 & \mid & 0 \\
1 & -1 & 2 & \mid & 0 \\
\end{pmatrix}
$$

2. **Gaussian Elimination:**
   Eliminate $x$ from the second and third rows using the row operations $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
0 & -3 & 3 & \mid & 0 \\
\end{pmatrix}
$$

   Swap Row 2 and Row 3 ($R_2 \leftrightarrow R_3$) and scale the new Row 2 using $R_2 \leftarrow -\frac{1}{3}R_2$:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & 1 & -1 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

   Eliminate $y$ from the first row using $R_1 \leftarrow R_1 - 2R_2$ to obtain Reduced Row Echelon Form (RREF):

$$
\begin{pmatrix}
1 & 0 & 1 & \mid & 0 \\
0 & 1 & -1 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

3. **Identify Pivot and Free Variables:**
   - Leading $1$s appear in columns 1 and 2, so $x$ and $y$ are **pivot (basic) variables**.
   - Column 3 has no pivot, so **$z$ is a free variable**. Let $z = t$, where $t \in \mathbb{R}$.

4. **Parametric Form of All Solutions:**
   Rewriting the non-zero rows as linear equations:

$$
\begin{cases}
x + z = 0, \\
y - z = 0.
\end{cases}
$$

   Solving for $x$ and $y$ in terms of $t$:

$$
x = -t, \quad y = t, \quad z = t
$$

   In vector parametric form, all solutions are given by:

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
= t \begin{pmatrix}
-1 \\
1 \\
1 \\
\end{pmatrix}, \quad t \in \mathbb{R}
$$

5. **Why $(0, 0, 0)$ Always Satisfies a Homogeneous System:**
   In any homogeneous system of linear equations, every equation has the form

$$
a_{i1}x_1 + a_{i2}x_2 + \dots + a_{in}x_n = 0
$$

   where the right-hand side is strictly $0$ and there is no non-zero constant term. Substituting $(x_1, x_2, \dots, x_n) = (0, 0, \dots, 0)$ evaluates the left-hand side of every equation to

$$
a_{i1}(0) + a_{i2}(0) + \dots + a_{in}(0) = 0 + 0 + \dots + 0 = 0
$$

   which matches the right-hand side identically regardless of the coefficients $a_{ij}$. In matrix notation $A\mathbf{x} = \mathbf{0}$, multiplying any matrix $A$ by the zero vector $\mathbf{0}$ always yields $A\mathbf{0} = \mathbf{0}$. Consequently, every homogeneous system is guaranteed to be consistent and possesses at least the trivial solution $(0, 0, 0)$ (corresponding to $t = 0$ in the parametric solution above).

## Verification

Choose $t = 3$ to obtain a non-trivial sample solution $(x, y, z) = (-3, 3, 3)$ and substitute it into all three original equations:

- **First equation:** $(-3) + 2(3) - 3 = -3 + 6 - 3 = 0$ (Matches $0$)
- **Second equation:** $2(-3) + 4(3) - 2(3) = -6 + 12 - 6 = 0$ (Matches $0$)
- **Third equation:** $(-3) - 3 + 2(3) = -3 - 3 + 6 = 0$ (Matches $0$)

Additionally, substituting $(x, y, z) = (0, 0, 0)$ satisfies $0 = 0$ in all three equations, confirming the parametric solution set.
