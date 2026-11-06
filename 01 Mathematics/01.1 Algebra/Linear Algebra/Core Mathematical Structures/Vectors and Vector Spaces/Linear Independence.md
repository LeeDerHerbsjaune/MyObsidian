---
type: technical-term
title: "Linear Independence"
aliases:
  - Linearly Independent Vectors
  - Linear Dependence
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
  - linear-independence
sources:
  - "Axler, Linear Algebra Done Right, 3rd Edition, 2015"
related: []
projects: []
---
> [!abstract] Definition
> A set of vectors is linearly independent if the only linear combination that produces the zero vector is the trivial combination, in which every coefficient equals zero.

## 1. Mathematical Formulation

Given vectors:

$$
\mathbf{v}_1,\ldots,\mathbf{v}_n
$$

They are linearly independent if:

$$
\alpha_1\mathbf{v}_1+\cdots+
\alpha_n\mathbf{v}_n=\mathbf{0}
$$

implies:

$$
\alpha_1=\cdots=\alpha_n=0
$$

## 2. Linear Dependence

> [!definition] Linear Dependence
> A vector set is linearly dependent if there exists a nontrivial linear combination that produces the zero vector.
>
> $$
> \sum_{i=1}^{n}\alpha_i\mathbf{v}_i=\mathbf{0}
> $$
>
> where at least one coefficient is nonzero.

## 3. Geometric Interpretation

For two vectors in $\mathbb{R}^2$:

- Independent vectors span a two-dimensional plane.
- Dependent vectors lie along the same line through the origin, provided neither is zero.

## 4. Matrix Criterion

Place the vectors as columns of a matrix:

$$
A=
\begin{bmatrix}
|&|&&|\\
\mathbf{v}_1&\mathbf{v}_2&\cdots&\mathbf{v}_n\\
|&|&&|
\end{bmatrix}
$$

The vectors are linearly independent if and only if:

$$
A\mathbf{x}=\mathbf{0}
$$

has only the trivial solution.

Equivalently:

$$
\operatorname{rank}(A)=n
$$

## 5. Important Properties

- Any set containing the zero vector is dependent.
- Any subset of an independent set is independent.
- Any superset of a dependent set is dependent.
- More than $n$ vectors in an $n$-dimensional vector space must be dependent.

## 6. Knowledge Relationships

### Foundation
- Vector Spaces
- Linear Combinations
- Systems of Linear Equations

### Downstream
- Spanning Sets
- Basis
- Dimension
- Matrix Rank

## 7. References

- Axler, Sheldon. *Linear Algebra Done Right*, 3rd Edition, 2015.
- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.