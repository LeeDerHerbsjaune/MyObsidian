---
type: technical-term
title: "Subspaces"
aliases:
  - Subspace
  - Vector Subspace
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
  - subspaces
sources:
  - "Axler, Linear Algebra Done Right, 3rd Edition, 2015"
related: []
projects: []
---
# Subspaces

> [!abstract] Definition
> A subspace is a subset of a vector space that is itself a vector space under the same vector addition and scalar multiplication operations.

## 1. Mathematical Definition

Let $V$ be a vector space over $\mathbb{F}$.

A subset $W\subseteq V$ is a subspace if:

$$
W\leq V
$$

Here, $W\leq V$ denotes that $W$ is a vector subspace of $V$.

## 2. Subspace Criterion

> [!important] Subspace Test
> A nonempty subset $W\subseteq V$ is a subspace if:
> 
>**Non-emptiness / Zero Vector:** The zero vector $\mathbf{0}$ of V must be in W (which also proves W is non-empty).
>$$
>\mathbf{0} \in W
>$$
>
> **Closure under Addition**: For any vectors $\mathbf{u}, \mathbf{v} \in w$,  their sum  $\mathbf{u}+\mathbf{v}$ must also be in .
> $$
> \mathbf{u},\mathbf{v}\in W
> \Rightarrow
> \mathbf{u}+\mathbf{v}\in W
> $$
>
> **Closure under Scalar Multiplication**
> $$
> \mathbf{v}\in W,\ \alpha\in\mathbb{F}
> \Rightarrow
> \alpha\mathbf{v}\in W
> $$

## 3. Examples

> [!example] Plane Through the Origin
> Consider:
>
> $$
> W=
> \left\{
> \begin{bmatrix}x\\y\\z\end{bmatrix}
> \in\mathbb{R}^3
> \mid x+y+z=0
> \right\}
> $$
>
> This is a subspace of $\mathbb{R}^3$.

> [!example] Trivial Subspaces
> Every vector space contains:
>
> - Zero subspace: $\{\mathbf{0}\}$
> - Entire space: $V$

> [!warning] Common Mistake
> A plane that does not pass through the origin is not a subspace because it does not contain the zero vector.

## 4. Fundamental Properties

- The intersection of subspaces is a subspace.
- The sum of two subspaces is a subspace.
- The union of two subspaces is generally not a subspace.
- Every subspace contains the zero vector.

## 5. Knowledge Relationships

### Foundation
- Vector Spaces — provides the parent algebraic structure.
- Vector Operations — defines the operations inherited by a subspace.

### Downstream
- Linear Combinations
- Spanning Sets
- Basis
- Dimension
- Quotient Vector Spaces

## 6. References

- Axler, Sheldon. *Linear Algebra Done Right*, 3rd Edition, 2015.