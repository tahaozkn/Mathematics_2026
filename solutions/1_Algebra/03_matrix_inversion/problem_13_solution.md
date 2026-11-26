### Exercise 13. Undoing a Composite Transformation

## Question

The matrices

$$
S = \begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}, \quad
H = \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

describe nonuniform scaling and shear. For $T = HS$, find $T^{-1}$ in two ways:
1. first compute $T$, then its inverse,
2. use $(HS)^{-1} = S^{-1}H^{-1}$.

Compare the results. Additionally compute $H^{-1}S^{-1}$ and verify that the incorrect order gives a different matrix. Explain the rule: “when undoing a composition of operations, we undo them from the end.”

## Solution

1. **Method 1: First Compute $T = HS$, Then Find Its Inverse $T^{-1}$**
   - **Compute the composite matrix $T = HS$:**

$$
\begin{aligned}
T &= \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1(2) + 1(0) & 1(0) + 1(1) \\
0(2) + 1(0) & 0(0) + 1(1) \\
\end{pmatrix} \\
&= \begin{pmatrix}
2 & 1 \\
0 & 1 \\
\end{pmatrix}
\end{aligned}
$$

   - **Find the determinant of $T$:**

$$
\det T = (2)(1) - (1)(0) = 2 - 0 = 2
$$

   - **Apply the $2 \times 2$ inverse formula to $T$:**

$$
\begin{aligned}
T^{-1} &= \frac{1}{2} \begin{pmatrix}
1 & -1 \\
0 & 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1 \\
\end{pmatrix}
\end{aligned}
$$

2. **Method 2: Use $(HS)^{-1} = S^{-1}H^{-1}$**
   - **Find $S^{-1}$:**
     With $\det S = (2)(1) - (0)(0) = 2$:

$$
S^{-1} = \frac{1}{2} \begin{pmatrix}
1 & 0 \\
0 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 1 \\
\end{pmatrix}
$$

   - **Find $H^{-1}$:**
     With $\det H = (1)(1) - (1)(0) = 1$:

$$
H^{-1} = \frac{1}{1} \begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
$$

   - **Multiply $S^{-1}$ on the right by $H^{-1}$:**

$$
\begin{aligned}
S^{-1}H^{-1} &= \begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{1}{2}(1) + 0(0) & \frac{1}{2}(-1) + 0(1) \\
0(1) + 1(0) & 0(-1) + 1(1) \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1 \\
\end{pmatrix}
\end{aligned}
$$

3. **Compare the Results and Test the Incorrect Order $H^{-1}S^{-1}$:**
   - **Comparison:** Both Method 1 and Method 2 produce the exact same inverse matrix:

$$
T^{-1} = (HS)^{-1} = S^{-1}H^{-1} = \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1 \\
\end{pmatrix}
$$

   - **Compute the incorrect order $H^{-1}S^{-1}$:**

$$
\begin{aligned}
H^{-1}S^{-1} &= \begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1\left(\frac{1}{2}\right) + (-1)(0) & 1(0) + (-1)(1) \\
0\left(\frac{1}{2}\right) + 1(0) & 0(0) + 1(1) \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{1}{2} & -1 \\
0 & 1 \\
\end{pmatrix}
\end{aligned}
$$

   - **Observation:** Because $-\frac{1}{2} \neq -1$, the incorrect order $H^{-1}S^{-1}$ yields a completely different matrix that is **not** equal to $T^{-1}$.

4. **Explanation of the Rule (“When Undoing a Composition of Operations, We Undo Them from the End”):**
   - When the composite transformation $T = HS$ is applied to an input vector $\mathbf{x}$, matrix multiplication acts from right to left:

$$
T\mathbf{x} = (HS)\mathbf{x} = H(S\mathbf{x})
$$

   - First, $S$ stretches the $x$-coordinate by a factor of $2$; second, $H$ shears the stretched result horizontally by adding the $y$-coordinate to the $x$-coordinate.
   - To return to the original vector $\mathbf{x}$, we cannot undo the scaling first because the shear $H$ has already mixed the $y$-coordinate into the scaled $x$-coordinate. Instead, we must peel off the transformations in reverse chronological order—starting from the last operation applied ($H$) and working backward to the first ($S$):

$$
(S^{-1}H^{-1})(HS\mathbf{x}) = S^{-1}(H^{-1}H)(S\mathbf{x}) = S^{-1}I(S\mathbf{x}) = S^{-1}S\mathbf{x} = \mathbf{x}
$$

## Verification

We can verify how $T$, $T^{-1} = S^{-1}H^{-1}$, and the incorrect matrix $H^{-1}S^{-1}$ act on a concrete test vector, such as $\mathbf{x} = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$:

1. **Apply $T = HS$ to $\mathbf{x}$:**
   - First apply $S$: $S\mathbf{x} = \begin{pmatrix} 2 & 0 \\ 0 & 1 \\ \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} 2 \\ 2 \end{pmatrix}$ (horizontal stretch).
   - Second apply $H$: $H(S\mathbf{x}) = \begin{pmatrix} 1 & 1 \\ 0 & 1 \\ \end{pmatrix} \begin{pmatrix} 2 \\ 2 \end{pmatrix} = \begin{pmatrix} 4 \\ 2 \end{pmatrix}$ (horizontal shear).
   - Thus, $\mathbf{y} = T\mathbf{x} = \begin{pmatrix} 4 \\ 2 \end{pmatrix}$.

2. **Undo with the true inverse $T^{-1} = S^{-1}H^{-1}$:**

$$
T^{-1}\mathbf{y} = \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{2}(4) - \frac{1}{2}(2) \\
0(4) + 1(2) \\
\end{pmatrix}
= \begin{pmatrix}
2 - 1 \\
2 \\
\end{pmatrix}
= \begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
= \mathbf{x}
$$

   The original vector $\mathbf{x}$ is recovered identically.

3. **Test the incorrect order $H^{-1}S^{-1}$ on $\mathbf{y}$:**

$$
(H^{-1}S^{-1})\mathbf{y} = \begin{pmatrix}
\frac{1}{2} & -1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{2}(4) - 1(2) \\
0(4) + 1(2) \\
\end{pmatrix}
= \begin{pmatrix}
2 - 2 \\
2 \\
\end{pmatrix}
= \begin{pmatrix}
0 \\
2 \\
\end{pmatrix}
\neq \mathbf{x}
$$

   Applying the inverses in the wrong order fails to recover $\mathbf{x}$, confirming both the algebraic formula $(HS)^{-1} = S^{-1}H^{-1}$ and its geometric meaning.
