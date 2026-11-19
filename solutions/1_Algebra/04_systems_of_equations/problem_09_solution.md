### Exercise 9. A System from a Sum Condition

## Question

Find numbers $x, y$ satisfying

$$
\begin{cases}
x + y = 10, \\
2x + 5y = 32.
\end{cases}
$$

Solve the system and explain geometrically why the solution is unique.

## Solution

1. **Set up the Augmented Matrix:**
   Write the system in augmented matrix form:

$$
\begin{pmatrix}
1 & 1 & \mid & 10 \\
2 & 5 & \mid & 32 \\
\end{pmatrix}
$$

2. **Gaussian Elimination:**
   Eliminate $x$ from the second row using the row operation $R_2 \leftarrow R_2 - 2R_1$:

$$
\begin{pmatrix}
1 & 1 & \mid & 10 \\
2 - 2(1) & 5 - 2(1) & \mid & 32 - 2(10) \\
\end{pmatrix}
= \begin{pmatrix}
1 & 1 & \mid & 10 \\
0 & 3 & \mid & 12 \\
\end{pmatrix}
$$

   Scale the second row using $R_2 \leftarrow \frac{1}{3}R_2$:

$$
\begin{pmatrix}
1 & 1 & \mid & 10 \\
0 & 1 & \mid & 4 \\
\end{pmatrix}
$$

3. **Back-Substitution:**
   From the second row, $y = 4$. Substitute $y = 4$ into the first equation $x + y = 10$:

$$
\begin{aligned}
x + 4 &= 10 \\
x &= 6
\end{aligned}
$$

   Thus, the numbers satisfying the system are $x = 6$ and $y = 4$, or in vector form:

$$
\begin{pmatrix}
x \\
y \\
\end{pmatrix}
= \begin{pmatrix}
6 \\
4 \\
\end{pmatrix}
$$

4. **Geometric Explanation of Uniqueness:**
   Each linear equation in two variables represents a straight line in the $xy$-plane:
   - The first equation $x + y = 10$ can be written in slope-intercept form as $y = -x + 10$, which is a line with slope $m_1 = -1$.
   - The second equation $2x + 5y = 32$ can be written as $y = -\frac{2}{5}x + \frac{32}{5}$, which is a line with slope $m_2 = -\frac{2}{5}$.

   Because the two lines have different slopes ($m_1 \neq m_2$), they are neither parallel nor coincident. In the Euclidean plane, two non-parallel lines must intersect at exactly one point. That unique intersection point is $(6, 4)$.

## Verification

Substitute $(x, y) = (6, 4)$ into both original equations:

- **First equation:** $6 + 4 = 10$ (Matches $10$)
- **Second equation:** $2(6) + 5(4) = 12 + 20 = 32$ (Matches $32$)

Both conditions hold identically, confirming that $(6, 4)$ is the unique solution.
