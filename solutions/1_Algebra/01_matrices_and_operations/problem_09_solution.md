### Exercise 9. Composing Transformations

## Question

Let

$$
S =
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},
\qquad
R =
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
$$

The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation. For

$$
x =
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
$$

compute $RSx$ and $SRx$. Compare the results and explain geometrically why the order of these transformations matters.

## Solution

We evaluate the compositions by applying the transformations step by step.

**For $RSx$:**
First, apply $S$ to $x$:

$$
Sx =
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
=
\begin{pmatrix}
2\cdot 1 + 0\cdot 2 \\
0\cdot 1 + 1\cdot 2 \\
\end{pmatrix}
=
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix}
$$

Next, apply $R$ to the resulting vector:

$$
RSx =
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix}
=
\begin{pmatrix}
0\cdot 2 + (-1)\cdot 2 \\
1\cdot 2 + 0\cdot 2 \\
\end{pmatrix}
=
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
$$

**For $SRx$:**
First, apply $R$ to $x$:

$$
Rx =
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
=
\begin{pmatrix}
0\cdot 1 + (-1)\cdot 2 \\
1\cdot 1 + 0\cdot 2 \\
\end{pmatrix}
=
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}
$$

Next, apply $S$ to the resulting vector:

$$
SRx =
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}
=
\begin{pmatrix}
2\cdot (-2) + 0\cdot 1 \\
0\cdot (-2) + 1\cdot 1 \\
\end{pmatrix}
=
\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}
$$

Comparing the results, $RSx = \begin{pmatrix} -2 \\ 2 \end{pmatrix}$ and $SRx = \begin{pmatrix} -4 \\ 1 \end{pmatrix}$, so **$RSx \neq SRx$**.

**Geometric explanation:** 
Matrix multiplication corresponds to the composition of linear transformations. In $RSx$, the vector $x$ is first stretched horizontally by a factor of $2$ (scaling along the coordinate axes) and then rotated by $90^\circ$ counterclockwise. In $SRx$, the order is reversed: the vector is first rotated by $90^\circ$ counterclockwise (which rotates the horizontal axis to the vertical axis), and then scaled. Because stretching is axis-aligned, rotating *before* scaling stretches a different spatial direction than scaling *before* rotating, making the final outcome order-dependent.

## Verification

We can verify these results independently by first computing the composite transformation matrices $RS$ and $SR$, and then multiplying them by $x$.

For the product matrix $RS$:

$$
RS =
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
=
\begin{pmatrix}
0\cdot 2 + (-1)\cdot 0 & 0\cdot 0 + (-1)\cdot 1 \\
1\cdot 2 + 0\cdot 0 & 1\cdot 0 + 0\cdot 1 \\
\end{pmatrix}
=
\begin{pmatrix}
0 & -1 \\
2 & 0 \\
\end{pmatrix}
$$

Multiplying $RS$ by $x$:

$$
(RS)x =
\begin{pmatrix}
0 & -1 \\
2 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
=
\begin{pmatrix}
0\cdot 1 + (-1)\cdot 2 \\
2\cdot 1 + 0\cdot 2 \\
\end{pmatrix}
=
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
$$

For the product matrix $SR$:

$$
SR =
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
=
\begin{pmatrix}
2\cdot 0 + 0\cdot 1 & 2\cdot (-1) + 0\cdot 0 \\
0\cdot 0 + 1\cdot 1 & 0\cdot (-1) + 1\cdot 0 \\
\end{pmatrix}
=
\begin{pmatrix}
0 & -2 \\
1 & 0 \\
\end{pmatrix}
$$

Multiplying $SR$ by $x$:

$$
(SR)x =
\begin{pmatrix}
0 & -2 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
=
\begin{pmatrix}
0\cdot 1 + (-2)\cdot 2 \\
1\cdot 1 + 0\cdot 2 \\
\end{pmatrix}
=
\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}
$$

Both methods yield identical results, confirming the calculations and verifying the noncommutativity of the transformation composition.
