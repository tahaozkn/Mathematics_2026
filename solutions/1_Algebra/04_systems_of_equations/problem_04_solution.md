### Exercise 4. Infinitely Many Solutions

## Question

Solve

$$
\begin{cases}
x + y + z = 2, \\
2x + 2y + 2z = 4, \\
x - y + z = 0.
\end{cases}
$$

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

## Solution

1. **Set up the Augmented Matrix:**
   Write the system in augmented matrix form $[A \mid \mathbf{b}]$:

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
2 & 2 & 2 & 4 \\
1 & -1 & 1 & 0 \\
\end{array}\right)
$$

2. **Gaussian Elimination:**
   Eliminate $x$ from the second and third rows ($R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$):

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
0 & 0 & 0 & 0 \\
0 & -2 & 0 & -2 \\
\end{array}\right)
$$

   Swap Row 2 and Row 3 ($R_2 \leftrightarrow R_3$) and scale the new Row 2 ($R_2 \leftarrow -\frac{1}{2}R_2$):

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
0 & 1 & 0 & 1 \\
0 & 0 & 0 & 0 \\
\end{array}\right)
$$

   Eliminate $y$ from the first row ($R_1 \leftarrow R_1 - R_2$) to obtain Reduced Row Echelon Form (RREF):

$$
\left(\begin{array}{ccc|c}
1 & 0 & 1 & 1 \\
0 & 1 & 0 & 1 \\
0 & 0 & 0 & 0 \\
\end{array}\right)
$$

3. **Identify Pivot and Free Variables:**
   - The leading $1$s appear in columns 1 and 2, so $x$ and $y$ are **pivot (basic) variables**.
   - Column 3 has no pivot, so **$z$ is a free variable**. Let $z = t$, where $t \in \mathbb{R}$ is an arbitrary real parameter.

4. **Parametric Form of the Solution:**
   Rewriting the RREF matrix as a system of equations:

$$
\begin{cases}
x + z = 1, \\
y = 1, \\
0 = 0.
\end{cases}
$$

   Expressing $x$ and $y$ in terms of $t$:
   - $x = 1 - t$
   - $y = 1$
   - $z = t$

   In vector parametric form, the solution set is:

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
= \begin{pmatrix}
1 \\
1 \\
0 \\
\end{pmatrix}
+ t \begin{pmatrix}
-1 \\
0 \\
1 \\
\end{pmatrix}, \quad t \in \mathbb{R}
$$

## Verification

Choose the parameter value $t = 2$. Substituting $t = 2$ into the parametric form gives the specific point:

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
= \begin{pmatrix}
1 - 2 \\
1 \\
2 \\
\end{pmatrix}
= \begin{pmatrix}
-1 \\
1 \\
2 \\
\end{pmatrix}
$$

Substitute $(x, y, z) = (-1, 1, 2)$ into all three original equations to verify consistency:

- **First equation:**
  $$
  (-1) + 1 + 2 = 2 \quad (\text{Matches } 2)
  $$

- **Second equation:**
  $$
  2(-1) + 2(1) + 2(2) = -2 + 2 + 4 = 4 \quad (\text{Matches } 4)
  $$

- **Third equation:**
  $$
  (-1) - 1 + 2 = 0 \quad (\text{Matches } 0)
  $$

All three equations hold identically, confirming that the parametric solution accurately describes the infinite solution set.
