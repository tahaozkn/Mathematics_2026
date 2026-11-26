### Exercise 1. Line Through Two Points

## Question

Find the equation of the line through $A = (1, 2)$ and $B = (4, -1)$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

## Solution

1. **Find a Direction Vector:**
   A direction vector $\mathbf{v}$ parallel to the line is given by the displacement vector from point $A$ to point $B$:

$$
\mathbf{v} = \overrightarrow{AB} = B - A = \begin{pmatrix}
4 - 1 \\
-1 - 2 \\
\end{pmatrix}
= \begin{pmatrix}
3 \\
-3 \\
\end{pmatrix}
$$

   *(Note: Any non-zero scalar multiple of $\mathbf{v}$, such as $\mathbf{v}_0 = \frac{1}{3}\mathbf{v} = \begin{pmatrix} 1 \\ -1 \end{pmatrix}$, is also a valid direction vector for the same line.)*

2. **Parametric Form of the Line:**
   Using point $A = (1, 2)$ as the base point and $\mathbf{v} = \begin{pmatrix} 3 \\ -3 \end{pmatrix}$ as the direction vector, every point $(x, y)$ on the line is described by $\mathbf{r}(t) = \mathbf{r}_A + t\mathbf{v}$ for $t \in \mathbb{R}$:

$$
\begin{pmatrix}
x \\
y \\
\end{pmatrix}
= \begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
+ t \begin{pmatrix}
3 \\
-3 \\
\end{pmatrix}
$$

   Writing out each coordinate component separately gives the parametric equations:

$$
\begin{cases}
x = 1 + 3t \\
y = 2 - 3t
\end{cases}, \quad t \in \mathbb{R}
$$

3. **General Form of the Line ($ax + by + c = 0$):**
   Eliminate the parameter $t$ by adding the two parametric equations together:

$$
\begin{aligned}
x + y &= (1 + 3t) + (2 - 3t) \\
x + y &= 3 \\
x + y - 3 &= 0
\end{aligned}
$$

   Thus, the general form of the line is:

$$
x + y - 3 = 0
$$

4. **Identify an Example of a Normal Vector:**
   In the general form $ax + by + c = 0$, the coefficients $(a, b)$ directly form a normal vector $\mathbf{n}$ perpendicular to the line. From $1x + 1y - 3 = 0$, we read off:

$$
\mathbf{n} = \begin{pmatrix}
1 \\
1 \\
\end{pmatrix}
$$

   *(We can confirm orthogonality with the direction vector via the dot product: $\mathbf{n} \cdot \mathbf{v} = 1(3) + 1(-3) = 3 - 3 = 0$.)*

## Verification

1. **Check Both Points in the General Form ($x + y - 3 = 0$):**
   - **Substitute $A = (1, 2)$:**

$$
1 + 2 - 3 = 0 \implies 0 = 0
$$

   - **Substitute $B = (4, -1)$:**

$$
4 + (-1) - 3 = 0 \implies 0 = 0
$$

   Both points satisfy the general equation.

2. **Check Both Points in the Parametric Form:**
   - **At $t = 0$:**

$$
\begin{cases}
x = 1 + 3(0) = 1 \\
y = 2 - 3(0) = 2
\end{cases}
\implies (x, y) = (1, 2) = A
$$

   - **At $t = 1$:**

$$
\begin{cases}
x = 1 + 3(1) = 4 \\
y = 2 - 3(1) = -1
\end{cases}
\implies (x, y) = (4, -1) = B
$$

Both representations accurately describe the line passing through $A$ and $B$.
