### Exercise 4. Plane Through Three Points

## Question

Find the equation of the plane through

$$
A = (1, 0, 0), \quad B = (0, 1, 0), \quad C = (0, 0, 1).
$$

First construct two vectors lying in the plane, and then use the cross product. Check the resulting equation on all three points.

## Solution

1. **Construct Two Vectors Lying in the Plane:**
   Using point $A = (1, 0, 0)$ as a common initial point, form two displacement vectors connecting $A$ to $B$ and $A$ to $C$:

$$
\mathbf{u} = \overrightarrow{AB} = B - A = \begin{pmatrix}
0 - 1 \\
1 - 0 \\
0 - 0 \\
\end{pmatrix}
= \begin{pmatrix}
-1 \\
1 \\
0 \\
\end{pmatrix}
$$

$$
\mathbf{v} = \overrightarrow{AC} = C - A = \begin{pmatrix}
0 - 1 \\
0 - 0 \\
1 - 0 \\
\end{pmatrix}
= \begin{pmatrix}
-1 \\
0 \\
1 \\
\end{pmatrix}
$$

   Since $\mathbf{u}$ and $\mathbf{v}$ are not scalar multiples of one another, they are linearly independent and span the plane.

2. **Find a Normal Vector Using the Cross Product:**
   The cross product $\mathbf{n} = \mathbf{u} \times \mathbf{v}$ produces a vector perpendicular to both $\mathbf{u}$ and $\mathbf{v}$, and therefore normal to the plane:

$$
\begin{aligned}
\mathbf{n} = \mathbf{u} \times \mathbf{v} &= \begin{pmatrix}
-1 \\
1 \\
0 \\
\end{pmatrix}
\times
\begin{pmatrix}
-1 \\
0 \\
1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
(1)(1) - (0)(0) \\
(0)(-1) - (-1)(1) \\
(-1)(0) - (1)(-1) \\
\end{pmatrix} \\
&= \begin{pmatrix}
1 - 0 \\
0 + 1 \\
0 + 1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1 \\
1 \\
1 \\
\end{pmatrix}
\end{aligned}
$$

3. **Write the Equation of the Plane:**
   Substitute the normal vector $\mathbf{n} = \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix}$ and point $A = (1, 0, 0)$ into the point-normal form $a(x - x_0) + b(y - y_0) + c(z - z_0) = 0$:

$$
\begin{aligned}
1(x - 1) + 1(y - 0) + 1(z - 0) &= 0 \\
x - 1 + y + z &= 0 \\
x + y + z - 1 &= 0
\end{aligned}
$$

   Thus, the equation of the plane is:

$$
x + y + z - 1 = 0 \quad (\text{or } x + y + z = 1)
$$

## Verification

1. **Check That All Three Points Satisfy $x + y + z - 1 = 0$:**
   - **Point $A = (1, 0, 0)$:**

$$
1 + 0 + 0 - 1 = 0 \implies 0 = 0
$$

   - **Point $B = (0, 1, 0)$:**

$$
0 + 1 + 0 - 1 = 0 \implies 0 = 0
$$

   - **Point $C = (0, 0, 1)$:**

$$
0 + 0 + 1 - 1 = 0 \implies 0 = 0
$$

2. **Check Orthogonality of $\mathbf{n}$ with Both In-Plane Vectors:**

$$
\mathbf{n} \cdot \mathbf{u} = 1(-1) + 1(1) + 1(0) = -1 + 1 + 0 = 0
$$

$$
\mathbf{n} \cdot \mathbf{v} = 1(-1) + 1(0) + 1(1) = -1 + 0 + 1 = 0
$$

All three points lie on the plane and the normal vector is confirmed orthogonal to the plane.
