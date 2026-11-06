---
type: technical-term
title: "Matrix Transpose"
aliases:
  - Transpose
  - Transposed Matrix
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
  - matrix-transpose
sources:
  - "Strang, Introduction to Linear Algebra, 5th Edition, 2016"
related: []
projects: []
---
> [!abstract] Definition
> The transpose of a matrix is obtained by interchanging its rows and columns.
>
> The transpose of $A$ is denoted by $A^T$.

## 1. Mathematical Definition

For:

$$
A=[a_{ij}]\in\mathbb{F}^{m\times n}
$$

its transpose is:

$$
A^T=[a_{ji}]\in\mathbb{F}^{n\times m}
$$

## 2. Example

$$
A=
\begin{bmatrix}
1&2&3\\
4&5&6
\end{bmatrix}
$$

$$
A^T=
\begin{bmatrix}
1&4\\
2&5\\
3&6
\end{bmatrix}
$$

## 3. Fundamental Properties

> [!important] Transpose Identities
> **Double Transpose**
> $$
> (A^T)^T=A
> $$
>
> **Transpose of a Sum**
> $$
> (A+B)^T=A^T+B^T
> $$
>
> **Scalar Multiplication**
> $$
> (\alpha A)^T=\alpha A^T
> $$
>
> **Transpose of a Product**
> $$
> (AB)^T=B^TA^T
> $$

> [!warning] Order Reversal
> The transpose of a product reverses the order of its factors.

## 4. Special Matrix Properties

> [!definition] Symmetric Matrix
> A square matrix is symmetric if:
>
> $$
> A^T=A
> $$

> [!definition] Skew-Symmetric Matrix
> A square matrix is skew-symmetric if:
>
> $$
> A^T=-A
> $$

## 5. Knowledge Relationships

### Foundation Knowledge
- **Matrices** — defines matrix dimensions and entries.
- **Matrix Operations** — provides matrix algebra.

### Downstream Knowledge
- **Symmetric Matrices** — studies matrices invariant under transposition.
- **Orthogonal Matrices** — uses transpose as the inverse.
- **Inner Product Spaces** — connects transpose to matrix representations of inner products.
- **Matrix Inverse** — establishes transpose-inverse identities.

## 6. References

- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.
- Meyer, Carl D. *Matrix Analysis and Applied Linear Algebra*, 2000.