---
type: technical-term
title: "Vector Spaces"
aliases:
  - Vector Space
  - Linear Space
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
  - mathematics
  - linear-algebra
  - vector-spaces
sources:
  - "Axler, Linear Algebra Done Right, 3rd Edition, 2015"
  - "Friedberg, Insel, and Spence, Linear Algebra, 4th Edition, 2003"
related: []
projects: []
---
> [!abstract] Definition
> A vector space is a nonempty set equipped with vector addition and scalar multiplication satisfying eight algebraic axioms.
>
> It is defined over a field $\mathbb{F}$, whose elements serve as scalars.

## 1. Mathematical Structure

$$
(V,+,\cdot,\mathbb{F})
$$

- $V$: Set of vectors.
- $+$: Vector addition.
- $\cdot$: Scalar multiplication.
- $\mathbb{F}$: Scalar field.

## 2. Vector Space Axioms

For $\mathbf{u},\mathbf{v},\mathbf{w}\in V$ and $\alpha,\beta\in\mathbb{F}$:

> [!important] Addition Axioms
> **Commutativity**
> $$
> \mathbf{u}+\mathbf{v}=\mathbf{v}+\mathbf{u}
> $$
>
> **Associativity**
> $$
> (\mathbf{u}+\mathbf{v})+\mathbf{w}
> =
> \mathbf{u}+(\mathbf{v}+\mathbf{w})
> $$
>
> **Additive Identity**
> $$
> \mathbf{v}+\mathbf{0}=\mathbf{v}
> $$
>
> **Additive Inverse**
> $$
> \mathbf{v}+(-\mathbf{v})=\mathbf{0}
> $$

> [!important] Scalar Multiplication Axioms
> **Compatibility**
> $$
> \alpha(\beta\mathbf{v})=(\alpha\beta)\mathbf{v}
> $$
>
> **Scalar Identity**
> $$
> 1\mathbf{v}=\mathbf{v}
> $$
>
> **Distributivity over Vector Addition**
> $$
> \alpha(\mathbf{u}+\mathbf{v})
> =
> \alpha\mathbf{u}+\alpha\mathbf{v}
> $$
>
> **Distributivity over Scalar Addition**
> $$
> (\alpha+\beta)\mathbf{v}
> =
> \alpha\mathbf{v}+\beta\mathbf{v}
> $$

## 3. Examples

- Coordinate spaces: $\mathbb{R}^n$
- Polynomial spaces: $P_n(\mathbb{R})$
- Matrix spaces: $M_{m\times n}(\mathbb{R})$
- Function spaces: $\mathbb{R}^X$
- Sequence spaces.

## 4. Fundamental Properties

- The zero vector is unique.
- Every vector has a unique additive inverse.
- $0\mathbf{v}=\mathbf{0}$.
- $\alpha\mathbf{0}=\mathbf{0}$.
- $(-1)\mathbf{v}=-\mathbf{v}$.

## 5. Knowledge Relationships

### Foundation
- Set Theory — defines sets and subsets.
- Abstract Algebra — provides groups and fields.
- Number Systems — establishes scalar fields.

### Downstream
- Subspaces
- Linear Combinations
- Linear Independence
- Spanning Sets
- Basis
- Dimension
- Linear Transformations

## 6. References

- Axler, Sheldon. *Linear Algebra Done Right*, 3rd Edition, 2015.
- Friedberg, Insel, and Spence. *Linear Algebra*, 4th Edition, 2003.