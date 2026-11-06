---
type: technical-term
title: "Orthogonal Projections"
aliases:
  - Orthogonal Projection
abbreviation: ""
field:
  - Mathematics
subfield:
  - Linear Algebra
status: learning
confidence: 1
created: 2026-11-04
updated: 2026-11-04
tags:
  - technical-term
  - linear-algebra
  - inner-product-spaces
sources:
  - "Axler, Sheldon. Linear Algebra Done Right. 3rd ed., 2015."
  - "Strang, Gilbert. Introduction to Linear Algebra. 5th ed., 2016."
related: []
projects: []
---

> [!abstract] Definition
> An **orthogonal projection** maps a vector onto a subspace such that the difference between the original vector and its projection is orthogonal to that subspace.
>
> It provides the mathematical foundation for decomposing vectors into components parallel and perpendicular to a subspace.

## 1. Mathematical Definition

> [!definition] Orthogonal Projection onto a Subspace
> Let $V$ be a finite-dimensional inner product space and let $W\subseteq V$ be a subspace.
>
> The orthogonal projection of $v\in V$ onto $W$ is the unique vector $p\in W$ satisfying:
>
> $$v-p\in W^\perp$$
>
> Equivalently:
>
> $$\langle v-p,w\rangle=0
> \quad\text{for all }w\in W$$

> [!important] Orthogonal Decomposition
> Every vector $v\in V$ can be uniquely decomposed as:
>
> $$v=p+e$$
>
> where:
> - $p\in W$ is the projection of $v$ onto $W$.
> - $e\in W^\perp$ is the orthogonal residual.
>
> Therefore:
>
> $$V=W\oplus W^\perp$$

## 2. Projection onto an Orthonormal Basis

> [!important] Projection Formula
> Let $\{q_1,\ldots,q_k\}$ be an orthonormal basis of $W$.
>
> The projection of $v$ onto $W$ is:
>
> $$\operatorname{proj}_W(v)
> =\sum_{i=1}^{k}\langle v,q_i\rangle q_i$$
>
> The residual is:
>
> $$e=v-\operatorname{proj}_W(v)$$

## 3. Matrix Representation

> [!definition] Projection Matrix
> Let $Q\in\mathbb{R}^{m\times k}$ have orthonormal columns spanning $W$:
>
> $$Q^TQ=I_k$$
>
> The projection of $b\in\mathbb{R}^m$ onto the column space of $Q$ is:
>
> $$p=QQ^Tb$$
>
> Therefore, the orthogonal projection matrix is:
>
> $$P=QQ^T$$

> [!note] General Full-Column-Rank Matrix
> If $A\in\mathbb{R}^{m\times k}$ has linearly independent columns, but its columns are not necessarily orthonormal, then:
>
> $$P=A(A^TA)^{-1}A^T$$
>
> This matrix projects onto $\operatorname{Col}(A)$.

## 4. Properties of Projection Matrices

> [!important] Idempotence
> $$P^2=P$$
>
> Projecting a vector onto the same subspace more than once does not change the result.

> [!important] Symmetry
> For real orthogonal projections:
>
> $$P^T=P$$
>
> For complex inner product spaces:
>
> $$P^*=P$$

> [!important] Eigenvalues
> The eigenvalues of an orthogonal projection matrix are either:
>
> $$\lambda\in\{0,1\}$$
>
> Vectors in the projected subspace correspond to eigenvalue $1$, while vectors in its orthogonal complement correspond to eigenvalue $0$.

> [!important] Rank and Trace
> For an orthogonal projection matrix:
>
> $$\operatorname{rank}(P)=\operatorname{tr}(P)=\dim W$$

## 5. Best Approximation Property

> [!important] Projection Theorem
> The orthogonal projection $p$ of $v$ onto $W$ is the unique vector in $W$ minimizing the distance to $v$:
>
> $$p=\underset{w\in W}{\operatorname{argmin}}\ \|v-w\|$$
>
> The residual $v-p$ is orthogonal to every vector in $W$.
>
> This property is fundamental to least-squares approximation.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Inner Products** — define the orthogonality condition.
- **Orthogonality** — defines the relationship between the projected component and residual.
- **Subspaces** — provide the target spaces onto which vectors are projected.
- **Orthonormal Bases** — simplify projection calculations.

### Downstream Knowledge
- **Least Squares** — solves approximation problems through orthogonal projection.
- **QR Factorization** — provides a computational method for projection and least-squares problems.
- **Projection Matrices** — form a useful matrix-theoretic representation of projections.

## 7. References
1. Axler, Sheldon. *Linear Algebra Done Right*. 3rd ed., Springer, 2015.
2. Strang, Gilbert. *Introduction to Linear Algebra*. 5th ed., Wellesley-Cambridge Press, 2016.