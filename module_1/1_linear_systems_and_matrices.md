###### System of linear equations
A **linear equation** is an equation of the form $a_1 x_1 + a_2 x_2 + ... + a_n x_n = b$, where $b$ and the coefficients $a_1, ..., a_n$ are real or complex numbers. A **system of linear equations / linear system** is a collection of one or more linear equations.

A **solution to a system** is an ordered sequence / n-tuple $(s_1, s_2, ..., s_n)$ of numbers turning each equation into equality upon setting $x_1 = s_1, x_2 = s_2, ..., x_n = s_n$. The set of all solutions of a linear system is called the **solution set**. A system is:
	1. **inconsistent** - no solutions
	2. **consistent** - has non-empty solution set
	3. **overdetermined** - has more equations than unknowns
	4.Two systems are **equivalent** - they possess the same set of solutions

###### Lines on the plane
$ax + by = c$ describes:
	1. the line with **slope** $k = \frac{-a}{b}$ through $(0, \frac{c}{b})$ if $b \ne 0$
	2. the line $x = \frac{c}{a}$ if $b = 0$
	3. it is **orthogonal** (perpendicular) to the normal vector $(a, b)$ 

![[pic_1.png]]

The set of solutions for the system of two linear equations is the set of intersection of two lines:
![[pic_2.png]]
There are 3 possible situations, if the lines:
	1. **coincide** - infinitely many solutions
	2. **parallel** - no solutions
	3. **intersect** - one single solution

###### Planes in the 3d-space
$ax + by + cz =d$ describes a plane in $\mathbb{R}^3$ . It is **orthogonal to the gradient** $(a, b, c)$.
The solution set can be:
	1. empty
	2. a point
	3. a line
	4. a plane

###### Gaussian and Gauss–Jordan elimination
Solution methods:
1. **By substitution** - express one variable via other from one equation and then substitute that into another
2. **By elimination** - combine two equations in order to eliminate the variable(s)

###### Shorthand matrix notations for linear systems
A linear system is uniquely determined by coefficients $a_ij$ and $b_i$.
$$
\begin{equation}
\begin{cases}
	a_{11} x_1 + a_{12} x_2 + ... + a_{1n} x_n = b_1 \\
	a_{21} x_1 + a_{22} x_2 + ... + a_{2n} x_n = b_2 \\
	...
	a_{m1} x_1 + a_{m2} x_2 + ... + a_{mn} x_n = b_m \\
\end{cases}\ \sim Ax = b,
\end{equation}
$$where
$$
A = \begin{pmatrix}  
a_{11} & a_{12} & ... & a_{1n} \\
a_{21} & a_{22} & ... & a_{2n} \\
...    & ...    & ... & ...    \\
a_{m1} & a_{m2} & ... & a_{mn} \\
\end{pmatrix} is \ an \ m \times n \ coefficient \ matrix
$$
$$
b = \begin{pmatrix}
b_1    \\
b_2    \\
\vdots \\
b_n    \\
\end{pmatrix} = (b_1, b_2, ..., b_m)^\mathsf{T} \ is \ the \ right \ hand \ side \ (RHS) \ vector
$$
**Augmented coefficient matrix:**
$$
(A \mid b) = \begin{pmatrix}
a_{11} & a_{12} & ... & a_{1n} & b_1    \\
a_{21} & a_{22} & ... & a_{2n} & b_2    \\
...    & ...    & ... & ...    & \vdots \\
a_{m1} & a_{m2} & ... & a_{mn} & b_m    \\
\end{pmatrix}
$$

###### Matrices row properties
**Elementary row operations** that simplify linear systems:
	1. Multiplication of a row by a nonzero constant
	2. Addition of one row to another
	3. Interchange of two rows

Every elementary row operation is *reversible*.

Matrices $A$ and $B$ are **row equivalent** if $B$ can be obtained from $A$ via elementary row operations.

**Row Echelon Form (REF) properties:**
	1. All nonzero rows are above any zero row
	2. Each leading entry is in the column to the right of the leading entry of the row above it.		Leading entry is the first nonzero entry in a row.
	3. All entries in a column below a leading entry are zeros.
	4. It *is not unique*
	5. Every matrix can be transformed to the REF

**Reduced Row Echelon Form (RREF) properties:**
	1. It is REF
	2. The leading entry is each nonzero row is 1
	3. Each leading 1 is the only nonzero element in its column
	4. It *is unique*. Any two equivalent systems of equations will have the same RREF.

**Gauss-Jordan elimination** is the reduction of the system to the RREF.

The **pivot column** of a matrix is a column with a leading entry in an echelon form of the matrix. The corresponding variable is called a **pivot variable**, and the otherwise it is a **free variable**.

The **free variables** are not determined by any other variables.