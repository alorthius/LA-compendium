##### Orthogonal bases
A set $S = {\vec{u_1} \vec{u_2}, \cdots, \vec{u_k}}$ of nonzero vectors in $\mathbb{R}^n$ is **orthogonal** if $\langle \vec{u_i}, \vec{u_j} \rangle = 0$ for $i \neq j$

An orthogonal set $S$ such that $||\vec{u}|| = 1$ for each $\vec{u} \in S$ is called **orthonormal**.

* Every *orthogonal set* $S$ can be made *orthonormal* if we replace each $\vec{u}$ is $S$ by $\frac{\vec{u}}{||\vec{u}||}$
* Every orthogonal set is linearly independent
* Every orthogonal set $S \subset \mathbb{R}^n$ is contained in an orthogonal basis of $\mathbb{R}^n$.

* **Coordinate representation in orthonormal bases:**
	For every $\vec{u} \in \mathbb{R}^n$ in an *orthonormal basis ONB* $S = (\vec{u_1}, \cdots, \vec{u_n})$ of $\mathbb{R^n}$:
	$\vec{u} = \langle \vec{u}, \vec{u_1}\rangle \cdot \vec{u_1} + \cdots + \langle \vec{u}, \vec{u_n}\rangle \cdot \vec{u_n}$
	$\vec{u} = \frac{\langle \vec{u}, \vec{u_1}\rangle}{||\vec{u_1}||^2} \cdot \vec{u_1} + \cdots + \frac{\langle \vec{u}, \vec{u_n}\rangle}{||\vec{u_n}||^2} \cdot \vec{u_n}$

* **Corollary**
	Let $B := (\vec{u_1}, \vec{u_2}, \cdots, \vec{u_n})$ be orthonormal basis of $\mathbb{R}^n$,
	$\vec{c} := (c_1, c_2, \cdots, c_n)^\mathsf{T}$ be coordinate vector of $\vec{x}$ in basis $B$,
	$T_B : \vec{x} \mapsto \vec{c}$  be the coordinate map
	$U$ be a matrix with columns $\vec{u_1}, \vec{u_2}, \cdots, \vec{u_n}$
	
	Then:
	$c_k = \vec{u_k}^\mathsf{T} \vec{x}$
	$T_B(\vec{x}) = U^\mathsf{T} \vec{x}$
	$U U^\mathsf{T} = I_n$

##### Orthonormal matrices
If an $m \times n$ matrix $Q$ has ***orthonormal** columns*, then:
* $Q^\mathsf{T} Q = I_n$
* *Least squares solution* of  $Q \vec{x} = \vec{b}$  is  $\hat{\vec{x}} = (Q^\mathsf{T} Q)^{-1} Q^\mathsf{T} \vec{b} = Q^\mathsf{T} \vec{b}$
* *The projection* $\vec{p}$ (the best approximation in $C(Q)$) is  $QQ^\mathsf{T} \vec{b}$
* *The orthogonal projection operator* onto $C(Q) \subset \mathbb{R}^m$ is  $P = QQ^\mathsf{T}$
* $\vec{p} = QQ^\mathsf{T}\vec{b}$  is *the basis decomposition* of $\vec{p}$ in the orthonormal basis $\vec{q_k}$ of $C(Q)$:  $\vec{p} = \vec{q_1}(\vec{q_1}^\mathsf{T} \vec{b}) + \vec{q_2}(\vec{q_2}^\mathsf{T} \vec{b}) + \cdots + \vec{q_n}(\vec{q_n}^\mathsf{T} \vec{b})$

If an $m \times n$ matrix $Q$ has ***orthogonal** columns*, then:
* *The orthogonal projection operator* onto $C(Q) \subset \mathbb{R}^m$ is:
	$P_W = Q(Q^\mathsf{T}Q)^{-1} Q^\mathsf{T} = Q \cdot \begin{pmatrix} \frac{1}{||\vec{q_1}||^2} & 0 & \cdots & 0 \\ 0 & \frac{1}{||\vec{q_2}||^2} & \cdots & 0 \\ \cdots & \cdots & \cdots & \cdots \\ 0 & 0 & \cdots & \frac{1}{||\vec{q_n}||^2} \end{pmatrix} \cdot Q^\mathsf{T} = \frac{\vec{q_1} \vec{q_1}^\mathsf{T}}{||\vec{q_1}||^2} + \frac{\vec{q_2} \vec{q_2}^\mathsf{T}}{||\vec{q_2}||^2} + \cdots + \frac{\vec{q_n} \vec{q_n}^\mathsf{T}}{||\vec{q_n}||^2}$
* *The projection* $\vec{p}$ (the best approximation of $b$ in $C(Q)$)  $\vec{p} = \frac{\vec{q_1}^\mathsf{T} \vec{b}}{||\vec{q_1}||^2}\cdot \vec{q_1} + \frac{\vec{q_2}^\mathsf{T} \vec{b}}{||\vec{q_2}||^2}\cdot \vec{q_2} + \cdots + \frac{\vec{q_n}^\mathsf{T} \vec{b}}{||\vec{q_n}||^2}\cdot \vec{q_n}$

An $n \times n$ matrix $U$ is called **orthogonal** if $U^{-1} = U^\mathsf{T}$ ( if $U^\mathsf{T}U = UU^\mathsf{T} = I_n$ )

1. An orthogonal matrix $U$ does not change scalar products $\langle U\vec{u}, U\vec{v}\rangle = \langle\vec{u},\vec{v}\rangle$
2. An orthogonal matrix preserves the angle between vectors

*$U$ is orthogonal $\iff$ its columns form an ONB of $\mathbb{R}^n$ $\iff$ $U$ does not change length of vectors $\iff$ $U$ sends every ONB into ONB*

##### Gram-Schmidt orthogonalization
![](img/img_6.png)

##### QR factorization / decomposition

**QR factorization** of an $m \times n$ matrix $A$ is its representation as $A = QR$, where:
	$Q$ is an $m \times n$ matrix having *orthonormal columns*
	$R$ is an $n \times n$ *upper-triangular* matrix

* It not always is unique
* $A$ has linearly independent columns $\iff$ $R$ is non-singular

![](img/img_7.png)

##### Definition(s) of rank of matrix
1. Rank is the number of pivot variables;
2. Rank is the dimension of a vector space spanned by its rows/columns;
3. Rank is the number of non-zero singular values;
4. Rank is the size of the largest non-zero minor;
	Non-zero minor shows that the rows and columns of the submatrix are linearly independent, so the original matrix rows and columns corresponding to them are also linearly independent, so the rank is at least as large as a size of a particular non-zero minor.
5. Rank is the dimension of the range of a matrix.

##### Relation between rank(A) and dimension of range(A)
Let $A$ be an $m \times n$ matrix.
* *Range* of $A$ is the set of all vectors $b \in \mathbb{R}^m$ of the form $y=Ax$ for which the system $Ax=b$ is consistent. It is the linear combination of the columns of $A$.
* $Ax=b$ is consistent $\iff b$ is in the $range(A)$.
* $rank(A)=dim\ range(A)$ 

##### Relation between rank(AB) and rank(A) and rank(B)
Let $A$ be an $m \times n$ matrix.
* For an $n \times k$ matrix $B$: $rank(AB) \le min\{rank(A), rank(B)\}$  $(range(AB) \in range(A))$
* For an $k \times m$ matrix $B$: $rank(BA) \le min\{rank(A), rank(B)\}$;  $(R(BA) \in R(A))$
	
* For a non-singular $n \times n$ matrix $B$: $rank(AB) = rank(A)$  $(range(AB) = range(A))$
* For a non-singular $m \times m$ matrix $B$: $rank(BA) = rank(A)$  $(R(BA)=R(A))$