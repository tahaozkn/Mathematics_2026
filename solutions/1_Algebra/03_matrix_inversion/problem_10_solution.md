### Exercise 10. Inverse of a Diagonal Matrix

## Question

Given

$$
D = \begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}, \quad
E = \begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}.
$$

Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

## Solution

1. **Determine Invertibility from Diagonal Structure:**
   - **Determinant of a Diagonal Matrix:** The determinant of any diagonal matrix is the product of its main diagonal entries.
   - **For matrix $D$:**

$$
\det D = (2)(-3)(5) = -30
$$

     Since $\det D = -30 \neq 0$ (all main diagonal entries are non-zero), **$D$ is invertible**.
   - **For matrix $E$:**

$$
\det E = (2)(0)(5) = 0
$$

     Since $\det E = 0$ (it contains a zero on the main diagonal, creating an entire row and column of zeros), **$E$ is not invertible** (singular).

2. **Find the Inverse of $D$:**
   A diagonal matrix acts on a vector by independently scaling each coordinate by its corresponding diagonal entry:

$$
D \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 2x \\ -3y \\ 5z \end{pmatrix}
$$

   To undo each independent scaling, we simply take the **multiplicative inverse (reciprocal)** of each non-zero diagonal entry while keeping all off-diagonal entries equal to $0$:

$$
D^{-1} = \begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5} \\
\end{pmatrix}
$$

## Verification

Check the result by computing both products $DD^{-1}$ and $D^{-1}D$:

- **Right inverse check ($DD^{-1}$):**

$$
\begin{aligned}
DD^{-1} &= \begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5} \\
\end{pmatrix} \\
&= \begin{pmatrix}
2\left(\frac{1}{2}\right) & 0 & 0 \\
0 & (-3)\left(-\frac{1}{3}\right) & 0 \\
0 & 0 & 5\left(\frac{1}{5}\right) \\
\end{pmatrix} \\
&= \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix} \\
&= I
\end{aligned}
$$

- **Left inverse check ($D^{-1}D$):**

$$
\begin{aligned}
D^{-1}D &= \begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5} \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix} \\
&= \begin{pmatrix}
\left(\frac{1}{2}\right)2 & 0 & 0 \\
0 & \left(-\frac{1}{3}\right)(-3) & 0 \\
0 & 0 & \left(\frac{1}{5}\right)5 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix} \\
&= I
\end{aligned}
$$

Since $DD^{-1} = D^{-1}D = I$, the inverse matrix $D^{-1}$ is verified.
