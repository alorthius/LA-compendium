##### Matrices basics
A **matrix** $A$ is a rectangular array of numbers / scalars.
$A$ has $m$ rows and $n$ columns - it is $m \times n$ matrix with size $m \times n$

* *Column vector* : $m \times 1$ matrix
* *Row vector* : $1 \times n$ matrix

$a_{ij}$ is the *entry* of $A$ in $i^{th}$ row and $j^{th}$ column. $a_{ij} = (A)_{ij}$
Entries $a_{11}, a_{22}, ...$ form the **main diagonal** of $A$.
$A = (a_{ij})_{m \times n}$ or $A = (a_{ij})$

*Special matrices:*
* **Zero matrix:** $a_{ij} = 0$
* **Square matrix:** $m = n$
* **Diagonal matrix:** all entries which are *not* on the main diagonal are equal to $0$
		$$
	D = diag\{d_1, d_2, ..., d_n\}
	$$
	$$
	D = \begin{pmatrix}  
	d_{1} & 0 & ... & 0 \\
	0 & d_{2} & ... & 0 \\
	...    & ...    & ... & ...    \\
	0 & 0 & ... & d_{n} \\
	\end{pmatrix}
	$$
* **Identity matrix:** a square diagonal matrix $I_n$ with all diagonal entries being equal to $1$:
$$
I_n = diag\{1, 1, ..., 1\}
$$

##### Basic operations
* **Equality:**
	Two matrices $B$ and $C$ are *equal* if they are:
		* of the same size
		* all the corresponding entries are equal
	$B = C \iff b_{ij} = c_{ij}, \quad 1 \le i \le m, 1 \le j \le n$

* **Multiplication by scalars:**
	$kA = (ka_{ij})_{m \times n} \quad (kA)_{ij} = ka_{ij}$ 

* **Addition / subtraction:**
	If two matrices $B$ and $C$ are of the same size:
	$(B \pm C)_{ij} = (B)_{ij} \pm (C)_{ij}$

* **Transposition $A^\mathsf{T}$:**
	$A = (a_{ij})_{m \times n}$
	$A^\mathsf{T} \quad is\ of\ size\ n \times m \quad and \quad (A^\mathsf{T})_{ij} = a_{ij}$ 
	*Rows of $A$ become columns of $A^\mathsf{T}$.* The main diagonal remains the same.

$$
A = \begin{pmatrix}  
a_1 & a_2 & a_3 \\
b_1 & b_2 & b_3 \\
\end{pmatrix} \quad 
A^\mathsf{T} = \begin{pmatrix}  
a_1 & b_1 \\
a_2 & b_2 \\
a_3 & b_3 \\
\end{pmatrix}
$$

* **Trace** of a *square* matrix:
	The sum of the elements on the main diagonal:
	$trace\ A\ := a_{11} + a_{22} + ... + a_{nn}$

##### Matrix basic operations properties
Let $A$, $B$ and $C$ be the matrices of the *same size*, and $r$, $s$ any scalars:
* *Commutative:* $A + B = B + A$
  *Matrix zero:* $A + 0 = 0 + A$
* *Associative:* $(A + B) + C = A + (B + C) \quad \quad r(sA) = (rs)A$
* *Distributive:* $r(A + B) = rA + rB \quad \quad (r + s)A = rA + sA$

##### Matrix multiplication
* **Row - column multiplication:**
	The **inner product** of a $1 \times n$ (row) vector $u = (u_1\ u_2\ ...\ u_n)$  and a $n \times 1$ (column) vector $v = (v_1\ v_2\ ...\ v_n)^\mathsf{T}$ is:
	$$u \times v = (u_1\ u_2\ ...\ u_n) \times \begin{pmatrix}
v_1    \\
v_2    \\
\vdots \\
v_n    \\
\end{pmatrix} = u_1 v_1 + u_2 v_2 + ... + u_n v_n
$$
	row $\times$ column = number
	column $\times$ row = matrix

* **Matrix - vector multiplication:**
	For matrix $A = (a_{ij})_{m \times n}$ and a column vector $x = (x_1 x_2 ... x_n)^\mathsf{T}$ the product $Ax$ can be defined in two ways:
	* **Row form of matrix - vector multiplication:**
		$r_i = (a_{i1}\ a_{i2}\ ...\ a_{in})$ - the $i^{th}$ row of $A$, then:
		$$
		A \times x =
	\begin{pmatrix}
	r_1    \\
	\vdots \\
	r_m    \\
	\end{pmatrix} \times x =
	\begin{pmatrix}
	r_1 x  \\
	\vdots \\
	r_m x  \\
	\end{pmatrix} =
	\begin{pmatrix}
	a_{11} x_1 + ... + a_{1n} x_n    \\
	\vdots                           \\
	a_{m1} x_1 + ... + a_{mn} x_n    \\
	\end{pmatrix}
    $$
	* **Column form of matrix - vector multiplication:**
		$c_1,\ c_2,\ ...,\ c_n$ - columns of $A$
		$$
		A \times x = \begin{pmatrix}
		c_1 & c_2 & ... & c_n
		\end{pmatrix} \times \begin{pmatrix}
		x_1 \\
		x_2 \\
		\vdots \\
		x_n \\
		\end{pmatrix} = x_1 c_1 + x_2 c_2 + ... + x_n c_n
    $$
**Matrix - matrix multiplication**
If $A$ is an $m \times n$ matrix and $B$ is an $n \times k$ matrix with columns $b_1, ..., b_k$, then the **product** $AB$ is: $A \times B = A \times (b_1 \quad b_2 \quad \dots \quad b_k) = (A b_1 \quad A b_2 \quad \dots \quad A b_k)$ and is $m \times k$ matrix.
  * The $j^{th}$ column of $AB$ is $Ac_j(B)$
  * Columns of $AB$ are linear combinations of the columns of $A$
  * The $j^{th}$ entry of $AB$ is the product of $i^{th}$ row of $A$ and $j^{th}$ column of $B$: $(AB)_{ij} = r_i(A) c_j(B)$

**Vector - matrix multiplication:**
  * $a = (a_1\ a_2\ ...\ a_n)$ - row vector, $B$ - $n \times k$ matrix with rows $r_i(B)$ and columns $c_j(B)$:
	  $a \times B = a(\ c_1(B) \quad c_2(B) \quad ... \quad c_k(B)\ ) = (\  ac_1(B) \quad ac_2(B) \quad ... \quad ac_k(B)\ ) = a_1 r_1(B) + a_2 r_2(B) + ... + a_n r_n(B)$
  * $aB$ is the linear combination of the rows of $B$
  * The $i^{th}$ row of $AB$ is $r_i(A)B$
  *  Rows of $AB$ are linear combinations of the rows of $B$

*Example:*
$$
A = (a_{ij})_{2 \times 3} = \begin{pmatrix}
0 & 2 & 1 \\
-1 & 0 & 2 \\
\end{pmatrix} \quad
B = (b_{ij})_{3 \times 3} = \begin{pmatrix}
1 & 0 & 1 \\
1 & 2 & 1 \\
2 & 1 & 0 \\
\end{pmatrix},\quad then \quad A \times B = C = (c_{ij})_{2 \times 3}
$$
$$
\begin{equation}
\begin{cases}
	c_1(C) = A \times c_1(B) = 1 \cdot \begin{pmatrix} 0 \\ -1 \end{pmatrix} + 1 \cdot \begin{pmatrix} 2 \\ 0 \end{pmatrix} + 2 \cdot \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} 4 \\ 3 \end{pmatrix} \\
    c_2(C) = A \times c_2(B) = 0 \cdot \begin{pmatrix} 0 \\ -1 \end{pmatrix} + 2 \cdot \begin{pmatrix} 2 \\ 0 \end{pmatrix} + 1 \cdot \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} 5 \\ 2 \end{pmatrix} \\
    c_3(C) = A \times c_3(B) = 1 \cdot \begin{pmatrix} 0 \\ -1 \end{pmatrix} + 1 \cdot \begin{pmatrix} 2 \\ 0 \end{pmatrix} + 0 \cdot \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} 2 \\ -1 \end{pmatrix}
\end{cases} \implies C = \begin{pmatrix} 4 & 5 & 2 \\ 3 & 2 & -1\end{pmatrix}
\end{equation}
$$
$$

$$
$$
\begin{equation}
\begin{cases}
	r_1(C) = r_1(A) \times B = 0 \cdot (1 \quad 0 \quad 1) + 2 \cdot (1 \quad 2 \quad 1) + 1 \cdot (2 \quad 1 \quad 0) = (4 \quad 5 \quad 2) \\
	r_2(C) = r_2(A) \times B = -1 \cdot (1 \quad 0 \quad 1) + 0 \cdot (1 \quad 2 \quad 1) + 2 \cdot (2 \quad 1 \quad 0) = (3 \quad 2 \quad -1)
\end{cases} \implies C = \begin{pmatrix} 4 & 5 & 2 \\ 3 & 2 & -1\end{pmatrix}
\end{equation}
$$

##### Multiplication properties
$A$ - matrix $m \times n$, $B$ and $C$ are of sizes permitting the multiplications below:
* *Associative law:* $(AB)C = A(BC)$
* *Distributive law:* $(A + B)C = AC + BC$   and   $A(B + C) = AB + AC$
* *Scalar:* $r(AB) = (rA)B = A(rB)$
* *Identity for matrix multiplication:* $I_m A = A = A I_n$
* *Multiplication and transposition:* $(AB)^\mathsf{T} = B^\mathsf{T} A^\mathsf{T}$
* $A = (A^\mathsf{T})^\mathsf{T}$
* *No commutativity in general:* $AB \ne BA$
* *Trace order independence:* $trace(AB) = trace(BA)$
* $trace(AB) \ne trace(A) \cdot trace(B)$

$A$, $B$, $C$ are $n \times n$ matrices:
* $trace(cA) = c \cdot trace(A)$
* $AB = AC$$\implies$ $B = C$ if $A \ne 0$

##### Linear combination and independence
$Ax$ is the **linear combination** *of columns* of $A$.
* A **linear combination of the vectors** $v_1,\ v_2,\ ...,\ v_k$ in $\mathbb{R}^n$ is a vector:
	$c_1 v_1 + c_2 v_2 + ... + c_k v_k$ with any scalars $c_1, c_2, ..., c_k$
* The set of all linear combinations of given vectors $v_1,\ v_2,\ ...,\ v_k$ is called their **linear span** and denoted as  $ls\{v_1,\ v_2,\ ...,\ v_k\}$

* A collection of non-zero vectors $v_1,\ v_2,\ ...,\ v_k$ is **linearly independent** if no nontrivial linear combination of the vectors in a collection equals to zero vector $0$. Or:
  They are linearly independent if the equality $c_1 v_1 + c_2 v_2 + ... + c_k v_k = 0$ implies that $c_1 = c_2 = \dots = c_k = 0$
  
* If REF of the collection of vectors $v_1,\ v_2,\ ...,\ v_k$ in homogeneous case ($b = 0$) has one unique solution - the vectors are *linearly independent*

##### Corollaries for linear systems
**Solutions to a homogeneous system $Ax = 0$:**
  * If $U$ is a solution of $Ax = 0$, so is $tU$
  * If $U$ and $V$ are solutions, so is $U + V$
  * If $U$ and $V$ are solutions, so is $sU + tV$ for all scalars $s$ and $t$

**Solutions to a non-homogeneous system $Ax = b$:**
  * If $U$ and $V$ are the solutions, then $U - V$ solves $Ax = 0$
  * If $U$ is a solution of $Ax = b$ and $AV = 0$, then $A(U + tV) = b$

  * For $Ax = b$ to be consistent, $b$ must be a *linear combination* of the columns of $A$
  * $Ax = b$ consistent for all $b$ $\iff$ columns of $A$ span $\mathbb{R}^m$ (solution existence)
  * Unique solution $\iff$ columns of $A$ linearly independent (solution uniqueness)


##### Invertible matrix
A square $n \times n$ matrix $A$ is called **invertible** if there is a matrix $B$ such that $AB = I_n (= BA)$.
Then $B$ is called the **inverse** of $A$ and denoted as $A^{-1}$.

* **Right- and left- invertibility:**
  If $A$, $B$ and $C$ are square matrices, such that $BA = AC = I$, then, if $A$ is invertible: $B = C = A^{-1}$. The matrix is invertible, if it is left- *and* right- invertible. 

  $AB = I$ - right-invertible $\implies$ solution existence
  $CA = I$ - left-invertible $\implies$ solution uniqueness
  For unique solution, matrix should be both left- and right- invertible

* **Product invertibility:**
  If $A$ and $B$ are invertible, then so is $AB$ and $(AB)^{-1} = B^{-1} A^{-1}$

##### Characterization of invertible matrices
$A$ is **non-singular** if the $Ax = b$ has a unique solution for *every* choice of b.
*Non - singularity $\iff$ Invertibility*

If $A$ is non-singular and can be transformed to its RREF $I_n$ by applying elementary matrices $E_1, E_2, ..., E_k$, then applying them on $I_n$ will result in $A^{-1}$.

For an $n \times n$ matrix $A$, the following statements are *equivalent*:
1. $A$ and $A^\mathsf{T}$ *are invertible and non-singular*
2. $A$ has $n$ pivot positions in its REF
3. $I_n$ is the RREF of $A$
4. $A$ is expressible as a product of elementary matrices
5. $Ax = 0$ has only trivial solution
6. $Ax = b$ is consistent for every $b \in \mathbb{R}^n$ 
7. There is an $n \times n$ matrix $B$, such that $AB = I$, and
     there is an $n \times n$ matrix $C$, such that $CA = I$
8. Both rows and columns of $A$ *span* $\mathbb{R}^n$ and *are linearly independent*

* If $A$ and $B$ are square matrices and $AB$ is invertible, then both $A$ and $B$ are invertible. 
* A square upper- or lower- triangular matrix $A$ is invertible $\iff$ there are no zeros on its diagonal
* The inverse matrix *is unique* (if exists)
* An expression of the invertible matrix $A$ as a product of elementary matrices *is not unique*
* $x := A^{-1}b$ solves $Ax = b$
* If $A$ is an $n \times n$ matrix that is not invertible, then the $Ax = 0$ has infinitely many solutions

* If $A$ is an $n \times n$ not invertible matrix, then the matrix obtained by interchanging two rows of $A$ can't be invertible
* If $A$ is invertible and a multiple of the first row of $A$ is added to the second row, then the resulting matrix is invertible


##### Elementary row operations
**Lower - triangular (upper - triangular)** is the square matrix with all entries *above (below)* the main diagonal are zero. 

*Lemma:* the product of two lower (upper) - triangular matrices is lower (upper) - triangular.
  
Let $A$ be an $m \times n$ coefficient matrix of a system $Ax = B$. The *elementary row transformations (operations) (ERO)* of matrix $A$ can be obtained by multiplication of the matrix from the left by matrices of special form, which are called **elementary matrices**. 
  
  1. **Row multiplication:**
	  Multiply $i^{th}$ row by $t$ = matrix multiplication $EA$: ($E$ is both lower- and upper- triangular)
	  $E = diag\{1, ..., 1, t, 1, ..., 1\}$
	                    $i - 1$
	$E^{-1} = diag\{1, ..., 1, t ^ {-1}, 1, ..., 1\}$
	                        $i - 1$
	
  2. **Row replacement:**
	  Add $\alpha$ times $k^{th}$ row to $l^{th}$ row = matrix multiplication $EA$: ($E$ is either lower- or upper- triangular)
	  $$
   E_{ij} = \begin{equation}
   \begin{cases}
   1, & \mbox{if } i = j \\
   \alpha, & \mbox{if } i = l, j = k\\
   0, & \mbox{otherwise}
   \end{cases}
   \end{equation}
   $$
	$$
	E = \begin{pmatrix}
	1 & k & & \\
	& \downarrow & & \\
	l \to & \alpha & 1 & \\
	& & & \ddots\\
	& & & & 1 \\
	\end{pmatrix} \quad \quad
	E^{-1} = \begin{pmatrix}
	1 & k & & \\
	& \downarrow & & \\
	l \to & -\alpha & 1 & \\
	& & & \ddots\\
	& & & & 1 \\
	\end{pmatrix}
   $$

  3. **Row interchange:**
	  Interchange $k^{th}$ and $l^{th}$ rows = matrix multiplication $EA$:
	  $$
	  E = E^{-1} = \begin{pmatrix}
	  1 & k \\
	  & 0 & 0 & 1 \\
	  & \downarrow & 1 & \uparrow \\
	  & 1 & 0 & 0 \\
	  & & & l & 1
	  \end{pmatrix}
	  \begin{matrix}
	  \\
	  \leftarrow k \\
	  \\
	  \leftarrow l \\
	  \\
	  \end{matrix}
   $$

##### LU - factorization
**$LU$ - factorization of $A$:**
  If $m \times n$ matrix $A$ can be reduced to a REF upper-triangular $m \times n$ matrix $U$ using only row multiplication and/or substitution operations, then $A = LU$, where $L$ is the lower-triangular $m \times m$ matrix - the product of the inverted elementary matrices.
  
  * $L$: lower-triangular, $U$: upper-triangular
  * $L$ is unique if all its diagonal entries are $1$
  * If row interchanges are needed, use $PA = LU$, where $P$ encodes all row interchanges

  * When $A = LU$, the $Ax = b$ can be written as $L(Ux) = b$. Then: $Ax = b \iff \begin{equation} \begin{cases} Ux = y \\ Ly = b \\ \end{cases} \end{equation}$
