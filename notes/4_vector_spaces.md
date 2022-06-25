##### Vector spaces
A **linear vector space $V$** is a set of vectors $u, v, w ...$  with 2 operations:
	1. Addition $V \times V \rightarrow V$
	2. Multiplication by scalar: $\mathbb{R} \times V \rightarrow V$

satisfying the following properties:
	- Commutative: $u + v = v + u$
	- Associative: $(u + v) + w = u + (v + w) \quad c(du) = (cd)u$
	- Additive zero: $\exists\ zero\ vector\ 0\ in\ V\ s.t.\ u + 0 = 0 + u = u$
	- Additive inverse: $\forall v \in V, \exists (-v) \in V s.t. -v + v = 0$
	- Distributive: $c(u + v) = cu + cv \quad (c + d)u = cu + du$
	- Multiplicative identity: $1 \cdot u = u$
	- $0 \cdot u = 0$
	- $k \cdot 0 = 0$
	- $(-1) \cdot u = (- u)$
	- if $k \cdot u = 0$, then either $k = 0$ or $u = 0$

$V = \{\vec{0}\}$ is the smallest vector space

A **vector subspace** is a non-empty subset $W$ of a vector space $V$ if it is closed under vector addition and multiplication by scalars:  if $u, v \in W$ and $k \in \mathbb{R}$, then $v + u \in W$ and $k \cdot v \in W$
* $\vec{0}$ always belongs to a subspace
* $\{\vec{0}\}$ is the smallest subspace
* A subspace of a linear space is a linear space by itself

* $C(AB) \subset C(A)$
* $A$ is non-singular $\implies C(A) = C(AB)$

##### Linear spans and combinations
A **linear combination** of vectors $v_1, v_2, ..., v_k$ in a vector space $V$ is a vector of the form $c_1v_1 + c_2v_2 + \dots + c_kv_k$ with any scalars $c_1, c_2, \dots, c_k$

A **linear span** $ls\{S\}$ of a set $S \subset V$  is the collection of all finite linear combinations of vectors from $S$

1. For any subset $S$ of a vector space $V$, $ls(S)$ is a subspace of $V$
2. If $W$ is a subspace of $V$ containing $S$, then $ls(S) \subset W$
3. $ls(S)$ is the smallest subspace of $V$ containing $S$
4. $ls(ls(S)) = ls(S)$

$ls(S_1) = ls(S_2)$ if and only if:
1. Every $v_1 \in S_1$ belongs to $ls(S_2)$
and
2. Every $v_2 \in S_2$ belongs to $ls(S_1)$

##### Linear independence
The set $S$ of vectors of a vector space $V$ is called **linearly independent** if no nontrivial linear combination of vectors from $S$ equals  $\vec{0}$.

* A set $S$ is linearly independent $\iff$ no vector in $S$ is a linear combination of the other vectors in $S$.
