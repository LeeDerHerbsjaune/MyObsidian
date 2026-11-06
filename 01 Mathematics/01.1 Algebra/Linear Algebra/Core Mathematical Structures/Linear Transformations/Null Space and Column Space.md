---
type: technical-term
title: "Null Space and Column Space"
aliases:
  - Null Space
  - Column Space
  - Kernel of a Matrix
  - Image of a Matrix
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
  - null-space
  - column-space
sources:
  - "Strang, Introduction to Linear Algebra, 5th Edition, 2016"
related: []
projects: []
---
> [!abstract] Definition
> The null space and column space are fundamental subspaces associated with a matrix.
>
> - The **null space** contains all input vectors mapped to zero by the matrix.
> - The **column space** contains all vectors that can be expressed as linear combinations of the matrix columns.

## 1. Null Space

> [!definition] Null Space
> For a matrix $A\in\mathbb{F}^{m\times n}$:
>
> $$
> \operatorname{Null}(A)
> =
> \{\mathbf{x}\in\mathbb{F}^n\mid A\mathbf{x}=\mathbf{0}\}
> $$
>
> It is a subspace of the input space $\mathbb{F}^n$.

<LearningViz type_id="NULL_SPACE" />

## 2. Column Space

> [!definition] Column Space
> Let the columns of $A$ be $\mathbf{a}_1,\ldots,\mathbf{a}_n$.
>
> The column space is:
>
> $$
> \operatorname{Col}(A)
> =
> \operatorname{span}
> \{\mathbf{a}_1,\ldots,\mathbf{a}_n\}
> $$
>
> It is a subspace of $\mathbb{F}^m$.

<LearningViz type_id="COLUMN_SPACE" />

## 3. Example

Consider:

$$
A=
\begin{bmatrix}
1&2\\
2&4
\end{bmatrix}
$$

> [!example] Null Space
> Solve:
>
> $$
> A\mathbf{x}=\mathbf{0}
> $$
>
> This gives:
>
> $$
> x_1+2x_2=0
> $$
>
> Therefore:
>
> $$
> \operatorname{Null}(A)
> =
> \operatorname{span}
> \left\{
> \begin{bmatrix}-2\\1\end{bmatrix}
> \right\}
> $$

> [!example] Column Space
> The columns are:
>
> $$
> \mathbf{a}_1=
> \begin{bmatrix}1\\2\end{bmatrix},
> \qquad
> \mathbf{a}_2=
> \begin{bmatrix}2\\4\end{bmatrix}
> $$
>
> Since $\mathbf{a}_2=2\mathbf{a}_1$:
>
> $$
> \operatorname{Col}(A)
> =
> \operatorname{span}
> \left\{
> \begin{bmatrix}1\\2\end{bmatrix}
> \right\}
> $$

## 4. Fundamental Properties

> [!important] Dimensions
> For $A\in\mathbb{F}^{m\times n}$:
>
> $$
> \dim(\operatorname{Col}(A))
> =
> \operatorname{rank}(A)
> $$
>
> $$
> \dim(\operatorname{Null}(A))
> =
> \operatorname{nullity}(A)
> $$

> [!important] Subspace Locations
> $$
> \operatorname{Null}(A)\leq\mathbb{F}^n
> $$
>
> $$
> \operatorname{Col}(A)\leq\mathbb{F}^m
> $$

## 5. Important Distinction

> [!warning] Row Reduction and Column Space
> Elementary row operations preserve the solution set of $A\mathbf{x}=\mathbf{0}$ and therefore preserve the null space.
>
> However, row operations generally change the column space as a subspace of $\mathbb{F}^m$.
>
> To determine a basis for the original column space, identify pivot columns using an echelon form, then select the corresponding columns from the original matrix.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Matrices** — defines the matrix and its columns.
- **Linear Combinations** — defines the span of matrix columns.
- **Linear Independence** — determines independent columns.
- **Elementary Row Operations** — provides methods for solving homogeneous systems.

### Downstream Knowledge
- **Kernel and Image** — gives the abstract transformation-level interpretation.
- **Matrix Rank** — measures the dimension of the column space.
- **Rank-Nullity Theorem** — relates nullity and rank.
- **Linear Systems** — uses null spaces to describe homogeneous solution sets.

## 7. References

- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.
- Lay, Lay, and McDonald. *Linear Algebra and Its Applications*, 5th Edition, 2016.