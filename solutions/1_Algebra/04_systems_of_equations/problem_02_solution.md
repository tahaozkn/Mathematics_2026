### Exercise 2. Gaussian Elimination — One Solution

## Question

Solve using Gaussian elimination:

$$
\begin{cases}
x + y + z = 6, \\
2x - y + z = 3, \\
x + 2y - z = 2.
\end{cases}
$$

After solving, substitute the result into all equations and check consistency.

## Solution

1. **Set up the Augmented Matrix:**
   Write the system in augmented matrix form $[A \mid \mathbf{b}]$:

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
2 & -1 & 1 & 3 \\
1 & 2 & -1 & 2 \\
\end{array}\right)
$$

2. **Forward Elimination (Row Echelon Form):**
   Eliminate $x$ from the second and third rows using the first row as the pivot ($R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$):

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & -3 & -1 & -9 \\
0 & 1 & -2 & -4 \\
\end{array}\right)
$$

   Swap Row 2 and Row 3 ($R_2 \leftrightarrow R_3$) to get a leading $1$ in the second row:

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & -2 & -4 \\
0 & -3 & -1 & -9 \\
\end{array}\right)
$$

   Eliminate $y$ from the third row ($R_3 \leftarrow R_3 + 3R_2$):

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & -2 & -4 \\
0 & 0 & -7 & -21 \\
\end{array}\right)
$$

   Scale the third row to obtain a leading $1$ ($R_3 \leftarrow -\frac{1}{7}R_3$):

$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & -2 & -4 \\
0 & 0 & 1 & 3 \\
\end{array}\right)
$$

3. **Back-Substitution:**
   Rewriting the row echelon form as a system of equations:

$$
\begin{cases}
x + y + z = 6, \\
y - 2z = -4, \\
z = 3.
\end{cases}
$$

   - From the third equation:
     $$
     z = 3
     $$

   - Substitute $z = 3$ into the second equation:
     $$
     y - 2(3) = -4 \implies y - 6 = -4 \implies y = 2
     $$

   - Substitute $y = 2$ and $z = 3$ into the first equation:
     $$
     x + 2 + 3 = 6 \implies x + 5 = 6 \implies x = 1
     $$

   Thus, the unique solution is:

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
= \begin{pmatrix}
1 \\
2 \\
3 \\
\end{pmatrix}
$$

## Verification

Substitute $(x, y, z) = (1, 2, 3)$ into each equation of the original system to verify consistency:

- **First equation:**
  $$
  1 + 2 + 3 = 6 \quad (\text{Matches } 6)
  $$

- **Second equation:**
  $$
  2(1) - 2 + 3 = 2 - 2 + 3 = 3 \quad (\text{Matches } 3)
  $$

- **Third equation:**
  $$
  1 + 2(2) - 3 = 1 + 4 - 3 = 2 \quad (\text{Matches } 2)
  $$

All three equations are satisfied identically, confirming that $(x, y, z) = (1, 2, 3)$ is the consistent, unique solution to the system.
