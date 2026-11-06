---
type: technical-term
title: "Linear Combinations"
aliases:
  - Linear Combination
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
  - linear-combinations
sources:
  - "Strang, Introduction to Linear Algebra, 5th Edition, 2016"
related: []
projects: []
---
> [!abstract] Definition
> A linear combination is an expression constructed by multiplying vectors by scalars and adding the resulting vectors.

## 1. Mathematical Formulation

Given vectors:
$$
\mathbf{v}_1,\mathbf{v}_2,\ldots,\mathbf{v}_n
$$
A linear combination is:

$$
\mathbf{v}
=
\alpha_1\mathbf{v}_1+
\alpha_2\mathbf{v}_2+
\cdots+
\alpha_n\mathbf{v}_n
$$

Where:

$$
\alpha_i\in\mathbb{F}
$$

The scalars $\alpha_i$ are called coefficients.

## 2. Example

Let:

$$
\mathbf{v}_1=
\begin{bmatrix}1\\0\end{bmatrix},
\qquad
\mathbf{v}_2=
\begin{bmatrix}0\\1\end{bmatrix}
$$

Choose coefficients $\alpha=2$ and $\beta=3$.

$$
2\mathbf{v}_1+3\mathbf{v}_2
=
\begin{bmatrix}2\\3\end{bmatrix}
$$

## 3. Matrix Representation

A linear combination can be expressed as a matrix-vector product:

$$
A\mathbf{x}
=
\begin{bmatrix}
|&|&&|\\
\mathbf{v}_1&\mathbf{v}_2&\cdots&\mathbf{v}_n\\
|&|&&|
\end{bmatrix}
\begin{bmatrix}
\alpha_1\\
\alpha_2\\
\vdots\\
\alpha_n
\end{bmatrix}
$$

The resulting vector belongs to the span of the given vectors.

## 4. Fundamental Properties

- Coefficients belong to the underlying scalar field.
- Linear combinations are closed under addition.
- Linear combinations are closed under scalar multiplication.
- The zero vector is a linear combination with all coefficients equal to zero.

## 5. Knowledge Relationships

### Foundation
- Vector Spaces — defines the allowed algebraic operations.
- Vectors — provides the elements being combined.

### Downstream
- Spanning Sets
- Linear Independence
- Basis
- Dimension
- Linear Systems

## 6. References

- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.