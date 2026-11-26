### Exercise 3. Plane Through a Point with a Given Normal Vector

## Question

Find the equation of the plane through $P = (1, -2, 3)$ and perpendicular to $\mathbf{n} = (2, 1, -1)$. Check the result by substituting the point $P$ and explain the role of the normal vector.

## Solution

1. **Set Up the Point-Normal Equation of the Plane:**
   A plane passing through a known point $P = (x_0, y_0, z_0)$ with a non-zero normal vector $\mathbf{n} = \begin{pmatrix} a \\ b \\ c \end{pmatrix}$ consists of all points $X = (x, y, z)$ such that the displacement vector $\overrightarrow{PX}$ is perpendicular (orthogonal) to $\mathbf{n}$:

$$
\mathbf{n} \cdot \overrightarrow{PX} = 0
$$

   Expanding the dot product in coordinates gives the point-normal form:

$$
a(x - x_0) + b(y - y_0) + c(z - z_0) = 0
$$

2. **Substitute the Given Point $P = (1, -2, 3)$ and Normal Vector $\mathbf{n} = (2, 1, -1)$:**

$$
2(x - 1) + 1(y - (-2)) + (-1)(z - 3) = 0
$$

   Simplify the signs inside the parentheses:

$$
2(x - 1) + (y + 2) - (z - 3) = 0
$$

3. **Expand and Simplify to General Form ($ax + by + cz + d = 0$):**

$$
\begin{aligned}
2x - 2 + y + 2 - z + 3 &= 0 \\
2x + y - z + 3 &= 0
\end{aligned}
$$

   Thus, the equation of the plane in general form is:

$$
2x + y - z + 3 = 0 \quad (\text{or } 2x + y - z = -3)
$$

4. **Explain the Role of the Normal Vector:**
   - **Defining Orientation in Space:** In $\mathbb{R}^3$, specifying a single direction vector only determines a line, because infinitely many planes can rotate around that line. Specifying a **normal vector** $\mathbf{n}$ uniquely fixes the tilt (orientation) of the plane: the plane is the unique flat surface completely perpendicular to $\mathbf{n}$.
   - **Algebraic Constraint via Orthogonality:** For any two points $P$ and $X$ lying on the plane, the vector $\overrightarrow{PX}$ connecting them lies entirely *inside* the plane. Because $\mathbf{n}$ is perpendicular to the entire plane, $\mathbf{n}$ must be orthogonal to every vector inside the plane ($\mathbf{n} \cdot \overrightarrow{PX} = 0$). This single dot-product condition translates geometric perpendicularity directly into the linear equation $ax + by + cz + d = 0$, where the components $(a, b, c)$ of $\mathbf{n}$ appear directly as the coefficients of $x$, $y$, and $z$.

## Verification

1. **Substitute $P = (1, -2, 3)$ into the Plane Equation ($2x + y - z + 3 = 0$):**

$$
\begin{aligned}
2(1) + (-2) - (3) + 3 &= 2 - 2 - 3 + 3 \\
&= 0
\end{aligned}
$$

   Since the left-hand side equals $0$, the point $P$ lies on the plane.

2. **Check Orthogonality with a Second Point on the Plane:**
   Choose another point satisfying $2x + y - z + 3 = 0$, such as $Q = (0, 0, 3)$ (since $2(0) + 0 - 3 + 3 = 0$). Compute the in-plane displacement vector $\overrightarrow{PQ}$ and take its dot product with $\mathbf{n}$:

$$
\overrightarrow{PQ} = Q - P = \begin{pmatrix}
0 - 1 \\
0 - (-2) \\
3 - 3 \\
\end{pmatrix}
= \begin{pmatrix}
-1 \\
2 \\
0 \\
\end{pmatrix}
$$

$$
\mathbf{n} \cdot \overrightarrow{PQ} = \begin{pmatrix}
2 \\
1 \\
-1 \\
\end{pmatrix}
\cdot
\begin{pmatrix}
-1 \\
2 \\
0 \\
\end{pmatrix}
= 2(-1) + 1(2) + (-1)(0) = -2 + 2 + 0 = 0
$$

Since $\mathbf{n} \cdot \overrightarrow{PQ} = 0$, the vector $\mathbf{n}$ is confirmed to be perpendicular to the plane.
