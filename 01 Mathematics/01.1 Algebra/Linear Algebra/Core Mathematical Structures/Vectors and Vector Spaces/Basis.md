---
type: technical-term
title: "Basis"
aliases:
  - Vector Space Basis
  - Basis Vectors
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
  - basis
sources:
  - "Axler, Linear Algebra Done Right, 3rd Edition, 2015"
related: []
projects: []
---

# Basis

> [!abstract] Definition
> A basis of a vector space is a set of vectors that is both linearly independent and spans the entire vector space.
>
> A basis provides a minimal and nonredundant generating set for a vector space.

## 1. Mathematical Formulation

A set:

$$
B=\{\mathbf{b}_1,\ldots,\mathbf{b}_n\}
$$

is a basis of $V$ if:

**Spanning Condition**

$$
\operatorname{span}(B)=V
$$

**Linear Independence Condition**

$$
\sum_{i=1}^{n}\alpha_i\mathbf{b}_i=\mathbf{0}
\Rightarrow
\alpha_i=0
$$

## 2. Standard Basis

The standard basis of $\mathbb{R}^3$ is:

$$
B=
\left\{
\begin{bmatrix}1\\0\\0\end{bmatrix},
\begin{bmatrix}0\\1\\0\end{bmatrix},
\begin{bmatrix}0\\0\\1\end{bmatrix}
\right\}
$$

## 3. Coordinate Representation

Every vector in a finite-dimensional vector space has a unique representation relative to a fixed basis.

$$
\mathbf{v}
=
\alpha_1\mathbf{b}_1+\cdots+
\alpha_n\mathbf{b}_n
$$

Its coordinate vector is:

$$
[\mathbf{v}]_B=
\begin{bmatrix}
\alpha_1\\
\vdots\\
\alpha_n
\end{bmatrix}
$$

## 4. Basis Properties

- Every finite-dimensional vector space has a basis.
- Every basis of a finite-dimensional vector space has the same number of elements.
- A basis is linearly independent.
- A basis spans the entire space.
- A basis is not necessarily unique.

## 5. Basis Extension Theorem

> [!theorem] Basis Extension
> Every linearly independent subset of a finite-dimensional vector space can be extended to a basis.

## 6. Knowledge Relationships

### Foundation
- Vector Spaces
- Linear Combinations
- Linear Independence
- Spanning Sets

### Downstream
- Dimension
- Coordinate Representation
- Change of Basis
- Linear Transformations
- Matrix Representation

## 7. References

- Axler, Sheldon. *Linear Algebra Done Right*, 3rd Edition, 2015.