### Exercise 1. From a System to a Matrix

## Question

Write the system

$$
\begin{cases}
2x - y + z = 4, \\
x + 3y - 2z = 1, \\
3x + y + z = 7.
\end{cases}
$$

in the form $A\mathbf{x} = \mathbf{b}$. Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

## Solution

1. **Matrix Form ($A\mathbf{x} = \mathbf{b}$):**
   The given system of linear equations can be written as:

$$
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
= \begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}
$$

2. **Identification of Components:**
   - **Coefficient matrix ($A$):**
   
$$
A = \begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1 \\
\end{pmatrix}
$$

   - **Vector of unknowns ($\mathbf{x}$):**

$$
\mathbf{x} = \begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
$$

   - **Right-hand side vector ($\mathbf{b}$):**

$$
\mathbf{b} = \begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}
$$

3. **Row-to-Equation Correspondence:**
   Each row in the matrix equation $A\mathbf{x} = \mathbf{b}$ directly encodes one linear equation from the system through row-column multiplication:
   - **Row 1:** Multiplying the first row $\begin{pmatrix} 2 & -1 & 1 \end{pmatrix}$ by $\mathbf{x}$ yields $2x - 1y + 1z$, which equals the first entry of $\mathbf{b}$ ($4$), reconstructing $2x - y + z = 4$.
   - **Row 2:** Multiplying the second row $\begin{pmatrix} 1 & 3 & -2 \end{pmatrix}$ by $\mathbf{x}$ yields $1x + 3y - 2z$, which equals the second entry of $\mathbf{b}$ ($1$), reconstructing $x + 3y - 2z = 1$.
   - **Row 3:** Multiplying the third row $\begin{pmatrix} 3 & 1 & 1 \end{pmatrix}$ by $\mathbf{x}$ yields $3x + 1y + 1z$, which equals the third entry of $\mathbf{b}$ ($7$), reconstructing $3x + y + z = 7$.

## Verification

Performing the matrix-vector product $A\mathbf{x}$ confirms that the matrix notation recovers the original system:

$$
A\mathbf{x} = \begin{pmatrix}
(2)(x) + (-1)(y) + (1)(z) \\
(1)(x) + (3)(y) + (-2)(z) \\
(3)(x) + (1)(y) + (1)(z) \\
\end{pmatrix}
= \begin{pmatrix}
2x - y + z \\
x + 3y - 2z \\
3x + y + z \\
\end{pmatrix}
= \begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}
$$

Equating corresponding components returns the exact original system of equations.
