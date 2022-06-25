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


##### Normal equation
** Formulation of the problem**
* We are solving the general least squares problem: given $m \times n$ matrix $A$ and $b \in \mathbb{R}^m$ with $m > n$ (the system $Ax=b$ is overdetermined), find such vector $x \in \mathbb{R}^n$, that $||Ax-b||^2$ is minimized. The problem is that $b$ is not in the column space of $A$ (its range), so we should project $b$ onto $A$'s range.
	
** Derivation of the normal equation**
	1. $b = b_{proj} + (b-b_{proj})$ : 
	2. $b_{proj}$ is the projection of $b$ onto $Col(A)$, and
		* the other part (residual vector) is orthogonal to the column $Col(A) \implies$ is orthogonal to $Row(A^\top) \implies$ is in the nullspace $Null(A^\top)$;
		* To get rid of the vector in the nullspace of $A^\top$, we just multiply both sides of the equation by $A^\top$:
	3. $A^\top Ax = A^\top b$ - is a *normal equation*.
		It always has a solution because $A^\top b \in Col(A^\top A)=Col(A^\top)$ , and $A^\top Ax \in Col(A^\top A)$
	4. As long as columns of $A$ are linearly independent, $A^\top A$ is a square matrix and an invertible matrix, we can multiply each side by $A(A^\top A)^{-1}$:
	5. $Ax=A(A^\top A)^{-1}A^\top b = b_{proj}$, and $A(A^\top A)^{-1}A^\top$ is the projection matrix.
	
** Solvability of normal equation**
	* $A^\top Ax = A^\top b$ - is a *normal equation*.
	1. It always has a solution because $A^\top b \in Col(A^\top A)=Col(A^\top)$ , and $A^\top Ax \in Col(A^\top A)$
	2. If $rank(A)=n$ ($A$ has linearly independent columns), the normal equation has a unique solution. 
