---
type: technical-term
title: "Orthonormal Bases"
aliases:
  - Orthonormal Basis
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
> An **orthonormal basis** is a basis consisting of mutually orthogonal unit vectors.
>
> It combines linear independence, spanning, orthogonality, and unit length into a particularly convenient coordinate system.

## 1. Mathematical Definition

> [!definition] Orthonormal Set
> A set of vectors $\{q_1,\ldots,q_n\}$ is orthonormal if:
>
> $$\langle q_i,q_j\rangle=\delta_{ij}$$
>
> where $\delta_{ij}$ is the Kronecker delta:
>
> $$\delta_{ij}=
> \begin{cases}
> 1,&i=j\\
> 0,&i\neq j
> \end{cases}$$
>
> An orthonormal basis is an orthonormal set that spans the vector space.

## 2. Coordinate Representation

> [!important] Orthonormal Coordinates
> Let $\{q_1,\ldots,q_n\}$ be an orthonormal basis of $V$.
>
> Every vector $v\in V$ can be represented as:
>
> $$v=\sum_{i=1}^{n}\langle v,q_i\rangle q_i$$
>
> Its coordinates are therefore:
>
> $$[v]_{\mathcal B}=
> \begin{bmatrix}
> \langle v,q_1\rangle\\
> \vdots\\
> \langle v,q_n\rangle
> \end{bmatrix}$$
>
> The inner product with each basis vector directly gives the corresponding coordinate.

## 3. Matrix Representation

> [!definition] Orthonormal Column Matrix
> Let $Q$ be a matrix whose columns form an orthonormal set:
>
> $$Q=[q_1\ q_2\ \cdots\ q_k]$$
>
> Then:
>
> $$Q^TQ=I_k$$
>
> For complex matrices, the corresponding condition is:
>
> $$Q^*Q=I_k$$
>
> where $Q^*$ denotes the conjugate transpose.

> [!important] Square Orthogonal Matrix
> If $Q$ is square and real, then:
>
> $$Q^TQ=QQ^T=I$$
>
> Therefore:
>
> $$Q^{-1}=Q^T$$
>
> A square complex matrix satisfying the analogous condition is called unitary.

## 4. Important Properties

> [!important] Parseval's Identity
> For an orthonormal basis:
>
> $$\|v\|^2=\sum_{i=1}^{n}|\langle v,q_i\rangle|^2$$
>
> The squared norm equals the sum of the squared magnitudes of the coordinates.

> [!important] Inner Product Preservation
> If $u$ and $v$ are represented in an orthonormal basis, then:
>
> $$\langle u,v\rangle=[u]_{\mathcal B}^*[v]_{\mathcal B}$$
>
> Thus, orthonormal coordinates preserve the inner-product structure.

> [!note] Existence
> Every finite-dimensional inner product space has an orthonormal basis.
>
> Such a basis can be constructed from any basis using the Gram-Schmidt process.

## 5. Knowledge Relationships

### Foundation Knowledge
- **Inner Products** — define the unit-length and orthogonality conditions.
- **Orthogonality** — establishes pairwise perpendicularity.
- **Basis and Dimension** — provide the spanning and independence requirements.

### Downstream Knowledge
- **Orthogonal Matrices** — arise when square real matrices have orthonormal columns.
- **QR Factorization** — represents a matrix using orthonormal columns and an upper triangular factor.
- **Spectral Theorem** — provides orthonormal eigenbases for real symmetric and complex Hermitian matrices.

## 6. References
1. Axler, Sheldon. *Linear Algebra Done Right*. 3rd ed., Springer, 2015.
2. Strang, Gilbert. *Introduction to Linear Algebra*. 5th ed., Wellesley-Cambridge Press, 2016.