---
type: technical-term
title: "Matrix Rank"
aliases:
  - Rank
  - Rank of a Matrix
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
  - matrix-rank
sources:
  - "Strang, Introduction to Linear Algebra, 5th Edition, 2016"
related: []
projects: []
---
> [!abstract] Definition
> The rank of a matrix is the dimension of its column space.
>
> Equivalently, it is the dimension of its row space and the number of pivots in any row echelon form of the matrix.

## 1. Mathematical Definition

For $A\in\mathbb{F}^{m\times n}$:

$$
\operatorname{rank}(A)
=
\dim(\operatorname{Col}(A))
$$

The row-rank theorem states:

$$
\dim(\operatorname{Row}(A))
=
\dim(\operatorname{Col}(A))
$$

## 2. Rank Bounds

> [!important] Fundamental Bounds
> $$
> 0\leq\operatorname{rank}(A)\leq\min(m,n)
> $$
>
> The zero matrix has rank zero.

## 3. Computing Matrix Rank

> [!method] Row Reduction
> 1. Apply elementary row operations.
> 2. Transform the matrix into row echelon form.
> 3. Count the nonzero rows or pivot positions.
>
> $$
> \operatorname{rank}(A)
> =
> \text{number of pivots}
> $$

## 4. Full Rank

> [!definition] Full Row Rank
> $$
> \operatorname{rank}(A)=m
> $$
>
> The rows are linearly independent.

> [!definition] Full Column Rank
> $$
> \operatorname{rank}(A)=n
> $$
>
> The columns are linearly independent.

> [!important] Full Rank Square Matrix
> For a square $n\times n$ matrix:
>
> $$
> \operatorname{rank}(A)=n
> $$
>
> if and only if $A$ is invertible.

## 5. Rank and Linear Systems

For:

$$
A\mathbf{x}=\mathbf{b}
$$

the system is consistent if and only if:

$$
\operatorname{rank}(A)
=
\operatorname{rank}([A\mid\mathbf{b}])
$$

If consistent, the number of free variables is:

$$
n-\operatorname{rank}(A)
$$

where $n$ is the number of unknowns.

## 6. Rank-Nullity Theorem

> [!theorem] Rank-Nullity Theorem
> For a matrix $A\in\mathbb{F}^{m\times n}$:
>
> $$
> \operatorname{rank}(A)+
> \operatorname{nullity}(A)=n
> $$
>
> Here, nullity is the dimension of the null space of $A$.

## 7. Knowledge Relationships

### Foundation Knowledge
- **Matrices** — provides matrix structure.
- **Vectors and Vector Spaces** — provides linear independence and subspaces.
- **Elementary Row Operations** — provides rank-preserving reduction methods.
- **Row Echelon Form** — exposes pivot positions.

### Downstream Knowledge
- **Rank-Nullity Theorem** — relates rank to nullity.
- **Linear Systems** — uses rank to determine consistency and solution structure.
- **Matrix Factorization** — uses rank to characterize matrix structure.
- **Singular Value Decomposition** — provides a numerical framework for analyzing rank.

## 8. References

- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.
- Axler, Sheldon. *Linear Algebra Done Right*, 3rd Edition, 2015.