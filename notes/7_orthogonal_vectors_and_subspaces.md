##### Distance
A mapping $\rho : V \times V \mapsto \mathbb{R}$ is called **the distance** on a linear vector space $V$ if it satisfies the following conditions:
	1. *Positivity:*  $\rho(\vec{x}, \vec{y}) \geq 0 \qquad \rho(\vec{x}, \vec{y}) = 0 \iff \vec{x} = \vec{y}$
	2. *Symmetry:* $\rho(\vec{x}, \vec{y}) = \rho(\vec{y}, \vec{x})$
	3. *Triangle inequality:* $\rho(\vec{x}, \vec{y}) \leq \rho(\vec{x}, \vec{z}) + \rho(\vec{z}, \vec{y})$
	4. *Translation invariant:* $\rho(\vec{x}, \vec{y}) = \rho(\vec{x} + \vec{z}, \vec{y} + \vec{z}) \quad \forall \vec{z} \in V$

* *Euclidean distance:*  $\rho_E(\vec{x}, \vec{y}) := \sqrt{(x_1 - y_1)^2 + (x_2 - y_2)^2 + \cdots + (x_n - y_n)^2} = || \vec{x} - \vec{y} ||$
* *Block / Manhattan distance:*  $\rho_M(\vec{x}, \vec{y}) := |x_1 - y_1| + |x_2 - y_2| + \cdots + |x_n - y_n|$
* *Maximum-coordinate distance:*  $\rho_\infty(\vec{x}, \vec{y}) = max\{|x_1 - y_1|, |x_2 - y_2|, \cdots, |x_n - y_n|\}$

##### Norm
**A norm** $|| \cdot ||$ *(length of the vector)* on a linear vector space $V$ is a function $V \to \mathbb{R}$ with the following properties:
	1. *Positivity:* $||\vec{x}|| \geq 0 \qquad ||\vec{x}|| = 0 \iff \vec{x} = \vec{0}$
	2. *Linearity:* $||k\vec{x}|| = |k| \cdot ||\vec{x}|| \quad \forall k \in \mathbb{R},\ \forall \vec{x} \in V$
	3. *Triangle inequality:* $||\vec{x} + \vec{y}|| \leq ||\vec{x}|| + ||\vec{y}||$

* *Euclidean norm:*  $||\vec{x}||_E := \sqrt{x_1^2 + x_2^2 + \cdots + x_n^2} = \sqrt{\langle \vec{x}, \vec{x} \rangle}$
* *Block / Manhattan norm:*  $||\vec{x}||_M := |x_1| + |x_2| + \cdots + |x_n|$
* *Maximum-coordinate norm (sup-norm):*  $||\vec{x}||_\infty = max\{|x_1|, |x_2|, \cdots, |x_n|\}$

##### Inner product
A mapping $\langle \cdot, \cdot \rangle : V \times V \mapsto \mathbb{R}$ is called an **inner product** in a linear vector space $V$ if it satisfies the following conditions:
	1. *Positivity:* $\langle \vec{u}, \vec{u} \rangle \geq 0 \qquad \langle \vec{u}, \vec{u} \rangle = 0 \iff \vec{u} = \vec{0}$
	2. *Symmetry:* $\langle \vec{u}, \vec{v} \rangle = \langle \vec{v}, \vec{u} \rangle$
	3. *Linearity:* $\langle c_1 \vec{u_1} + c_2 \vec{u_2}, \vec{v} \rangle = c_1 \langle \vec{u_1}, \vec{v} \rangle + c_2 \langle \vec{u_2}, \vec{v} \rangle \quad \forall c_1,c_2 \in \mathbb{R}$

* *Inner / dot / scalar product*: $\langle \vec{x}, \vec{y} \rangle = \vec{x} \times \vec{y} = \vec{x}^T \vec{y} = x_1y_1 + \cdots + x_ny_n$

##### Basic inequalities and theorems
* **Cosine theorem:**
$\langle \vec{x}, \vec{y} \rangle = \vec{x} \times \vec{y} = || \vec{x} || \cdot || \vec{y} || \cdot \cos{\theta}$,   where $\theta$ is the angle between $\vec{x}$ and $\vec{y}$

* **Proposition:**
$\langle A\vec{x}, \vec{y} \rangle = \langle \vec{x}, A^\mathsf{T} \vec{y} \rangle \qquad \forall A_{m \times n} \quad \forall \vec{x} \in \mathbb{R}^n \quad \forall \vec{y} \in \mathbb{R}^m$

* **Cauchy-Bunyakovsky-Schwarz inequality:**
$|\langle \vec{x}, \vec{y} \rangle| \leq ||\vec{x}|| \cdot ||\vec{y}||$

* **Triangle inequality:**
$||\vec{x} \pm \vec{y}|| \leq ||\vec{x}|| + ||\vec{y}||$

* **Pythagorean theorem:**
$\vec{x} \vec{y} = 0 \iff ||\vec{x} \pm \vec{y}||^2 = ||\vec{x}||^2 + ||\vec{y}||^2$

* **Parallelogram identity:**
$||\vec{x} + \vec{y}||^2 + ||\vec{x} - \vec{y}||^2 = 2 ||\vec{x}||^2 + 2||\vec{y}||^2$


##### Orthogonal vectors and subspaces
* $\vec{x}$ and $\vec{y}$ are **orthogonal** $(\vec{x} \perp \vec{y}) \iff \langle \vec{x},\vec{y} \rangle = 0$
* $\vec{x}$ is **orthogonal to subspace** $M$ $(\vec{x} \perp M) \iff \langle \vec{x},\vec{y} \rangle \quad \forall \vec{y} \in M$
* *two subspaces* $L$ and $M$ are **orthogonal** $(L \perp M) \iff \langle \vec{x},\vec{y} \rangle = 0 \quad \forall \vec{x} \in L,\ \forall \vec{y} \in M$

* An **orthogonal complement** $L^\perp$ of a subspace $L: \qquad L^\perp = \{\vec{y} \in \mathbb{R}^n | \vec{y} \perp L\}$
* $L^\perp$ is a subspace
* $\vec{x} \perp \vec{v_1}, \cdots, \vec{v_m} \Longrightarrow \vec{x} \perp ls(\vec{v_1}, \cdots, \vec{v_m})$
* $dim(L^\perp) = n - dim(L)$

* **Orthogonal sum** of orthogonal subspaces $L$ and $M : L \oplus M = \{\vec{x} + \vec{y} | \vec{x} \in L, \vec{y} \in M\}$
* $L \oplus M$ is a subspace
* $dim(L \oplus M) = dim(L) + dim(M)$  (the union of bases of $L$ and $M$ is a basis of $L \oplus M$)
* $L \oplus L^\perp = \mathbb{R}^n$

**Second fundamental theorem of LA:**
1. The column space $C(A)$ of $A$ is the *orthogonal complement* of its left nullspace $N(A^\mathsf{T})$
2. The nullspace $N(A)$ of $A$ is the *orthogonal complement* of its row space $R(A) = C(A^\mathsf{T})$


##### Shortest distance
* **Shortest distance to a line:**
Suppose $\ell$ is a line in $\mathbb{R}^n$ in direction of $\vec{a}$, $P$ is a point in $\mathbb{R}^n$ outside $\ell$:
$Q \in \ell\ minimizes\ |PQ| \iff \overrightarrow{PQ} \perp \overrightarrow{a}$

* **Shortest distance to a plane:**
Suppose $\pi$ is a plane in $\mathbb{R}^n$, $P$ is a point in $\mathbb{R}^n$ outside $\pi$:
$Q \in \pi\ minimizes\ |PQ| \iff \overrightarrow{PQ} \perp \overrightarrow{\pi}$

Instead of a line $\ell$ or a plane $\pi$ we can take any subspace $W \in \mathbb{R}^n$.
