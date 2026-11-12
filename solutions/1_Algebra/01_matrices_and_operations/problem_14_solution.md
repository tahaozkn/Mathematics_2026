### Exercise 14. Rotation Matrices

## Question

The matrix for a rotation through an angle $\theta$ is

$$R(\theta) = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \\ \end{pmatrix}$$

Compute $R(\alpha)R(\beta)$ and, using the angle-sum formulas for sine and cosine, show that

$$R(\alpha)R(\beta) = R(\alpha+\beta).$$

Explain the result geometrically.

## Solution

Computing the matrix product $R(\alpha)R(\beta)$ gives:

$$\begin{aligned} R(\alpha)R(\beta) &= \begin{pmatrix} \cos\alpha & -\sin\alpha \\ \sin\alpha & \cos\alpha \\ \end{pmatrix} \begin{pmatrix} \cos\beta & -\sin\beta \\ \sin\beta & \cos\beta \\ \end{pmatrix} \\ &= \begin{pmatrix} \cos\alpha\cos\beta - \sin\alpha\sin\beta & -\cos\alpha\sin\beta - \sin\alpha\cos\beta \\ \sin\alpha\cos\beta + \cos\alpha\sin\beta & -\sin\alpha\sin\beta + \cos\alpha\cos\beta \\ \end{pmatrix} \\ &= \begin{pmatrix} \cos\alpha\cos\beta - \sin\alpha\sin\beta & -(\sin\alpha\cos\beta + \cos\alpha\sin\beta) \\ \sin\alpha\cos\beta + \cos\alpha\sin\beta & \cos\alpha\cos\beta - \sin\alpha\sin\beta \\ \end{pmatrix} \end{aligned}$$

Applying the trigonometric angle-sum formulas

$$\cos(\alpha+\beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$$

and

$$\sin(\alpha+\beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$$

to each entry yields:

$$R(\alpha)R(\beta) = \begin{pmatrix} \cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta) \\ \end{pmatrix} = R(\alpha+\beta).$$

**Geometric explanation:** 
Matrix multiplication represents the composition of linear transformations. Applying $R(\beta)$ to a vector rotates it counterclockwise about the origin by angle $\beta$, and then applying $R(\alpha)$ rotates the resulting vector counterclockwise by an additional angle $\alpha$. Performing two successive counterclockwise rotations in the plane is geometrically identical to a single counterclockwise rotation by the sum of the angles, $\alpha+\beta$.

## Verification

We can verify the identity by evaluating both sides at specific angles, $\alpha = \frac{\pi}{6}$ and $\beta = \frac{\pi}{3}$, for which $\alpha + \beta = \frac{\pi}{2}$:

$$R\left(\frac{\pi}{6}\right) = \begin{pmatrix} \frac{\sqrt{3}}{2} & -\frac{1}{2} \\ \frac{1}{2} & \frac{\sqrt{3}}{2} \\ \end{pmatrix}, \qquad R\left(\frac{\pi}{3}\right) = \begin{pmatrix} \frac{1}{2} & -\frac{\sqrt{3}}{2} \\ \frac{\sqrt{3}}{2} & \frac{1}{2} \\ \end{pmatrix}$$

Multiplying these two matrices directly gives:

$$\begin{aligned} R\left(\frac{\pi}{6}\right)R\left(\frac{\pi}{3}\right) &= \begin{pmatrix} \frac{\sqrt{3}}{2}\cdot\frac{1}{2} + \left(-\frac{1}{2}\right)\cdot\frac{\sqrt{3}}{2} & \frac{\sqrt{3}}{2}\cdot\left(-\frac{\sqrt{3}}{2}\right) + \left(-\frac{1}{2}\right)\cdot\frac{1}{2} \\ \frac{1}{2}\cdot\frac{1}{2} + \frac{\sqrt{3}}{2}\cdot\frac{\sqrt{3}}{2} & \frac{1}{2}\cdot\left(-\frac{\sqrt{3}}{2}\right) + \frac{\sqrt{3}}{2}\cdot\frac{1}{2} \\ \end{pmatrix} \\ &= \begin{pmatrix} \frac{\sqrt{3}}{4} - \frac{\sqrt{3}}{4} & -\frac{3}{4} - \frac{1}{4} \\ \frac{1}{4} + \frac{3}{4} & -\frac{\sqrt{3}}{4} + \frac{\sqrt{3}}{4} \\ \end{pmatrix} \\ &= \begin{pmatrix} 0 & -1 \\ 1 & 0 \\ \end{pmatrix} \end{aligned}$$

Evaluating $R(\alpha+\beta)$directly at$\alpha + \beta = \frac{\pi}{2}$ gives:  $$
R\left(\frac{\pi}{2}\right) =
\begin{pmatrix}
\cos\left(\frac{\pi}{2}\right) & -\sin\left(\frac{\pi}{2}\right) \\
\sin\left(\frac{\pi}{2}\right) & \cos\left(\frac{\pi}{2}\right) \\
\end{pmatrix}
=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{
