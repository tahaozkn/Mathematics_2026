### Exercise 3. Inconsistent System

## Question

Solve or show that the system is inconsistent:

$$
\begin{cases}
x + 2y = 3, \\
2x + 4y = 7.
\end{cases}
$$

Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

## Solution

1. **Set up the Augmented Matrix:**
   Write the system in augmented matrix form $[A \mid \mathbf{b}]$:

$$
\left(\begin{array}{cc|c}
1 & 2 & 3 \\
2 & 4 & 7 \\
\end{array}\right)
$$

2. **Gaussian Elimination:**
   Eliminate $x$ from the second row using the row operation $R_2 \leftarrow R_2 - 2R_1$:

$$
\left(\begin{array}{cc|c}
1 & 2 & 3 \\
2 - 2(1) & 4 - 2(2) & 7 - 2(3) \\
\end{array}\right)
= \left(\begin{array}{cc|c}
1 & 2 & 3 \\
0 & 0 & 1 \\
\end{array}\right)
$$

3. **Identifying the Contradiction:**
   After elimination, the second row of the augmented matrix is:

$$
\begin{pmatrix}
0 & 0 & \mid & 1 \\
\end{pmatrix}
$$

   Translating this row back into a linear equation yields:

$$
0x + 0y = 1 \implies 0 = 1
$$

4. **Interpretation:**
   Because $0 = 1$ is a false statement (a mathematical contradiction), no values of $x$ and $y$ can simultaneously satisfy both equations. Geometrically, the two equations represent parallel lines ($y = -\frac{1}{2}x + \frac{3}{2}$ and $y = -\frac{1}{2}x + \frac{7}{4}$) that never intersect. Therefore, the system is **inconsistent** and has **no solution**.

## Verification

We verify the inconsistency algebraically by multiplying the first equation by $2$:

$$
2(x + 2y) = 2(3) \implies 2x + 4y = 6
$$

Comparing this with the second equation ($2x + 4y = 7$) requires $6 = 7$, confirming the contradiction and proving that no solution exists.
