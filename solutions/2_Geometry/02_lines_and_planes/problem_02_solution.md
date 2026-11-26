### Exercise 2. A Line in Space

## Question

Given

$$
L : (x, y, z) = (2, -1, 3) + t(1, 2, -2).
$$

State a point on the line and its direction vector, check whether $P = (4, 3, -1)$ lies on $L$, and find the point corresponding to $t = -1$.

## Solution

1. **Identify a Point on the Line and Its Direction Vector:**
   Comparing the given equation with the standard vector parametric form $\mathbf{r}(t) = \mathbf{r}_0 + t\mathbf{v}$:
   - **Base Point ($t = 0$):**

$$
P_0 = (2, -1, 3)
$$

   - **Direction Vector:**

$$
\mathbf{v} = \begin{pmatrix}
1 \\
2 \\
-2 \\
\end{pmatrix}
$$

2. **Check Whether $P = (4, 3, -1)$ Lies on $L$:**
   Write the line as a system of three scalar parametric equations:

$$
\begin{cases}
x = 2 + t \\
y = -1 + 2t \\
z = 3 - 2t
\end{cases}
$$

   Point $P = (4, 3, -1)$ lies on $L$ if and only if there exists a **single** parameter value $t \in \mathbb{R}$ that satisfies all three coordinate equations simultaneously:
   - **From the $x$-coordinate:**

$$
2 + t = 4 \implies t = 2
$$

   - **From the $y$-coordinate:**

$$
-1 + 2t = 3 \implies 2t = 4 \implies t = 2
$$

   - **From the $z$-coordinate:**

$$
3 - 2t = -1 \implies -2t = -4 \implies t = 2
$$

   Since all three equations yield the exact same parameter value $t = 2$, the point **$P = (4, 3, -1)$ lies on $L$**.

3. **Find the Point Corresponding to $t = -1$:**
   Substitute $t = -1$ into the parametric equation of the line:

$$
\begin{aligned}
(x, y, z) &= (2, -1, 3) + (-1)(1, 2, -2) \\
&= (2 - 1, \, -1 - 2, \, 3 + 2) \\
&= (1, -3, 5)
\end{aligned}
$$

   Thus, the point on $L$ corresponding to $t = -1$ is $Q = (1, -3, 5)$.

## Verification

We can verify that both $P = (4, 3, -1)$ and $Q = (1, -3, 5)$ lie on $L$ by checking that their displacement vectors from the base point $P_0 = (2, -1, 3)$ are scalar multiples of the direction vector $\mathbf{v} = \begin{pmatrix} 1 \\ 2 \\ -2 \end{pmatrix}$:

1. **Check $\overrightarrow{P_0P}$:**

$$
\overrightarrow{P_0P} = P - P_0 = \begin{pmatrix}
4 - 2 \\
3 - (-1) \\
-1 - 3 \\
\end{pmatrix}
= \begin{pmatrix}
2 \\
4 \\
-4 \\
\end{pmatrix}
= 2 \begin{pmatrix}
1 \\
2 \\
-2 \\
\end{pmatrix}
= 2\mathbf{v}
$$

   Since $\overrightarrow{P_0P} = 2\mathbf{v}$, $P$ is confirmed to lie on $L$ at $t = 2$.

2. **Check $\overrightarrow{P_0Q}$:**

$$
\overrightarrow{P_0Q} = Q - P_0 = \begin{pmatrix}
1 - 2 \\
-3 - (-1) \\
5 - 3 \\
\end{pmatrix}
= \begin{pmatrix}
-1 \\
-2 \\
2 \\
\end{pmatrix}
= (-1) \begin{pmatrix}
1 \\
2 \\
-2 \\
\end{pmatrix}
= -\mathbf{v}
$$

   Since $\overrightarrow{P_0Q} = -\mathbf{v}$, $Q = (1, -3, 5)$ is confirmed to be the point at $t = -1$.
