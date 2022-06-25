##### Low rank approximations
**Spectral theorem** states that for symmetric (Hermitian, anti-symmetric, skew-Hermitian, orthogonal, unitary) matrix there is an orthogonal basis of eigenvectors $\vec{u_1}, \dots, \vec{u_n}$ for eigenvalues $\lambda_1, \dots, \lambda_n$ such that:
* $A = \sum_{i = 1}^{n} \lambda_i \vec{u_i} \vec{u_i}^\mathsf{T}$
* $P^{-1} AP = P^\mathsf{T} AP = \Lambda \iff A = P \Lambda P^\mathsf{T}$,
	where $\Lambda = diag(\lambda_1, \dots, \lambda_n)$,  $P$ with columns $\vec{u_1}, \dots, \vec{u_n}$

Eigenvalues for different matrices are:
1. *Real* for symmetric / Hermitian matrices
2. *Purely imaginary* for anti-symmetric / skew-Hermitian ones
3. *Unimodular* ($|\lambda| = 1$) for orthogonal / unitary matrices


* $dist(A, B) = ||A - B||$
* **Frobenius** norm:  $||A||_F^2 := \sum_{j,k=1}^{n} |a_{jk}|^2 = trace(A^\mathsf{T}A) = \sum_{j=1}^{n} |\lambda_j|^2$
* $||A - A_k||_F^2 = \sum_{j=k+1}^n \lambda_j^2$
* $A_k$ is the best rank $k$ approximation of $A$


* **Rank-one approximation problem:**
In Frobenius norm, the best rank-one approximation of $A$ is $\vec{u_1} \vec{v_1}^\mathsf{T}$ (usually we write $\sigma_1 \vec{u} \vec{v_1}$, where $\vec{u}$ is the unit vector)

* **The trolley line problem:**
For the given vectors $\vec{a_1}, \vec{a_2}, \dots, \vec{a_m}$ in $\mathbb{R}^m$, find their best line fit $\ell$. The objective function to be minimized:
$f(\ell) := \sum_{k=1}^{m} dist^2(\vec{a_j}, \ell)$


##### Singular Value Decomposition
* Let $A$ be any $m \times n$ matrix
* Matrix $B := A^\mathsf{T}A$ is $n \times n$ and nonnegative:
	$\vec{x}^\mathsf{T} B \vec{x} = \vec{x}^\mathsf{T} (A^\mathsf{T}A) \vec{x} = (A \vec{x})^\mathsf{T} (A \vec{x}) = ||A \vec{x}||^2 \ge 0$
* The eigenvalues of $A$ are $\lambda_1 \ge \lambda_2 \ge \dots \ge \lambda_n$ 
* $\sigma_j := \sqrt{\lambda_j}$ are **singular values** of $A$
* $r := rank\ B = rank\ A$  positive  $\sigma_j$

**Singular Value Decomposition SVD:**
Every $m \times n$ matrix $A$ can be written as $A = U \Sigma V^\mathsf{T}$,
	where $U$ and $V$ are orthogonal:
	$U = (\vec{u_1} \dots \vec{u_r} | \vec{u_{r+1}} \dots \vec{u_m})$ 
	$V = (\vec{v_1} \dots \vec{v_r} | \vec{v_{r+1}} \dots \vec{v_n})$ ,
	$\Sigma$ is an $m \times n$ matrix with singular values of $A$ on its main diagonal and zeros otherwise.
* $\vec{v_j}$ are eigenvectors of $A^\mathsf{T}A$ with eigenvalues $\sigma_j^2: A^\mathsf{T} A \vec{v_j} = \sigma_j^2 \vec{v_j}$
* $\vec{u_j} := \frac{A\vec{v_j}}{||A\vec{v_j}||} = \frac{A\vec{v_j}}{\sigma_j}$ for $j = 1, \dots, r$ is an orthonormal basis for the column space of $A$
* $\vec{v_j}$ for $j = r, \dots, n$ is a basis for nullspace of $A$
* $\vec{u_1}, \dots, \vec{u_m}$ is an orthonormal basis for $\mathbb{R}^m$
* $A = \sigma_1 \vec{u_1} \vec{v_1}^\mathsf{T} + \dots + \sigma_r \vec{u_r} \vec{v_r}^\mathsf{T}$
	The vectors $\vec{u_1}, \dots, \vec{u_r}$ are the **left singular vectors** of $A$;
	The vectors $\vec{v_1}, \dots, \vec{v_r}$ are the **right singular vectors** of $A$.

* The reduced SVD removes the uninformative parts


![](img/img_8.png)


##### Applications
* **Polar decomposition**
	Any square matrix $A$ can be written as $QS$ with orthogonal $Q$ and symmetric positive semidefinite $S$;
	$A = U\Sigma V^\mathsf{T} := QS$
	$Q := UV^\mathsf{T}$,
	$S := V\Sigma V^\mathsf{T}$

* **Moore-Penrose pseudo-inverse**
	For an $m \times n$ matrix $A$, its Moore-Penrose pseudo-inverse is an $n \times m$ matrix $A^\dagger$ satisfying:
	* $A^\dagger AA^\dagger = A^\dagger$
	* $AA^\dagger = A$
	* $(A^\dagger A)^\mathsf{T} = A^\dagger A$
	* $(AA^\dagger) = AA^\dagger$

* For every matrix $A$, its Moore-Penrose pseudo-inverse $A^\dagger$ exists and is unique
* $A = QR$,  $A^\dagger = R^{-1}Q^\mathsf{T}$

* $\hat{x} = A^\dagger \vec{b}$ is the best solution of $A \vec{x} = \vec{b}$

![](img/img_9.png)