---
type: technical-term
title: Linear Transformations
aliases:
  - Linear Transformation
  - Linear Map
  - Linear Operator
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
  - linear-transformations
sources:
  - Axler, Linear Algebra Done Right, 3rd Edition, 2015
  - Strang, Introduction to Linear Algebra, 5th Edition, 2016
related:
  - "[[Kernel & Image]]"
  - "[[Change of Basis]]"
  - "[[Matrix Representation of Linear Transformations]]"
  - "[[Null Space and Column Space]]"
  - "[[Rank-Nullity Theorem]]"
projects: []
---
> [!abstract] Definition
> A linear transformation is a function between two vector spaces that preserves vector addition and scalar multiplication.
>
> Linear transformations describe structure-preserving mappings between vector spaces.

## 1. Mathematical Definition

> [!definition] Linearity
> Let $V$ and $W$ be vector spaces over the same field $\mathbb{F}$.
>
> A function:
>
> $$
> T:V\rightarrow W
> $$
>
> is linear if, for all $\mathbf{u},\mathbf{v}\in V$ and $\alpha,\beta\in\mathbb{F}$:
>
> $$
> T(\alpha\mathbf{u}+\beta\mathbf{v})
> =
> \alpha T(\mathbf{u})+\beta T(\mathbf{v})
> $$

## 2. Fundamental Properties

> [!important] Properties of Linear Transformations
> Every linear transformation satisfies:
>
> **Zero Preservation**
> $$
> T(\mathbf{0}_V)=\mathbf{0}_W
> $$
>
> **Additivity**
> $$
> T(\mathbf{u}+\mathbf{v})
> =
> T(\mathbf{u})+T(\mathbf{v})
> $$
>
> **Homogeneity**
> $$
> T(\alpha\mathbf{v})=\alpha T(\mathbf{v})
> $$

## 3. Composition

> [!definition] Composition of Linear Transformations
> Let:
>
> $$
> T:U\rightarrow V,\qquad S:V\rightarrow W
> $$
>
> Their composition is:
>
> $$
> S\circ T:U\rightarrow W
> $$
>
> defined by:
>
> $$
> (S\circ T)(\mathbf{u})=S(T(\mathbf{u}))
> $$
>
> The composition of two linear transformations is also linear.

## 4. Isomorphism

> [!definition] Linear Isomorphism
> A linear transformation is an isomorphism if it is bijective.
>
> Two vector spaces are isomorphic if there exists a linear isomorphism between them.
>
> Finite-dimensional vector spaces over the same field are isomorphic if and only if they have the same dimension.

## Content of Subject

- Kernel and Image
- Null Space and Column Space
- Matrix Representation of Linear Transformations
- Change of Basis
- Rank-Nullity Theorem

## Conceptual Structure

> [!abstract] Transformation Structure
> - Linear Transformations
> - Kernel and Image
> - Rank-Nullity Theorem

> [!abstract] Matrix Representation
> - Matrix Representation of Linear Transformations
> - Null Space and Column Space

> [!abstract] Coordinate Representation
> - Change of Basis

## Knowledge Relationships

### Foundation Knowledge

- **Vector Spaces** — defines the domain and codomain of linear transformations.
- **Vectors** — provides the elements mapped by transformations.
- **Linear Combinations** — linearity requires preservation of linear combinations.
- **Basis** — provides the coordinate systems used to represent transformations.
- **Matrices** — provides the algebraic representation of linear transformations.

### Downstream Knowledge

- **Eigenvalues and Eigenvectors** — studies vectors whose directions are preserved by linear transformations.
- **Diagonalization** — identifies bases in which certain transformations have diagonal matrix representations.
- **Similarity Transformations** — relates matrix representations of the same linear transformation under different bases.
- **Invariant Subspaces** — studies subspaces preserved by a linear transformation.
- **Singular Value Decomposition** — develops a structured representation of linear maps between finite-dimensional inner product spaces.

## References

- Axler, Sheldon. *Linear Algebra Done Right*, 3rd Edition, 2015.
- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.
- Hoffman, Kenneth, and Ray Kunze. *Linear Algebra*, 2nd Edition, 1971.