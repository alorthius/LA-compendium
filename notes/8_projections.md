##### Orthogonal decomposition
Assume $W$ is a subspace of a vector space $V$ with scalar product $\langle \cdot, \cdot \rangle$. Then for all $\vec{v} \in V$ there exist unique $\vec{w_1} \in W$ and $\vec{w_2} \in W^\perp$ such that $\vec{v} = \vec{w_1} + \vec{w_2}$

Let $V = W \oplus W^\perp$ and $\vec{v} = \vec{w_1} + \vec{w_2}$ with $\vec{w_1} \in W$ and $\vec{w_2} \in W^\perp$. Then:
* $\vec{w_1}$ is the **orthogonal projection** of $\vec{v}$ on $W$
* $\vec{w_2}$ is the **orthogonal projection** of $\vec{v}$ on $W^\perp$

$P_j : \vec{v} \mapsto \vec{w_j}$ is the **orthogonal projector** onto $W$ or $W^\perp$

**Properties of projectors** $P_j$:
1. *Linearity:*  $P_j (a \vec{u} + b \vec{v}) = a P_j(\vec{u}) + bP_j(\vec{v})$
2. *Idempotent:*  $P_j^2 = P_j$
3. *Orthogonality:*  $P_1 P_2 = P_2 P_1 = 0$
4. *Completeness:*  $P_1 + P_2 = I$

5. $\vec{w_1} = P_1 \vec{v}$ is the vector in $W$ that is closest to $\vec{v}$
6. $\vec{w_2} = P_2 \vec{v}$ is the vector in $W^\perp$ that is closest to $\vec{v}$

The **projection matrix** $P$ onto the line in direction $\vec{a} \in \mathbb{R}^m$: $P = \frac{\vec{a} \vec{a}^T}{\vec{a}^T \vec{a}}$
$\vec{p} = P \vec{b}$, where
* $\vec{b}$ is the vector of which we want to find the projection
* $\vec{p}$ is the projection vector of $\vec{b}$
$trace(P) = 1$


##### Least squares solutions
* **best (least square) solution:**  $\vec{x_0} = (A^\mathsf{T} A)^{-1} A^\mathsf{T} \vec{b}$
* **the closest vector** $A \vec{x_0}$ = projection of $\vec{b}$ onto $C(A)$:  $P \vec{b} = A \cdot \vec{x_0} = A \cdot (A^\mathsf{T} A)^{-1} A^\mathsf{T} \vec{b}$
* **projection matrix:**  $P = A \cdot (A^\mathsf{T} A)^{-1} A^\mathsf{T}$

![](img/img_5.png)
