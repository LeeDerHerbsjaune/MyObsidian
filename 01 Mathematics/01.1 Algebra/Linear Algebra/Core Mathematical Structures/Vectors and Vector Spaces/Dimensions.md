---
type: technical-term
title: "Dimension"
aliases:
  - Vector Space Dimension
  - Dimension of a Vector Space
field:
  - Mathematics
subfield:
  - Linear Algebra
status: learning
confidence: 1
created: 2026-11-04
updated: 2026-11-04
tags:
  - mathematics
  - linear-algebra
  - dimension
sources:
  - "Axler, Linear Algebra Done Right, 3rd Edition, 2015"
related: []
projects: []
---
> [!abstract] Definition
> The dimension of a finite-dimensional vector space is the number of vectors in any basis of that space.
>
> It measures the number of independent directions required to represent every vector in the space.

## 1. Mathematical Formulation

If:

$$
B=\{\mathbf{b}_1,\ldots,\mathbf{b}_n\}
$$

is a basis of $V$, then:

$$
\dim(V)=n
$$

## 2. Examples

$$
\dim(\mathbb{R})=1
$$

$$
\dim(\mathbb{R}^2)=2
$$

$$
\dim(\mathbb{R}^3)=3
$$

For polynomial spaces:

$$
\dim(P_n(\mathbb{R}))=n+1
$$

For matrix spaces:

$$
\dim(M_{m\times n}(\mathbb{R}))=mn
$$

The zero vector space has dimension zero.

## 3. Dimension Theorem

> [!theorem] Invariance of Dimension
> Every basis of a finite-dimensional vector space contains the same number of vectors.
>
> This guarantees that dimension is well-defined.

## 4. Subspace Dimension

If $W$ is a subspace of a finite-dimensional vector space $V$:

$$
\dim(W)\leq\dim(V)
$$

## 5. Dimension Formula

For finite-dimensional subspaces $U$ and $W$:

$$
\dim(U+W)
=
\dim(U)+\dim(W)-\dim(U\cap W)
$$

If their sum is direct:

$$
\dim(U\oplus W)
=
\dim(U)+\dim(W)
$$

## 6. Finite and Infinite Dimensions

> [!important] Classification
> **Finite-dimensional:** Has a finite basis.
>
> **Infinite-dimensional:** Has no finite basis.
>
> For example:
>
> $$
> \mathbb{R}[x]
> $$
>
> the space of all real polynomials, is infinite-dimensional.

## 7. Knowledge Relationships

### Foundation
- Vector Spaces
- Linear Independence
- Spanning Sets
- Basis

### Downstream
- Rank-Nullity Theorem
- Matrix Rank
- Linear Transformations
- Direct Sums
- Quotient Vector Spaces

## 8. References

- Axler, Sheldon. *Linear Algebra Done Right*, 3rd Edition, 2015.
- Friedberg, Insel, and Spence. *Linear Algebra*, 4th Edition, 2003.