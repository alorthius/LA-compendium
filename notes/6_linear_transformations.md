##### Mapping $T : \mathbb{R}^n \mapsto \mathbb{R}^m$
A mapping $T : \mathbb{R}^n \mapsto \mathbb{R}^m$ is **linear** if:
$\forall \alpha_1, \alpha_2 \in \mathbb{R}$, $\vec{x_1}, \vec{x_2} \in \mathbb{R}^n$ : $T(\alpha_1 \vec{x_1} + \alpha_2 \vec{x_2}) = \alpha_1 T(\vec{x_1}) + \alpha_2 T(\vec{x_2})$ 
In particular, $T(0)$ is a zero vector of $\mathbb{R}^m$


Let $\vec{e_1}, \cdots, \vec{e_n}$ be the standard basis  of $\mathbb{R}^n$ and $\vec{u_j} := T(\vec{e_j})$, and $A$ be the $m \times n$ matrix with columns $\vec{u_1}, \cdots, \vec{u_n}$. Then:
$$
\forall \vec{x} \in \mathbb{R}^n \quad:\quad T(\vec{x}) = A\vec{x}
$$
Every linear transformation between $\mathbb{R}^n$ and $\mathbb{R}^m$ amounts to multiplication by the matrix $A$.  $T = T_A \leftrightarrow A$


##### Mapping $T : V \mapsto W$
A mapping $T : V \mapsto W$ is **linear** if:
$\forall \alpha_1, \alpha_2 \in \mathbb{R}$, $\vec{u_1}, \vec{u_2} \in V$ : $T(\alpha_1 \vec{u_1} + \alpha_2 \vec{u_2}) = \alpha_1 T(\vec{u_1}) + \alpha_2 T(\vec{u_2}) \in W$ 
In particular, $T(0)$ is a zero vector $\vec{0_W}$ of $W$.


Let $\vec{v_1}, \cdots, \vec{v_n}$ be a basis of $V$ and $\vec{w_1}, \cdots, \vec{w_m}$ a basis of $W$. Set $\vec{u_j} := (T(\vec{v_j}))_W$ and denote be $A$ the $m \times n$ matrix with columns $\vec{u_1}, \cdots, \vec{u_2}$. Then:
$$
\forall \vec{v} \in V \quad:\quad (T(\vec{v}))_W = A(\vec{v})_V
$$

##### Composition mapping
If  $T_1 : \mathbb{R}^m \mapsto \mathbb{R}^k$  and  $T_2 : \mathbb{R}^k \mapsto \mathbb{R}^n$  are linear transformations, then their **composition** $T_2 \circ T_1 : \mathbb{R}^m \mapsto \mathbb{R}^n$  is given by:
$$
(T_2 \circ T_1) \cdot (\vec{x}) = T_2(T_1(\vec{x}))
$$
If $T_1$ has matrix $A \in M_{k \times m}(\mathbb{R})$ and $T_2$ has matrix $B \in M_{n \times k}(\mathbb{R})$, then the matrix of $T_2 \circ T_1$ is $BA$

Assume that
* $\vec{u_1}, \cdots, \vec{u_n}$ are linearly independent vectors in $\mathbb{R}^n$ (are basis vectors $S$)
* $\vec{v_1}, \cdots, \vec{v_n}$ are arbitrary vectors in $\mathbb{R}^m$
Then there exists a unique linear transformation $T : \mathbb{R}^n \mapsto \mathbb{R}^m$ such that $T(\vec{u_j}) = \vec{v_j}$ for all $j = 1, \cdots, n$.

##### Linear transformations in different bases
$$
A = P_{S_0 \rightarrow S}\ A_0\ P_{S \rightarrow S_0}
$$where:
* $P_{S_0 \to S}$ is the transition matrix,
* $P_{S_0 \to S} = (P_{S \to S_0})^{-1}$
* $A_0$ is the matrix in linear transformation in the initial basis $S_0$
* $S$ is the new basis

$$
P_{S \to S_0}\ c = x
c = (P_{S \to S_0})^{-1}\ x
$$
where $c$ is the coordinate vector.