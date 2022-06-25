##### Eigenvalue
An **eigenvalue EV** of a square matrix $A$ is a number $\lambda$ for which $A - \lambda \cdot I$ is singular.

* Diagonal entries of a diagonal matrix $D$ are its eigenvalues
* A square matrix $A$ is singular $\iff$ $0$ is an eigenvalue of $A$
* $A - \lambda I$ is singular $\iff det(A - \lambda I) = 0$

*Markov matrix* - a matrix with non-negative entries and whose columns/rows each sums to $1$.
EV = $\lambda = 1$ for every Markov matrix.

$p_A(\lambda) := det(A - \lambda I)$ is a **characteristic polynomial** of $\lambda$ of degree $n = size(A)$ 

* $A$ possesses at most $n$ distinct eigenvalues
* $det(A - \lambda I) = \lambda^2 - (a_{11} + a_{22})\lambda + det(A)$
* The sum of eigenvalues is equal to the $trace(A)$
* The product of eigenvalues is equal to the $det(A)$

##### Eigenvector
$A - \lambda I$ singular means the system of linear equations $(A - \lambda I) \vec{v} = 0$ has a nontrivial solution. For an eigenvalue $\lambda$ any nonzero $\vec{v}$ satisfying $(A - \lambda I) \vec{v} = \vec{0}$ is called an **eigenvector EVc** of $A$ corresponding to eigenvalue $\lambda$. 
* $(A - \lambda I) \vec{v} = 0 \iff A \vec{v} = \lambda \vec{v}$
* $A - \lambda I$ is singular $\iff$ $det(A - \lambda I) = 0$ $\iff$ $A \vec{v} = \lambda \vec{v}$ for some $\vec{v} \neq 0$
* Diagonal entries of an upper/lower-triangular matrix are its eigenvalues


##### Diagonalization
* $A$ is a $k \times k$ matrix
* $r_1, \dots, r_k$ are eigenvalues of $A$
* $\vec{v_1}, \dots, \vec{v_k}$ are the corresponding eigenvectors
* $P$ is composed of columns of $\vec{v_i}$

Then  $AP = P \cdot diag\{r_1, \dots, r_k\}$
If $P$ is *invertible*, then: $P^{-1}AP = \begin{pmatrix} r_1 & \dots & 0 \\ \vdots & \ddots & \vdots \\ 0 & \dots & r_k \\ \end{pmatrix}$
* If $P$ is such that the above equality holds, then $r_i$ are the eigenvalues of $A$ and the columns of $P$ are the corresponding eigenvectors.
* Let $r_1, \dots, r_h$ be distinct eigenvalues of $A$ and $\vec{v_1}, \dots, \vec{v_h}$ be the corresponding eigenvectors. Then $\vec{v_1}, \dots, \vec{v_h}$ are linearly independent.
* If $A$ has $k$ distinct eigenvalues, then $P$ is invertible.

Let nonsingular $P$ satisfy $P^{-1}AP = D = diag\{r_1, \dots, r_k\}$.
Then $A^n = P D^n P^{-1} = P \begin{pmatrix} r_1^n & \dots & 0 \\ \vdots & \ddots & \vdots \\ 0 & \dots & r_k^n \end{pmatrix} P^{-1}$
And the solution of the difference equation $\vec{z_{n+1}} = A \vec{z_n}$ with initial vector $\vec{z_0}$:
$\vec{z_n} = P \begin{pmatrix} r_1^n & \dots & 0 \\ \vdots & \ddots & \vdots \\ 0 & \dots & r_k^n \end{pmatrix} P^{-1} \vec{z_0} = P \begin{pmatrix} r_1^n & \dots & 0 \\ \vdots & \ddots & \vdots \\ 0 & \dots & r_k^n \end{pmatrix} \vec{c}$


##### Jordan normal form
* For $k \times k$ matrix $A$ exists such a non-singular matrix $P$ that $P^{-1}AP = D$ only if there are $k$ linearly independent eigenvectors of matrix $A$.

$\vec{v_2}, \vec{v_3}, \dots$ are **generalized eigenvectors** $A$ for eigenvalue $\lambda$ if $(A - \lambda)\vec{v_k} = \vec{v_{k-1}}$ with $\vec{-1} := 0$

Matrices $A$ and $B$ are **similar** if there is a nonsingular $P$ such that $P^{-1}AP=B$  $(A \sim B)$. Not every matrix is similar to diagonal one.
Assume $P = (\vec{v_1} \vec{v_2} \dots \vec{v_k}):\quad P^{-1}AP = J_k(\lambda) := \begin{pmatrix} \lambda & 1 & \dots & \dots & 0 \\ 0 & \lambda & 1 & \dots & 0 \\ \dots & \dots & \dots & \dots & \dots \\ 0 & 0 & \dots & \lambda & 1 \\ 0 & 0 & \dots & \dots & \lambda \end{pmatrix}$
* $\vec{v_1}$ is the eigenvector and $\vec{v_2}, \dots, \vec{v_k}$ are the generalized eigenvectors
* $\vec{v_1}, \vec{v_2}, \dots, \vec{v_k}$ span a **root subspace** of $A$ for eigenvalue $\lambda$
* root subspaces are formed by vectors satisfying $(A - \lambda)^k \vec{v} = 0$ and are invariant with respect to A.

* Every matrix is similar to a canonical matrix in the *block-diagonal* form, where all the non-zero parts are the *Jordan blocks* on its diagonal. Diagonal matrix is the case when size of blocks is $1$

* $A \sim \oplus J_{k_j} (\lambda_j)$

If $A \sim B$, then:
* $det(A) = det(B)$
* $trace(A) = trace(B)$
* $A$ is invertible $\iff$ $B$ is invertible
* $rank(A) = rank(B)$
* $dim(ker\ A) = dim(ker\ B)$
* $p_A(\lambda) = p_B(\lambda)$
* the EV of $A$ and $B$ are the same
* dimensions of root spaces are the same
