---
type: technical-term
title: "Spanning Sets"
aliases:
  - Spanning Set
  - Span
  - Linear Span
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
  - spanning-sets
sources:
  - "Axler, Linear Algebra Done Right, 3rd Edition, 2015"
related: []
projects: []
---
> [!abstract] Definition
> A spanning set is a collection of vectors whose linear combinations generate every vector in a given vector space or subspace.

## 1. Mathematical Formulation

Given:

$$
S=\{\mathbf{v}_1,\ldots,\mathbf{v}_n\}
$$

The span of $S$ is:

$$
\operatorname{span}(S)
=
\left\{
\sum_{i=1}^{n}\alpha_i\mathbf{v}_i
\mid
\alpha_i\in\mathbb{F}
\right\}
$$

A set $S$ spans $V$ if:

$$
\operatorname{span}(S)=V
$$

## 2. Examples

The standard basis vectors:

$$
\mathbf{e}_1=
\begin{bmatrix}1\\0\end{bmatrix},
\qquad
\mathbf{e}_2=
\begin{bmatrix}0\\1\end{bmatrix}
$$

span $\mathbb{R}^2$ because:

$$
\begin{bmatrix}x\\y\end{bmatrix}
=
x\mathbf{e}_1+y\mathbf{e}_2
$$

## 3. Properties of Span

> [!important] Fundamental Properties
> - The span of a set is a subspace.
> - Every set spans its own span.
> - Adding vectors cannot decrease the span.
> - Removing redundant vectors may preserve the span.
> - The empty set spans the zero subspace.

## 4. Column Space

For a matrix $A$:

$$
A=
\begin{bmatrix}
|&|&&|\\
\mathbf{a}_1&\mathbf{a}_2&\cdots&\mathbf{a}_n\\
|&|&&|
\end{bmatrix}
$$

Its column space is:

$$
\operatorname{Col}(A)
=
\operatorname{span}
\{\mathbf{a}_1,\ldots,\mathbf{a}_n\}
$$

## 5. Knowledge Relationships

### Foundation
- Vectors
- Vector Spaces
- Linear Combinations

### Downstream
- Linear Independence
- Basis
- Dimension
- Column Space
- Matrix Rank

## 6. References

- Axler, Sheldon. *Linear Algebra Done Right*, 3rd Edition, 2015.