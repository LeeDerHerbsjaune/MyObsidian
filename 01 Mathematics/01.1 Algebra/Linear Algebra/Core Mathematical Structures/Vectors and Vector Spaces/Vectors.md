---
type: technical-term
title: "Vectors"
aliases:
  - Vector
  - Mathematical Vectors
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
  - vectors
sources:
  - "Axler, Linear Algebra Done Right, 3rd Edition, 2015"
  - "Strang, Introduction to Linear Algebra, 5th Edition, 2016"
related: []
projects: []
---
> [!abstract] Definition
> A vector is an element of a vector space over a field. It is a mathematical object that can participate in vector addition and scalar multiplication.
>
> Vectors may represent geometric displacements, ordered tuples, matrices, polynomials, functions, or other abstract mathematical objects.

> [!important] Vector Representation
> In an n-dimensional coordinate space, a vector can be represented as:
>
> $$
> \mathbf{v}=
> \begin{bmatrix}
> v_1\\v_2\\\vdots\\v_n
> \end{bmatrix}
> $$
>
> Its coordinates depend on the selected basis, whereas the abstract vector does not.

## 1. Vector Operations

> [!definition] Vector Addition
> $$
> \mathbf{u}+\mathbf{v}
> =
> \begin{bmatrix}
> u_1+v_1\\
> \vdots\\
> u_n+v_n
> \end{bmatrix}
> $$

> [!definition] Scalar Multiplication
> $$
> \alpha\mathbf{v}
> =
> \begin{bmatrix}
> \alpha v_1\\
> \vdots\\
> \alpha v_n
> \end{bmatrix}
> $$

## 2. Geometric Properties

> [!important] Scope Qualification
> Magnitude, direction, and angle require additional geometric structures.

> [!definition] Euclidean Norm
> $$
> \|\mathbf{v}\|_2=
> \sqrt{\sum_{i=1}^{n}v_i^2}
> $$

> [!definition] Unit Vector
> $$
> \hat{\mathbf{v}}=
> \frac{\mathbf{v}}{\|\mathbf{v}\|_2},
> \qquad \mathbf{v}\neq\mathbf{0}
> $$

## 3. Fundamental Properties

- Zero vector: $\mathbf{0}$
- Additive inverse: $-\mathbf{v}$
- Vector equality: equality of elements.
- Vector addition is associative and commutative.
- Scalar multiplication is distributive.

## 4. Knowledge Relationships

### Foundation
- Vector Spaces — defines the algebraic structure containing vectors.
- Set Theory — provides the language for mathematical objects.
- Number Systems — establishes scalar fields.

### Downstream
- Vector Operations — develops vector arithmetic.
- Linear Combinations — studies combinations of vectors.
- Normed Vector Spaces — introduces vector magnitude.
- Inner Product Spaces — introduces angles and orthogonality.

## 5. References

- Axler, Sheldon. *Linear Algebra Done Right*, 3rd Edition, 2015.
- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.