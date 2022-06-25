##### Determinants in 2D
**The determinant** of the matrix $A = \begin{pmatrix} a & b \\ c & d\end{pmatrix}$ is: $det\ A$ or $\begin{bmatrix}a & b \\ c & d\end{bmatrix}$ and equals to the number $ad - bc$

The matrix is **singular** if and only if its determinant is $0$.
* $det\ A = 0 \iff$ the vectors $(a\ c)^\mathsf{T}$ and $(b\ d)^\mathsf{T}$ are collinear $\iff$ the matrix $A$ is singular $\iff$ the system $Ax = b$ is not always consistent

* $det A = 0 \iff singular$
* $nonsingular \implies detA \ne 0$

* $det\ A \ne 0$:  **Cramer's rule** for solutions:
  $$
  \begin{pmatrix} a & b & | e \\ c & d & | f \end{pmatrix} \quad \quad \quad x = \frac{de - bf}{ad - bc} = \frac {
  \begin{bmatrix} e & b \\ f & d\end{bmatrix} } {
  \begin{bmatrix} a & b \\ c & d\end{bmatrix} } \quad \quad
  y = \frac{af - ce}{ad - bc} = \frac {
  \begin{bmatrix} a & e \\ c & f\end{bmatrix} } {
  \begin{bmatrix} a & b \\ c & d\end{bmatrix} }
 $$
**Properties:**
1. If the columns / rows of $A$ are exchanged to get $A_1$, then $det(A) = - det(A_1)$
2. $det\ A$ is a **linear function** of any row / column:
    $det \begin{pmatrix} a_1 + a_2 \\ a\end{pmatrix} = det \begin{pmatrix} a_1 \\ a \end{pmatrix} + det \begin{pmatrix} a_2 \\ a \end{pmatrix}$
    $det \begin{pmatrix} s \times a_1 \\ a \end{pmatrix} = s \times det \begin{pmatrix} a_1 \\ a \end{pmatrix}$
3. If columns / rows of $A$ are *collinear*, then $det\ A = 0$
4. $det\ A$ does *not* change if we add to row an even number of times another row
5. $A$ is invertible $\iff det(A) \ne 0$;
    $A^{-1} = \frac{1}{det\ A} \times \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$

The determinant of the matrix is signed *area of the parallelogram* formed by vectors $(a\ b)$ and $(c\ d)$ on the $xy$-plane.


##### Determinants in 3D
**The determinant** of the matrix $A = \begin{pmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{pmatrix}$ is: $det\ A$ or $\begin{bmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{bmatrix}$ and equals to the number $a_{11}(a_{22} a_{33} - a_{23} a_{32}) - a_{12}(a_{21} a_{33} - a_{23} a_{31}) + a_{13}(a_{21} a_{32} - a_{22} a_{31})$

*Mnemonic rules:*
1. $\begin{bmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{bmatrix} = a_{11} \times \begin{bmatrix} a_{22} & a_{23} \\ a_{32} & a_{33} \end{bmatrix} - a_{12} \times \begin{bmatrix} a_{21} & a_{23} \\ a_{31} & a_{33} \end{bmatrix} + a_{13} \times \begin{bmatrix} a_{21} & a_{22} \\ a_{31} & a_{32} \end{bmatrix}$

2. Arrow rule: ![](img/img_3.png)
  $---\ =\ -, \quad  \textemdash\textemdash\textemdash = +$
  
3. Triangle rule:
  ![](img/img_4.png)
  
  The determinant of the matrix is the signed *volume of the parallelepiped* formed by the rows of matrix in the $xyz$-space.


##### Determinants in any dimension
The *determinant* is a function $det$ on the square matrices possessing the following *properties*:

1. **Norming:**
    The determinant of the identity matrix is $1$:
    $det(I_n) = 1$;

2. **Antisymmetry:**
    The determinant changes its sign when two rows are exchanged:
    $\begin{bmatrix} c & d \\ a & b \end{bmatrix} = - \begin{bmatrix} a & b \\ c & d \end{bmatrix}$

3. **Row multilinearity:**
    The determinant depends linearly on the first row:
    $\begin{bmatrix} a + a' & b + b' \\ c & d \end{bmatrix} = \begin{bmatrix} a & b \\ c & d \end{bmatrix} + \begin{bmatrix} a' & b' \\ c & d \end{bmatrix}, \quad \quad \begin{bmatrix} sa & sb \\ c & d \end{bmatrix} = s \begin{bmatrix} a & b \\ c & d \end{bmatrix}$

4. **Equal rows:**
    If two rows of $A$ are equal, then $det(A) = 0$
5. **Row operation:**
    Subtracting a multiple of one row from another row leaves the determinant unchanged.
6. **Zero row:**
    If $A$ has a row of zeros, then $det(A) = 0$

7. **Triangularity:**
    If $A$ is triangular, then $det(A) = a_{11}\ a_{22}\ ...\ a_{nn}$

8. **Singularity:**
    If $A$ is nonsingular, then $det(A) \ne 0$

9. **Product rule:**
    $det(AB) = det(A)\ det(B)$ for square matrices
    $det(A^{-1}) = \frac{1}{det(A)}$

10. **Transpose rule:**
    $det(A^\mathsf{T}) = det(A)$
    **Under transposition all row rules become column rules.**

11. $det(A + B) \ne det(A) + det(B)$
12. $det(tA) \ne t\ det(A)$
13. $det(AB) = det(BA)$ for square matrices
14. $det(uA) = u^n det(A)$ for square matrix

15. $det(-A) = - det(A)$ for $n \times n$ matrix $A$, where $n$ is odd
16. $det(-A) = det(A)$ for $n \times n$ matrix $A$, where $n$ is even

* The $(i,\ j)-$**minor** $M_{ij}$ of $A$ is the determinant of the $(n-1) \times (n-1)$ submatrix obtained after removing $i^{th}$ row and $j^{th}$ column from $A$. 
* The $(i,\ j)-$**cofactor** of $A$ is the $C_{ij} := (-1)^{i+j} M_{ij}$

*Row Cofactor Expansion:*
$det(A) = a_{i1}\ C_{i1}\ +\ a_{i2}\ C_{i2}\ +\ ...\ +\ a_{in}\ C_{in}$

*Column Cofactor Expansion:*
$det(A) = a_{1i}\ C_{1i}\ +\ a_{2i}\ C_{2i}\ +\ ...\ +\ a_{ni}\ C_{ni}$

If $A$ is singular, then cofactor expansion $= 0$.
$$
\begin{equation}
\begin{split}
\begin{bmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{bmatrix}
& = \ 
	\begin{bmatrix} \color{pink} a_{11} & \color{pink} 0 & \color{pink} 0 \\ \color{pink} a_{21} & a_{22} & a_{23} \\ \color{pink} a_{31} & a_{32} & a_{33} \end{bmatrix} + 
	
	\begin{bmatrix} \color{pink} 0 & \color{pink} a_{12} & \color{pink} 0 \\ a_{21} & \color{pink} a_{22} & a_{23} \\ a_{31} & \color{pink} a_{32} & a_{33} \end{bmatrix} +
	
	\begin{bmatrix} \color{pink} 0 & \color{pink} 0 & \color{pink} a_{13} \\ a_{21} & a_{22} & \color{pink} a_{23} \\ a_{31} & a_{32} & \color{pink} a_{33} \end{bmatrix} \\
& = \
	\color{pink} a_{11} \color{white}
		\underbrace{\begin{bmatrix} a_{22} & a_{23} \\ a_{32} & a_{33} \\ \end{bmatrix}}_{\text{(1,\ 1)-minor}} \quad \quad \ \ \ \color{SpringGreen} -
	\color{pink} a_{12} \color{white}
		\underbrace{\begin{bmatrix} a_{21} & a_{23} \\ a_{31} & a_{33} \\ \end{bmatrix}}_{\text{(1,\ 2)-minor}} +
	\color{pink} a_{13} \color{white}
		\underbrace{\begin{bmatrix} a_{21} & a_{22} \\ a_{31} & a_{32} \\ \end{bmatrix}}_{\text{(1,\ 3)-minor}} \\
& = \ 
	\color{pink} a_{11} \color{white}
		\underbrace{\begin{bmatrix} a_{22} & a_{23} \\ a_{32} & a_{33} \\ \end{bmatrix}}_{\text{(1,\ 1)-cofactor}} +
	\color{pink} a_{12} \color{white} \underbrace{ \color{SpringGreen} (-\ 1)\ 
		\begin{bmatrix} a_{21} & a_{23} \\ a_{31} & a_{33} \\ \end{bmatrix}}_{\text{(1,\ 2)-cofactor}} +
	\color{pink} a_{13} \color{white}
		\underbrace{\begin{bmatrix} a_{21} & a_{22} \\ a_{31} & a_{32} \\ \end{bmatrix}}_{\text{(1,\ 3)-cofactor}} \\
\end{split}
\end{equation}
$$

**Cross-product of vectors:**
* *Orthonormal vectors:* both has length of $1$ (*normal*) and are orthogonal to each other
* Let $\vec{U} = (u_1,\ u_2,\ u_3)$ and $\vec{V} = (v_1,\ v_2,\ v_3)$ are non-collinear vectors in $\mathbb{R}^3$;
   Let $\vec{e_1}, \vec{e_2}, \vec{e_3}$ be the orthonormal basis vectors in $\mathbb{R}^3$

**Cross-product**, or **vector product** of $\vec{U}$ and $\vec{V}$ is $\vec{U} \times \vec{V}$.
$\vec{U} \times \vec{V} = \begin{bmatrix} \vec{e_1} & \vec{e_2} & \vec{e_3} \\ u_1 & u_2 & u_3 \\ v_1 & v_2 & v_3 \end{bmatrix} = C_{11}\ \vec{e_1}\ +\ C_{12}\ \vec{e_2}\ +\ C_{13}\ \vec{e_3} = (C_{11},\ C_{12},\ C_{13})$ 
Magnitude of the vector achieved by the cross-product is perpendicular to the parallelogram created by the vectors $\vec{U}$ and $\vec{V}$, and its area equals to the vector magnitude. 

* Cross-product of two vectors in $\mathbb{R}^2$ is the area of the parallelogram could be created by those vectors.
* $\vec{U} \times \vec{V} = - \vec{V} \times \vec{U}$
* If $\vec{U}$ is to the left of $\vec{V}$  - product is negative
* $(k \cdot \vec{U}) \times \vec{V} = k \cdot (\vec{U} \times {\vec{V}})$


##### Inverse matrix via determinants
Let $\sigma : \{1, 2, ..., n\} \rightarrow \{1, 2, ..., n\}$ be one-to-one function:
	$\sigma \rightsquigarrow \begin{pmatrix} 1 & 2 & \dots & n \\ \sigma(1) & \sigma(2) & \dots & \sigma(n) \end{pmatrix}$ 
$P_\sigma$ - the matrix performing the row permutations $\sigma$.

* $det(A) = \sum_{\sigma} a_{1\ \sigma(1)} \cdot a_{2\ \sigma(2)}\ \cdot \ ...\ \cdot \ a_{n\ \sigma(n)} \times det(P_\sigma)$

**Characteristic polynomial** of a $n \times n$ matrix $A$ is:  $p_A(\lambda) := det(A - \lambda I)$
It is polynomial of degree $n$, and has at most $n$ zeros.
$p_A(\lambda) = \begin{bmatrix} a_{11} - \lambda & a_{12} & \dots & a_{1n} \\ a_{21} & a_{22} - \lambda & \dots & a_{2n} \\ \dots & \dots & \dots & \dots \\ a_{n1} & a_{n2} & \dots & a_{nn} - \lambda \end{bmatrix} = (-\lambda)^n + trace(A)(-\lambda)^{n-1} + \dots + c_1 \lambda + det(A)$


The $n \times n$ matrix $A$ with $det(A) \ne 0$ **is invertible** and $(A^{-1})_{ij} = \frac{C_{ji}}{det(A)}$
The row cofactor expansion gives:  $AC^\mathsf{T} = det(A) I_n$
$C^\mathsf{T}$ is the **classical adjoint / adjugate** matrix $adj(A)$ of $A$.
$A^{-1} = \frac{1}{det(A)} \cdot adj(A)$
$A \cdot adj(A) = adj(A) \cdot A = det(A) \cdot I$


**Cramer's rule:**
$A$ is a $n \times n$ invertible matrix,  $\vec(b) \in \mathbb{R}^n$.
Then, the $j^{th}$ entry of $\vec{x} := A^{-1}\ \vec{b} = x_j = \frac{det(B_j)}{det(A)}$,  where $B_j$ is $A$ with the $i^{th}$ column replaced by $\vec{b}$.


##### Equation of a plane in $\mathbb{R}^3$
Given three points: $P_1(x_1, y_1, z_1), P_1(x_2, y_2, z_2), P_3(x_3, y_3, z_3)$, find the equation of the plane $\pi$ through those points.
Let $P(x, y, z)$ be a generic point of the plane; then:
$\begin{vmatrix} x - x_1 & y - y_1 & z - z_1 \\ x_2 - x_1 & y_2 - y_1 & z_2 - z_1 \\ x_3 - x_1 & y_3 - y_1 & z_3 - z_1\end{vmatrix} = \begin{vmatrix} x & y & z \\ x_2 - x_1 & y_2 - y_1 & z_2 - z_1 \\ x_3 - x_1 & y_3 - y_1 & z_3 - z_1 \end{vmatrix} - \underbrace{\begin{vmatrix} x_1 & y_1 & z_1 \\ x_2 - x_1 & y_2 - y_1 & z_2 - z_1 \\ x_3 - x_1 & y_3 - y_1 & z_3 - z_1 \end{vmatrix}}_{d} = (C_{11}x + C_{12}y + C_{13}z) - d = 0$
$ax + by + cz = d$ - the *normal* vector $\vec{n} := (a, b, c)$ can be taken to be the cross-product $\vec{U} \times \vec{V}$ of $\vec{U} = \vec{P_1 P_2}$ and $\vec{V} = \vec{P_1 P_3}$
