A matrix $A$ with complex entries is called **Hermitian** if $A^* := (\bar{A})^\mathsf{T} = A$  $(a_{ij} = \bar{a_{ji}})$.
$A^*$ is the **adjoint** of $A$

Let $A$ be *Hermitian* matrix, then:
1. All eigenvalues are real;
2. Eigenvectors corresponding to distinct eigenvalues are orthogonal (may have complex entries)
3. No generalized eigenvectors
4. Diagonalizable


##### Anti-symmetric matrices
* **Anti-symmetric** matrix:
	$A^\mathsf{T} = - A$
* **Skew-Hermitian** matrix:
	$A^* = -A$

* *For a real matrix $A$:  $A$ is anti-symmetric $\iff$ $iA$ is Hermitian*
* Eigenvalues of anti-symmetric matrices are purely imaginary
* Every anti-symmetric $A$ is orthogonally diagonalizable: $Q^\mathsf{T}AQ = -iD$

* *$A$ is skew-Hermitian $\iff$ $iA$ is Hermitian*
* $A$ is Hermitian $\implies$ $iA$ is skew-Hermitian
* If $A$ is anti-symmetric (skew-Hermitian), then $e^{tA}$ is orthogonal (unitary).
* If $e^{tA}$ is orthogonal, then $A$ is anti-symmetric

##### Unitary matrices
* A matrix $U$ with complex entries is **unitary** if $U^\dagger = U^{-1}$
* $U^\dagger U = UU^\dagger = UU^{-1} = I$

* *Characterization of unitary matrices:*
	For a square $U$:   $U$ is unitary $\iff U$ preserves norms:  $||U \vec{x}|| = ||\vec{x}||$
	A unitary matrix $U$ also preserves the scalar products:  $(U\vec{x})\times(U\vec{y}) = \vec{x} \times \vec{y}$

* *Spectral properties of unitary matrices:*
	For a unitary matrix $U$:
	1. All eigenvalues $\lambda$ satisfy $|\lambda| = 1$
	2. Eigenvectors corresponding to distinct eigenvalues are orthogonal

* *Spectral Theorem for unitary matrices:*
	A unitary matrix $U$ is unitarily diagonalizable, i.e., there is a unitary matrix $P$ such that $P^\dagger UP = diag\{e^{i\theta_1}, \dots, e^{i\theta_n}\}$


##### Projections
The sum $U + W$ of two subsets $U$ and $W$ of a vector space $V$ is:
$U + W = \{ \vec{u} + \vec{w}\ |\ \vec{u} \in U, \vec{w} \in W \}$

* This sum is *direct* ($U \dotplus W$)  if $U \cap W = \{ \vec{0} \}$
	 $U \dotplus W \ne U \cup W$ 
	 If $\vec{v_1}$ and $\vec{v_2}$ are linearly independent, then $ls\{\vec{v_1}\} \dotplus ls\{\vec{v_2}\} = ls\{\vec{v_1}, \vec{v_2}\}$
	 
* The sum $V = U \dotplus W$ is direct $\iff$ every vector $\vec{v} \in V$  has a *unique* representation as $\vec{v} = \vec{u} + \vec{w}$, with $\vec{u} \in U$ and $\vec{w} \in W$
	1. $\vec{v} \mapsto \vec{u}$ is the *projection* of $V$ onto $U$ parallel to $W$
	2. $\vec{v} \mapsto \vec{w}$ is the *projection* of $V$ onto $W$ parallel to $U$

* The  projection $T$ of $V$ onto $U$ parallel to $W$ is a linear mapping satisfying $T^2=T$.
* It is uniquely fixed by the requirements that $T \vec{u} = \vec{u}$ for all $\vec{u} \in U$ and $T \vec{w} = 0$ for all $\vec{w} \in W$.

* An $n \times n$ matrix $A$ is called **idempotent** if $A^2 = A$
* If $A$ is a matrix of projection $T$ of $V$ onto $U$ parallel to $W$, then $A$ is an idempotent matrix.

* Idempotent matrix has eigenvalues: $\lambda = 0$ and/or $\lambda = 1$
* Every idempotent $A$ is a matrix of projection of $\mathbb{R}^n$ onto the column space $col(A)$ parallel to the nullspace $nul(A)$

* $A$ is a matrix of an orthogonal projection $\iff A$ is a symmetric idempotent

* $P$ is idempotent and symmetric: $nul(P) = nul(A^\mathsf{T}) = (col(A))^\perp$
* For any $m \times n$ matrix $A$ with linearly independent columns the matrix $P := A(A^\mathsf{T}A)^{-1}A^\mathsf{T}$ is an orthogonal projection of $\mathbb{R}^m$ onto $col(A)$.
