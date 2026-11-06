---
type: technical-term
title: "Inner Products"
aliases:
  - Inner Product
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
> An **inner product** is a function that assigns a scalar to every pair of vectors in a vector space and satisfies positivity, definiteness, linearity, and conjugate symmetry.
>
> It provides the mathematical foundation for measuring vector lengths, defining angles, and expressing orthogonality.

## 1. Mathematical Definition

> [!definition] Inner Product
> Let $V$ be a vector space over $\mathbb{F}$, where $\mathbb{F}=\mathbb{R}$ or $\mathbb{C}$.
>
> An inner product is a function
>
> $$\langle\cdot,\cdot\rangle:V\times V\rightarrow\mathbb{F}$$
>
> satisfying the following axioms for all $u,v,w\in V$ and $a\in\mathbb{F}$.

> [!important] Inner Product Axioms
> **1. Conjugate Symmetry**
>
> $$\langle u,v\rangle=\overline{\langle v,u\rangle}$$
>
> For real vector spaces, this becomes symmetry:
>
> $$\langle u,v\rangle=\langle v,u\rangle$$
>
> **2. Linearity in the First Argument**
>
> $$\langle au+v,w\rangle=a\langle u,w\rangle+\langle v,w\rangle$$
>
> **3. Conjugate Linearity in the Second Argument**
>
> $$\langle u,av+w\rangle=\overline{a}\langle u,v\rangle+\langle u,w\rangle$$
>
> **4. Positive Definiteness**
>
> $$\langle v,v\rangle\geq 0$$
>
> and
>
> $$\langle v,v\rangle=0\iff v=0$$
>
> In complex spaces, $\langle v,v\rangle$ is real and nonnegative.

## 2. Standard Examples

> [!example] Euclidean Inner Product
> For $u,v\in\mathbb{R}^n$:
>
> $$\langle u,v\rangle=u^Tv=\sum_{i=1}^{n}u_iv_i$$
>
> This is the standard dot product.

> [!example] Complex Inner Product
> For $u,v\in\mathbb{C}^n$, under the convention of linearity in the first argument:
>
> $$\langle u,v\rangle=\sum_{i=1}^{n}u_i\overline{v_i}$$
>
> Complex conjugation ensures that $\langle v,v\rangle$ is real and nonnegative.

> [!example] Weighted Inner Product
> Let $W$ be a real symmetric positive-definite matrix. Define:
>
> $$\langle u,v\rangle_W=u^TWv$$
>
> This produces an inner product that assigns different geometric weights to different directions.

## 3. Properties

> [!important] Cauchy-Schwarz Inequality
> $$|\langle u,v\rangle|\leq\|u\|\|v\|$$
>
> Equality holds if and only if $u$ and $v$ are linearly dependent.

> [!important] Orthogonality
> Two vectors are orthogonal if and only if:
>
> $$\langle u,v\rangle=0$$

> [!important] Induced Norm
> Every inner product defines a norm:
>
> $$\|v\|=\sqrt{\langle v,v\rangle}$$

> [!note] Parallelogram Identity
> Every inner-product-induced norm satisfies:
>
> $$\|u+v\|^2+\|u-v\|^2=2\|u\|^2+2\|v\|^2$$
>
> This identity is also used to characterize norms that arise from inner products.

## 4. Gram Matrix Representation

> [!definition] Gram Matrix
> Given vectors $v_1,\ldots,v_k$ in an inner product space, their Gram matrix is:
>
> $$G_{ij}=\langle v_i,v_j\rangle$$
>
> Thus:
>
> $$G=
> \begin{bmatrix}
> \langle v_1,v_1\rangle & \cdots & \langle v_1,v_k\rangle\\
> \vdots & \ddots & \vdots\\
> \langle v_k,v_1\rangle & \cdots & \langle v_k,v_k\rangle
> \end{bmatrix}$$
>
> A Gram matrix is Hermitian and positive semidefinite. It is positive definite exactly when the vectors are linearly independent.

## 5. Knowledge Relationships

### Foundation Knowledge
- **Vector Spaces** — define the algebraic structure on which an inner product operates.
- **Complex Numbers** — relevant when defining inner products over complex vector spaces.

### Downstream Knowledge
- **Norms** — are induced directly by inner products.
- **Orthogonality** — is defined through a zero inner product.
- **Orthogonal Projections** — use inner products to compute components along subspaces.
- **Gram Matrices** — encode pairwise inner products of vector collections.

## 6. References
1. Axler, Sheldon. *Linear Algebra Done Right*. 3rd ed., Springer, 2015.
2. Strang, Gilbert. *Introduction to Linear Algebra*. 5th ed., Wellesley-Cambridge Press, 2016.