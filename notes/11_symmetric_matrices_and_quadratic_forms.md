##### Symmetric matrices
A matrix $A$ with real entries is **symmetric** if $A^\mathsf{T} = A$

If $A$ is a symmetric $n \times n$ matrix, then:
1. All eigenvalues are real;
2. Eigenvectors corresponding to distinct eigenvalues are orthogonal
3. Even if $A$ has multiple eigenvalues, there is a nonsingular $P$ whose columns $\vec{w_1}, \dots, \vec{w_n}$ are eigenvectors of $A$ such that:
	* $\vec{w_1}, \dots, \vec{w_n}$ are mutually orthonormal
	* $P^{-1} = P^\mathsf{T}$  ($P$ is orthogonal)
	* $P^{-1} AP = P^\mathsf{T}AP = diag\{r_1, \dots, r_n\}$

A matrix $A$ with complex entries is called **Hermitian** if $A* := (\bar{A})^\mathsf{T} = A$  $(a_{ij} = \bar{a_{ji}})$.
$A*$ is the **adjoint** of $A$

Let $A$ be Hermitian matrix, then:
1. All eigenvalues are real;
2. Eigenvectors corresponding to distinct eigenvalues are orthogonal (may have complex entries)
3. No generalized eigenvectors
4. Diagonalizable


##### Quadratic forms
A **quadratic form** $Q$ is a function $Q : \mathbb{R}^n \mapsto \mathbb{R} : Q(\vec{x}) = Q(x_1, x_2, \dots, x_n) = \sum a_{ij} x_i x_j$
* $Q(\vec{x}) = \vec{x}^\mathsf{T} A \vec{x}$
* $Q(\vec{x}) = Q(P \vec{y}) = (P \vec{y})^\mathsf{T} A (P \vec{y}) = \vec{y}^\mathsf{T} (P^\mathsf{T} AP) \vec{y}$

* *Principal axis theorem:*
	If $A$ is a symmetric matrix, then there is an orthogonal change of variables $\vec{x} = P \vec{y}$ that transforms the quadratic form $\vec{x}^\mathsf{T} A \vec{x}$ into $\vec{x}^\mathsf{T} A \vec{x} = \vec{y}^\mathsf{T} D \vec{y} = r_1 y_1^2 + \dots + r_n y_n^2$, where $r_1, \dots, r_n$ are the eigenvalues of $A$ corresponding to the eigenvectors $\vec{v_1}, \dots, \vec{v_n}$ forming the columns of $P$

A quadratic form $Q(\vec{x}) = \vec{x}^\mathsf{T} A \vec{x}$ (a symmetric matrix $A$ with $r_1, \dots, r_k$ being its eigenvalues) is called:
1. *Positive definite* $\iff \forall \vec{x} \neq 0: Q(\vec{x}) > 0 \iff \forall j=1,\dots,k: r_j > 0$
2. *Positive semidefinite* $\iff \forall \vec{x} \neq 0: Q(\vec{x}) \ge 0 \iff \forall j=1,\dots,k: r_j \ge 0$
3. *Negative definite* $\iff \forall \vec{x} \neq 0: Q(\vec{x}) < 0 \iff \forall j=1,\dots,k: r_j < 0$
4. *Negative semidefinite* $\iff \forall \vec{x} \neq 0: Q(\vec{x}) \le 0 \iff \forall j=1,\dots,k: r_j \le 0$
5. *Indefinite* $\iff \exists \vec{x_1}, \vec{x_2}: Q(\vec{x_1}) < 0\   \&\ Q(\vec{x_2}) > 0 \iff \exists i, j : r_i < 0\ \&\ r_j > 0$

* Assume that $Q(\vec{x}) = \vec{x}^\mathsf{T} A \vec{x}$ with symmetric $A$ and that $\lambda_{min}$ and $\lambda_{max}$ are the minimal and maximal eigenvalues of $A$. Then:  $\lambda_{min} ||\vec{x}||^2 \le Q(\vec{x}) \le \lambda_{max} ||\vec{x}||^2$


##### Cholesky decomposition
Let $A$ be a symmetric matrix. The following are equivalent:
1. $A$ is positive definite
2. There is a nonsingular $B$ such that $A = B^\mathsf{T}B$
3. There is a nonsingular $C$ such that $C^\mathsf{T}AC = I$

*The standard form of Cholesky decomposition:*  $A = LL^\mathsf{T}$

* If there is Cholesky decomposition of $A$ then $A$ is semi-definite
* If $A$ is positive semi-definite, then $LL^\mathsf{T}$ exists and is unique
* Positive definite matrix decomposition:
	If $L$ has diagonal $S$, then with $L := L_1 S$ and $D := S^2$:  $A = L_1 D L_1^\mathsf{T}$

**Sylvester criterion:**
A symmetric $A$ is positive definite $\iff$ all principal minors $M_k$ of $A$ are positive

**Principal minor:**
The *principal minor* $M_k$ is the determinant of the $k \times k$ upper-left corner of $A$

* For negative definiteness, signs of principal minors should alternate, starting from the negative one.
