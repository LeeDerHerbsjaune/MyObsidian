---
type: technical-term
title: "Orthogonality"
aliases:
  - Orthogonal Vectors
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
> **Orthogonality** is the relationship between vectors whose inner product is zero.
>
> In Euclidean geometry, orthogonal vectors are perpendicular. In abstract inner product spaces, orthogonality generalizes this geometric concept.

## 1. Mathematical Definition

> [!definition] Orthogonal Vectors
> Two vectors $u,v\in V$ are orthogonal if:
>
> $$\langle u,v\rangle=0$$
>
> This relationship is written:
>
> $$u\perp v$$

> [!note] Zero Vector
> The zero vector is orthogonal to every vector because:
>
> $$\langle 0,v\rangle=0$$
>
> However, the zero vector does not have a defined angle with another vector.

## 2. Orthogonal Sets

> [!definition] Orthogonal Set
> A set of vectors $\{v_1,\ldots,v_k\}$ is orthogonal if:
>
> $$\langle v_i,v_j\rangle=0\quad\text{for }i\neq j$$
>
> An orthogonal set of nonzero vectors is automatically linearly independent.

> [!important] Linear Independence of Orthogonal Vectors
> Suppose:
>
> $$c_1v_1+\cdots+c_kv_k=0$$
>
> Taking the inner product with $v_j$ gives:
>
> $$c_j\langle v_j,v_j\rangle=0$$
>
> Since $v_j\neq 0$, positive definiteness implies $c_j=0$.
>
> Therefore, all coefficients are zero, so the vectors are linearly independent.

## 3. Orthogonal Complement

> [!definition] Orthogonal Complement
> For a subspace $W\subseteq V$, its orthogonal complement is:
>
> $$W^\perp=\{v\in V:\langle v,w\rangle=0\text{ for all }w\in W\}$$
>
> The orthogonal complement contains every vector orthogonal to the entire subspace.

> [!important] Finite-Dimensional Decomposition
> If $V$ is finite-dimensional and has an inner product, then:
>
> $$V=W\oplus W^\perp$$
>
> Consequently:
>
> $$\dim W+\dim W^\perp=\dim V$$
>
> This means every vector can be uniquely decomposed into a component in $W$ and a component in $W^\perp$.

## 4. Orthogonality and Pythagorean Theorem

> [!important] Pythagorean Identity
> If $u\perp v$, then:
>
> $$\|u+v\|^2=\|u\|^2+\|v\|^2$$
>
> More generally:
>
> $$\|u+v\|^2=\|u\|^2+\|v\|^2+2\operatorname{Re}\langle u,v\rangle$$
>
> Under the real inner product convention, the final term becomes $2\langle u,v\rangle$.

## 5. Orthogonal Vectors and Bases

> [!important] Orthogonal Basis
> An orthogonal basis is a basis whose distinct vectors are pairwise orthogonal.
>
> An orthogonal basis is linearly independent by the orthogonality property.

> [!note] Orthonormal Basis
> An orthonormal basis is an orthogonal basis in which every vector has unit norm.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Inner Products** — define orthogonality.
- **Vector Spaces and Subspaces** — provide the algebraic structures on which orthogonality is considered.

### Downstream Knowledge
- **Orthonormal Bases** — normalize orthogonal basis vectors.
- **Orthogonal Projections** — use orthogonality to define the closest vector in a subspace.
- **Orthogonal Complements** — characterize the subspace perpendicular to a given subspace.

## 7. References
1. Axler, Sheldon. *Linear Algebra Done Right*. 3rd ed., Springer, 2015.
2. Strang, Gilbert. *Introduction to Linear Algebra*. 5th ed., Wellesley-Cambridge Press, 2016.