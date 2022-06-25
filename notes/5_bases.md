##### Bases
A set $S$ of vectors in a vector space $V$ is called **a basis of** $V$ if the following two conditions hold:
	* $S$ is linearly independent
	* $S$ spans $v$

* Any linearly independent vectors $\vec{v_1}, \cdots, \vec{v_n}$ in $\mathbb{R}^n$ form its basis.
* Column of any nonsingular $n \times n$ matrix form a basis of $\mathbb{R}^n$.
* If $\vec{v_1}, \cdots, \vec{v_n}$ is a basis of a vector space $V$, then any $x \in V$ has a **unique representation** $\vec{x} = c_1 \vec{v_1} + \cdots + c_n \vec{v_n}$.

* A **finite-dimensional** vector space $V$ possesses a finite basis;
* An **infinite-dimensional** vector space $V$ does **not** possess a finite basis.
* Any two bases of a finite-dimensional linear vector space have the same number of elements.

**Dimension of the space** $V$ denoted as $dimV$  is the number of elements in any basis of a finite-dimensional vector space $V$.

*Sufficient conditions for a basis:*
	Assume $V$ is an $n$-dimensional linear vector space and $S \subset V$ has $n$ elements. Then the following are equivalent:
	1. $S$ is a basis of $V$
	2. $S$ is linearly independent
	3. $ls(S) = V$

##### Four subspaces and rank of a matrix
Any $m \times n$ matrix $A = (a_{ij})_{m \times n}$ is composed of:
* $m$ **row vectors** $\begin{equation}\begin{cases} \vec{r_1} = (a_{11}, a_{12}, \cdots, a_{1n}) \\ \quad\quad\quad \cdots\cdots \\ \vec{r_m} = (a_{m1}, a_{m2}, \cdots, a_{mn}) \end{cases}\end{equation}$
* $n$ **column vectors** $\vec{c_1} = \begin{pmatrix} a_{11} \\ \cdots \\ a_{m1} \end{pmatrix}, \cdots, \vec{c_n} = \begin{pmatrix} a_{1n} \\ \cdots \\ a_{mn} \end{pmatrix}$.
*There are four subspaces of a matrix:*
	1. **Row space** $R(A)$ of $A$ if the *linear span* of $\vec{r_1}, \cdots, \vec{r_m}$.  It coincides with $C(A^\mathsf{T}) \subset \mathbb{R}^n$
	2. **Column space** $C(A)$ of $A$ is the *linear span* of $\vec{c_1}, \cdots, \vec{c_n}$;  $C(A) \subset \mathbb{R}^m$
	3. **Nullspace** $N(A)$ of $A$ is the *solution set* of $Ax = 0$;  $N(A) \subset \mathbb{R}^n$
	4. **Left nullspace** $N(A^\mathsf{T})$ of $A$ is the *solution set* of $y^\mathsf{T} A = 0$;  $N(A^\mathsf{T}) \subset \mathbb{R}^m$

$dim\ R(A) = dim\ C(A) = rank(A)$
$dim\ N(A) = n_c - rank(A)$
$dim\ N(A^\mathsf{T}) = m_r - rank(A)$

##### Coordinate map
Let's fix a basis $S = (\vec{v_1}, \vec{v_2}, \cdots, \vec{v_n})$ of a vector space $V$, then every $\vec{x} \in V$ gets its unique coordinates $(c_1, c_2, \cdots, c_n)$ in basis $S$.
$\vec{x} = c_1 \vec{v_1} + c_2 \vec{v_2} + \cdots + c_n \vec{v_n}$

$T_S : \vec{x} \mapsto (c_1, c_2, \cdots, c_n)^\mathsf{T} \in \mathbb{R}^n$  is the **coordinate map** of $V$ in the basis $S$.

Let $V$ and $W$ be linear vector spaces. A mapping $T: V \mapsto W$ is:
* **linear** if for all $\vec{x}, \vec{y} \in V$ and all $a, b \in \mathbb{R}$:  $T(a\vec{x} + b\vec{y}) = aT(\vec{x}) + bT(\vec{y})$
* **isomorphism of** $V$ and $W$ if it is linear, and *both onto and one-to-one*.

One-to-one: $Tp_1 = Tp_2 \Rightarrow p_1 = p_2$
Onto: $T: V \mapsto W$, $Tv = w \in W$ $(\forall a \in V) (\exists b \in V) : {Tb = a \in W}$

##### Isomorphism
Let $V$ and $W$ be linear vector spaces. A mapping $T: V \mapsto W$ is:
* *linear* if for all $\vec{x}, \vec{y} \in V$ and all $a, b \in \mathbb{R}$:  $T(a\vec{x} + b\vec{y}) = aT(\vec{x}) + bT(\vec{y})$
* *isomorphism of* $V$ and $W$ if it is linear, and *both onto* (surjection) and *one-to-one* (injection).
	
* An *isomorphism* between two vector spaces $V$ and $W$ is a *bijection* $\phi:V \mapsto W$ which preserves scalar multiplication and vector addition, such that:
	* $\phi(\alpha \vec{v})=\alpha\phi(\vec{v})$ for all $\vec{v} \in V$ and $\alpha \in \mathbb{K}$;
	* $\phi(\vec{v}+\vec{u})=\phi(\vec{v})+\phi(\vec{u})$ for all $\vec{v}, \vec{u} \in V$.
* Here we assumed that $V$ and $W$ are both vector spaces over the same base field $\mathbb{K}$ (real or complex).
	
* Isomorphism allows to replace the object with the other of the same structure. For example, the vector space $\mathbb{P}_2=\{ax^2+bx+c\mid a,b,c \in \mathbb{R}\}$ of polynomials of degree at most $2$ is isomorphic to $\mathbb{R}^3$ (every polynomial $p(t)$ of degree $n$ can be uniquely identified with $n+1$ points on its curve).
* Isomorphism can be reversed. A vector space isomorphism is an invertible linear transformation. An isomorphism preserves the dimension of the vector space. 
	
* The mapping $V \mapsto \mathbb{R}^n$ and $x \mapsto [x]_B$ is an isomorphism of vector spaces.

* Two linear vector spaces $V$ and $W$ are said to be **isomorphic** if there is an isomorphism $T : V \mapsto W$.
* Coordinate map $T_S$ is an isomorphism between $V$ and $\mathbb{R}^n$

* Any two vector spaces of the same dimension are isomorphic.
* Up to isomorphism, $\mathbb{R}^n$ is the only $n$-dimensional vector space.
* The coordinate map of $\mathcal{P}_n$ to $\mathbb{R}^{n+1}$ is an isomorphism.


##### Change of basis
$\vec{c}\ ' = P_{S \mapsto S'} \vec{c}$,  where $P_{S \mapsto S'}$ is the **transition matrix** with columns equal to $T_{S'}(\vec{v_1}),\ T_{S'}(\vec{v_2}),\ \cdots,\ T_{S'}(\vec{v_n})$

*Computing the transition matrices in* $\mathbb{R}^n$
To find the transition matrix from *old basis* $S = (\vec{v_1}, \cdots, \vec{v_n})$to the *new basis* $S' = (\vec{v_1}', \cdots, \vec{v_n}')$, we have to:
1. Form a matrix $B$ with columns being the vector coordinates of $\vec{v_k}$ (in the standard basis $S_0 = (\vec{e_1}, \cdots, \vec{e_n})$)
2. Form a matrix $B'$ with columns being the vector coordinates of $\vec{v_k}'$ (in the standard basis $S_0 = (\vec{e_1}, \cdots, \vec{e_n})$)
3. Use elementary row transformations to get $(B' | B) \sim (I_n | P_{S \mapsto S'})$

$B = P_{S \mapsto S_0}$, $B' = P_{S' \mapsto S_0}$, thus $(B')^{-1} B = P_{S \mapsto S'}$

$P_{S' \to S_0} (\vec{x})_{S'} = \vec{x} = R_{S \to S_0} (\vec{x})_S$
$(\vec{x})_{S'} = (P_{S' \to S_0})^{-1}\ P_{S \to S_0}\ (\vec{x})_S$

