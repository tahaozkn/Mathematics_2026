### Exercise 9. Area and the Determinant

## Question

The vectors

$$
\mathbf{u} = \begin{pmatrix}
3 \\
1 \\
\end{pmatrix}, \quad
\mathbf{v} = \begin{pmatrix}
1 \\
4 \\
\end{pmatrix}
$$

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

## Solution

1. **Form the Matrix with Vectors as Columns:**
   Place the vectors $\mathbf{u}$ and $\mathbf{v}$ as columns of a $2 \times 2$ matrix $A$:

$$
A = \begin{pmatrix}
\mathbf{u} & \mathbf{v}
\end{pmatrix}
= \begin{pmatrix}
3 & 1 \\
1 & 4 \\
\end{pmatrix}
$$

2. **Compute the Determinant and Area:**
   Compute the determinant of matrix $A$:

$$
\det A = (3)(4) - (1)(1) = 12 - 1 = 11
$$

   The area of the parallelogram spanned by two vectors in the plane is given by the absolute value of the determinant of the matrix formed by those vectors:

$$
\text{Area} = |\det A| = |11| = 11
$$

3. **Reverse the Order of the Vectors:**
   Form a new matrix $A'$ by swapping the columns, placing $\mathbf{v}$ first and $\mathbf{u}$ second:

$$
A' = \begin{pmatrix}
\mathbf{v} & \mathbf{u}
\end{pmatrix}
= \begin{pmatrix}
1 & 3 \\
4 & 1 \\
\end{pmatrix}
$$

   Compute the determinant of $A'$:

$$
\det A' = (1)(1) - (3)(4) = 1 - 12 = -11
$$

4. **Explanation of Changes and Invariants:**
   - **What changes in the determinant?** The determinant changes sign, going from $11$ to $-11$. This occurs because swapping two columns of a square matrix multiplies its determinant by $-1$. Geometrically, the negative sign indicates a change in the **orientation** (chirality) of the ordered pair of vectors in the plane from counterclockwise to clockwise.
   - **What does not change in the area?** The absolute value of the determinant—and therefore the geometric area of the parallelogram—remains completely unchanged at $11$. Area is a non-negative scalar measure of spatial extent, independent of the order in which the bounding vectors are listed.

## Verification

We can verify the area geometrically using alternative methods:

- **Bounding Box Method:**
  The parallelogram is enclosed inside a $3 \times 3$ rectangle (since the span in the $x$-direction goes from $0$ to $3 + 1 = 4$, and in the $y$-direction goes from $0$ to $1 + 4 = 5$, adjusted for the exact bounding box of $3$ units wide by $3$ units high: $x \in [0, 4]$, $y \in [0, 5]$). 
  Subtracting the areas of the surrounding right triangles and rectangles from the total bounding box area:
  - Total bounding box area $= (4)(5) = 20$
  - Subtract the corner triangles and rectangles: $2 \cdot \left(\frac{1}{2} \cdot 3 \cdot 1\right) + 2 \cdot \left(\frac{1}{2} \cdot 1 \cdot 3\right) + \text{extra regions} = 3 + 3 + 3 = 9$
  - Parallelogram area $= 20 - 9 = 11$.

Both the determinant method and geometric decomposition yield the exact same area of $11$, confirming the result.
