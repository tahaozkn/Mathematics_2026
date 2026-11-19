### Exercise 13. Does Every Equation Add New Information?

## Question

Consider the system

$$
\begin{cases}
x_1 + x_2 = 10, \\
x_2 + x_3 = 8, \\
x_1 - x_3 = 2.
\end{cases}
$$

Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

## Solution

1. **Set up the Augmented Matrix:**
   Write the system in augmented matrix form with columns corresponding to $x_1$, $x_2$, and $x_3$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
1 & 0 & -1 & \mid & 2 \\
\end{pmatrix}
$$

2. **Gaussian Elimination:**
   Eliminate $x_1$ from the third row using the row operation $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
0 & -1 & -1 & \mid & -8 \\
\end{pmatrix}
$$

   Eliminate $x_2$ from the third row using $R_3 \leftarrow R_3 + R_2$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

   Eliminate $x_2$ from the first row using $R_1 \leftarrow R_1 - R_2$ to obtain Reduced Row Echelon Form (RREF):

$$
\begin{pmatrix}
1 & 0 & -1 & \mid & 2 \\
0 & 1 & 1 & \mid & 8 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

3. **Parametric Form of the Solution Set:**
   - Columns 1 and 2 contain leading $1$s, so $x_1$ and $x_2$ are **pivot (basic) variables**.
   - Column 3 has no pivot, so **$x_3$ is a free variable**. Let $x_3 = t$, where $t \in \mathbb{R}$.

   Rewriting the non-zero rows as equations gives $x_1 - x_3 = 2$ and $x_2 + x_3 = 8$. Expressing all variables in terms of $t$:

$$
x_1 = 2 + t, \quad x_2 = 8 - t, \quad x_3 = t
$$

   In vector parametric form, the solution set is:

$$
\begin{pmatrix}
x_1 \\
x_2 \\
x_3 \\
\end{pmatrix}
= \begin{pmatrix}
2 \\
8 \\
0 \\
\end{pmatrix}
+ t \begin{pmatrix}
1 \\
-1 \\
1 \\
\end{pmatrix}, \quad t \in \mathbb{R}
$$

4. **Redundancy Check:**
   No, all three equations are **not** independently necessary to describe the solution set. During row reduction, the third row became $\begin{pmatrix} 0 & 0 & 0 & \mid & 0 \end{pmatrix}$, showing that the third equation is a linear combination of the first two equations and adds no new constraint.

   Explicitly, subtracting the second equation ($E_2$) from the first equation ($E_1$) yields the third equation ($E_3$):

$$
\begin{aligned}
(x_1 + x_2) - (x_2 + x_3) &= 10 - 8 \\
x_1 + x_2 - x_2 - x_3 &= 2 \\
x_1 - x_3 &= 2
\end{aligned}
$$

   Because $E_3 = E_1 - E_2$, any triple $(x_1, x_2, x_3)$ satisfying the first two equations automatically satisfies the third equation.

## Verification

Choose a sample parameter value $t = 3$ to obtain the specific point:

$$
\begin{pmatrix}
x_1 \\
x_2 \\
x_3 \\
\end{pmatrix}
= \begin{pmatrix}
2 + 3 \\
8 - 3 \\
3 \\
\end{pmatrix}
= \begin{pmatrix}
5 \\
5 \\
3 \\
\end{pmatrix}
$$

Substitute $(x_1, x_2, x_3) = (5, 5, 3)$ into all three original equations:

- **First equation:** $5 + 5 = 10$ (Matches $10$)
- **Second equation:** $5 + 3 = 8$ (Matches $8$)
- **Third equation:** $5 - 3 = 2$ (Matches $2$)

All three equations hold identically, confirming both the parametric solution and the redundancy of the third equation.
