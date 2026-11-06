---
type: technical-term
title: "Matrix Inverse"
aliases:
  - Inverse Matrix
  - Multiplicative Inverse of a Matrix
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
  - matrix-inverse
sources:
  - "Strang, Introduction to Linear Algebra, 5th Edition, 2016"
related: []
projects: []
---
> [!abstract] Definition
> The inverse of a square matrix $A$ is a matrix $A^{-1}$ that produces the identity matrix when multiplied by $A$ from either side.
>
> A matrix has an inverse if and only if it is nonsingular.

## 1. Mathematical Definition

> [!definition] Inverse Matrix
> For a square matrix $A\in\mathbb{F}^{n\times n}$:
>
> $$
> AA^{-1}=A^{-1}A=I_n
> $$
>
> The matrix $A^{-1}$ is called the inverse of $A$.

## 2. Inverse of a 2 × 2 Matrix

For:

$$
A=
\begin{bmatrix}
a&b\\
c&d
\end{bmatrix}
$$

if $ad-bc\neq 0$, then:

$$
A^{-1}
=
\frac{1}{ad-bc}
\begin{bmatrix}
d&-b\\
-c&a
\end{bmatrix}
$$

## 3. Invertibility Conditions

> [!important] Invertible Matrix Theorem
> For a square matrix $A\in\mathbb{F}^{n\times n}$, the following conditions are equivalent:
>
> - $A$ is invertible.
> - $A\mathbf{x}=\mathbf{0}$ has only the trivial solution.
> - The columns of $A$ are linearly independent.
> - The columns of $A$ span $\mathbb{F}^n$.
> - $\operatorname{rank}(A)=n$.
> - $A$ has a pivot in every row and column.
> - $\det(A)\neq 0$.

## 4. Inverse Properties

> [!important] Fundamental Identities
> **Inverse of an Inverse**
> $$
> (A^{-1})^{-1}=A
> $$
>
> **Inverse of a Product**
> $$
> (AB)^{-1}=B^{-1}A^{-1}
> $$
>
> **Inverse of a Transpose**
> $$
> (A^T)^{-1}=(A^{-1})^T
> $$
>
> **Scalar Multiple**
> $$
> (\alpha A)^{-1}=\frac{1}{\alpha}A^{-1},
> \qquad \alpha\neq 0
> $$

## 5. Computing the Inverse

> [!method] Gauss–Jordan Elimination
> Construct the augmented matrix:
>
> $$
> [A\mid I_n]
> $$
>
> Apply elementary row operations until the left side becomes the identity:
>
> $$
> [A\mid I_n]\longrightarrow[I_n\mid A^{-1}]
> $$
>
> If the left side cannot be reduced to $I_n$, the matrix is singular.

<LearningViz type_id="MATRIX_INVERSE_2D" />

## 6. Computational Considerations

> [!warning] Numerical Practice
> Explicitly computing $A^{-1}$ is often unnecessary when solving $A\mathbf{x}=\mathbf{b}$.
>
> Numerical algorithms commonly use factorizations and linear-system solvers instead of forming the inverse directly.

## 7. Knowledge Relationships

### Foundation Knowledge
- **Matrices** — establishes square matrices and identity matrices.
- **Matrix Multiplication** — defines the product used in the inverse identity.
- **Elementary Row Operations** — provides a method for computing inverses.

### Downstream Knowledge
- **Determinants** — provides an equivalent invertibility criterion for square matrices.
- **Linear Systems** — uses inverses to express solutions when they exist uniquely.
- **Orthogonal Matrices** — a special class whose inverse equals its transpose.
- **Matrix Factorization** — provides practical computational methods.

## 8. References

- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.
- Meyer, Carl D. *Matrix Analysis and Applied Linear Algebra*, 2000.