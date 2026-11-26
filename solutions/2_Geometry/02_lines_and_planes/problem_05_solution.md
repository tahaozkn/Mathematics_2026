### Exercise 5. Relative Position of Two Lines

## Question

Analyze the position of

$$
L_1 : (x, y, z) = (1, 1, 0) + t(1, 2, 1),
$$

$$
L_2 : (x, y, z) = (2, 0, 1) + s(0, 1, -1).
$$

If they intersect, give the intersection point. If not, determine whether they are parallel or skew. Justify the classification.

## Solution

1. **Check Whether the Lines Are Parallel (Compare Direction Vectors):**
   Extract the direction vectors from the parametric equations of $L_1$ and $L_2$:

$$
\mathbf{v}_1 = \begin{pmatrix}
1 \\
2 \\
1 \\
\end{pmatrix}, \quad
\mathbf{v}_2 = \begin{pmatrix}
0 \\
1 \\
-1 \\
\end{pmatrix}
$$

   Two lines are parallel if and only if their direction vectors are scalar multiples of each other ($\mathbf{v}_1 = k\mathbf{v}_2$ for some scalar $k \in \mathbb{R}$). Looking at the first component:

$$
1 = k(0) \implies 1 = 0 \quad (\text{impossible})
$$

   Since $\mathbf{v}_1$ and $\mathbf{v}_2$ are not proportional, **the lines $L_1$ and $L_2$ are not parallel**. Therefore, they must either **intersect** at a single point or be **skew**.

2. **Test for an Intersection Point:**
   Write both lines in scalar parametric form:

$$
L_1 : \begin{cases}
x = 1 + t \\
y = 1 + 2t \\
z = t
\end{cases}
\qquad
L_2 : \begin{cases}
x = 2 \\
y = s \\
z = 1 - s
\end{cases}
$$

   An intersection point exists if and only if there is a pair of parameter values $(t, s) \in \mathbb{R}^2$ that produces the exact same $(x, y, z)$ coordinates on both lines. Set the corresponding coordinates equal:

$$
\begin{cases}
1 + t = 2 & \text{(Equation 1: } x\text{-coordinate)} \\
1 + 2t = s & \text{(Equation 2: } y\text{-coordinate)} \\
t = 1 - s & \text{(Equation 3: } z\text{-coordinate)}
\end{cases}
$$

   - **Solve Equations 1 and 2 for $t$ and $s$:**
     From Equation 1:

$$
1 + t = 2 \implies t = 1
$$

     Substitute $t = 1$ into Equation 2:

$$
s = 1 + 2(1) = 3
$$

   - **Check Consistency in Equation 3:**
     Substitute $t = 1$ and $s = 3$ into Equation 3 ($t = 1 - s$):

$$
\begin{aligned}
\text{Left-hand side:} &\quad t = 1 \\
\text{Right-hand side:} &\quad 1 - s = 1 - 3 = -2
\end{aligned}
$$

     Since $1 \neq -2$, the system of three equations is **inconsistent**—no single pair $(t, s)$ satisfies all three coordinate equations simultaneously.

3. **Classification and Justification:**
   - **Classification:** The lines $L_1$ and $L_2$ are **skew lines**.
   - **Justification:** In $\mathbb{R}^3$, two distinct lines must fall into one of three mutually exclusive cases:
     1. **Parallel** (same direction, no intersection),
     2. **Intersecting** (different directions, share a common point), or
     3. **Skew** (different directions, no common point, do not lie in a common plane).

     Because $\mathbf{v}_1$ and $\mathbf{v}_2$ are not scalar multiples (ruling out parallel/coincident lines) and the coordinate system $L_1(t) = L_2(s)$ has no solution (ruling out intersection), $L_1$ and $L_2$ are **skew**.

## Verification

We can independently confirm that $L_1$ and $L_2$ are skew using the **scalar triple product** $\overrightarrow{P_1P_2} \cdot (\mathbf{v}_1 \times \mathbf{v}_2)$, which measures the signed volume of the parallelepiped spanned by the connecting vector $\overrightarrow{P_1P_2}$ and the two direction vectors. Two lines in space are coplanar (either parallel or intersecting) if and only if this volume is zero; if it is non-zero, the lines cannot lie in the same plane and must be skew.

1. **Compute the Vector Connecting Base Points $P_1 = (1, 1, 0)$ and $P_2 = (2, 0, 1)$:**

$$
\overrightarrow{P_1P_2} = P_2 - P_1 = \begin{pmatrix}
2 - 1 \\
0 - 1 \\
1 - 0 \\
\end{pmatrix}
= \begin{pmatrix}
1 \\
-1 \\
1 \\
\end{pmatrix}
$$

2. **Compute the Cross Product $\mathbf{v}_1 \times \mathbf{v}_2$:**

$$
\begin{aligned}
\mathbf{v}_1 \times \mathbf{v}_2 &= \begin{pmatrix}
1 \\
2 \\
1 \\
\end{pmatrix}
\times
\begin{pmatrix}
0 \\
1 \\
-1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
(2)(-1) - (1)(1) \\
(1)(0) - (1)(-1) \\
(1)(1) - (2)(0) \\
\end{pmatrix} \\
&= \begin{pmatrix}
-2 - 1 \\
0 + 1 \\
1 - 0 \\
\end{pmatrix} \\
&= \begin{pmatrix}
-3 \\
1 \\
1 \\
\end{pmatrix}
\end{aligned}
$$

3. **Compute the Scalar Triple Product:**

$$
\begin{aligned}
\overrightarrow{P_1P_2} \cdot (\mathbf{v}_1 \times \mathbf{v}_2) &= \begin{pmatrix}
1 \\
-1 \\
1 \\
\end{pmatrix}
\cdot
\begin{pmatrix}
-3 \\
1 \\
1 \\
\end{pmatrix} \\
&= 1(-3) + (-1)(1) + 1(1) \\
&= -3 - 1 + 1 \\
&= -3 \neq 0
\end{aligned}
$$

Since the scalar triple product is $-3 \neq 0$, the lines do not lie in a common plane, confirming that $L_1$ and $L_2$ are skew.
