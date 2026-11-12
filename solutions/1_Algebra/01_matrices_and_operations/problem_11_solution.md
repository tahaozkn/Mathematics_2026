### Exercise 11. When Do Matrices Commute?

## Question

Given

$$
A = \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}, \quad B = \begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
$$

Find the conditions on $a, b, c, d$ under which $AB = BA$. Describe the general form of all such matrices $B$.

## Solution

1. **Compute the product $AB$:**

$$
AB = \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
= \begin{pmatrix}
a + c & b + d \\
c & d \\
\end{pmatrix}
$$

2. **Compute the product $BA$:**

$$
BA = \begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
a & a + b \\
c & c + d \\
\end{pmatrix}
$$

3. **Equate $AB = BA$:**
For the two matrices to be equal, their corresponding entries must match:

$$
\begin{cases}
a + c = a, \\
b + d = a + b, \\
c = c, \\
d = c + d.
\end{cases}
$$

4. **Solve the system:**
- From $a + c = a$, we find $c = 0$.
- From $b + d = a + b$, substituting $c = 0$ yields $d = a$.
- The entry $c = c$ is trivially satisfied, and $d = c + d$ becomes $d = 0 + d$, which holds since $d = a$.

5. **General form of matrix $B$:**
Substituting $c = 0$ and $d = a$, the matrix $B$ takes the form:

$$
B = \begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix}
$$

where $a$ and $b$ can be any real numbers.

## Verification

We verify the commutativity property by multiplying $A$ and this general form of $B$:

$$
AB = \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix}
= \begin{pmatrix}
a & b + a \\
0 & a \\
\end{pmatrix}
$$

$$
BA = \begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
a & a + b \\
0 & a \\
\end{pmatrix}
$$

Since $AB = BA$ holds identically for any real values of $a$ and $b$, the conditions and general form are fully verified without any unclosed environments.
