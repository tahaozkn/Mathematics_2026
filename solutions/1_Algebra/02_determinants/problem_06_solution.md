### Exercise 6. Parameter and Invertibility

## Question

For

$$
A(t) =
\begin{pmatrix}
t & 1 \\
2 & t \\
\end{pmatrix}
$$

find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

## Solution

A square matrix is not invertible (singular) if and only if its determinant equals zero. First, compute the determinant of $A(t)$:

$$
\det A(t) = (t)(t) - (1)(2) = t^2 - 2
$$

Setting the determinant equal to zero gives the equation:

$$
t^2 - 2 = 0
$$

Solving for $t$:

$$
t^2 = 2 \implies t = \pm\sqrt{2}
$$

Thus, the matrix $A(t)$ is not invertible when **$t = \sqrt{2}$** or **$t = -\sqrt{2}$**.

**Relation to the determinant being zero:**
When $\det A(t) = 0$, the rows (and columns) of $A(t)$ become linearly dependent—specifically, one row is a scalar multiple of the other. Geometrically, the linear transformation represented by $A(t)$ collapses the $2$-dimensional plane onto a $1$-dimensional line (reducing the area scaling factor to zero). Because distinct input vectors map to the same output vector along that line, the transformation cannot be uniquely reversed, meaning no inverse matrix $A(t)^{-1}$ exists.

## Verification

We can verify that $A(t)$ is singular at $t = \sqrt{2}$ and $t = -\sqrt{2}$ by substituting both values into the matrix and checking for linear dependence between the rows.

1. **For $t = \sqrt{2}$:**

$$
A(\sqrt{2}) =
\begin{pmatrix}
\sqrt{2} & 1 \\
2 & \sqrt{2} \\
\end{pmatrix}
$$

Multiplying the first row by $\sqrt{2}$ gives $\sqrt{2} \begin{pmatrix} \sqrt{2} & 1 \end{pmatrix} = \begin{pmatrix} 2 & \sqrt{2} \end{pmatrix}$, which is identical to the second row. Performing $R_2 \leftarrow R_2 - \sqrt{2}R_1$ yields a row of zeros:

$$
\begin{pmatrix}
\sqrt{2} & 1 \\
0 & 0 \\
\end{pmatrix}
$$

2. **For $t = -\sqrt{2}$:**

$$
A(-\sqrt{2}) =
\begin{pmatrix}
-\sqrt{2} & 1 \\
2 & -\sqrt{2} \\
\end{pmatrix}
$$

Multiplying the first row by $-\sqrt{2}$ gives $-\sqrt{2} \begin{pmatrix} -\sqrt{2} & 1 \end{pmatrix} = \begin{pmatrix} 2 & -\sqrt{2} \end{pmatrix}$, which is identical to the second row. Performing $R_2 \leftarrow R_2 + \sqrt{2}R_1$ yields a row of zeros:

$$
\begin{pmatrix}
-\sqrt{2} & 1 \\
0 & 0 \\
\end{pmatrix}
$$

In both cases, row reduction leaves only one pivot, confirming that $A(t)$ is not invertible precisely at $t = \pm\sqrt{2}$.
