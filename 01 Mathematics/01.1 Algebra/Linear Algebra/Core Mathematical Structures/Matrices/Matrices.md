---
type: technical-term
title: Matrices
aliases:
  - Matrix
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
  - matrices
sources:
  - Strang, Introduction to Linear Algebra, 5th Edition, 2016
related:
  - "[[Matrix Operations]]"
  - "[[Matrix Multiplication]]"
  - "[[Matrix Transpose]]"
  - "[[Matrix Inverse]]"
  - "[[Matrix Rank]]"
  - "[[Elementary Row Operations]]"
  - "[[Reduced Row Echelon Form]]"
  - "[[Row Echelon Form]]"
projects: []
---
> [!abstract] Definition
> A matrix is a rectangular array of elements arranged in rows and columns. In linear algebra, its entries usually belong to a scalar field such as $\mathbb{R}$ or $\mathbb{C}$.

## 1. Mathematical Representation

> [!definition] General Matrix
> An $m\times n$ matrix is written as:
>
> $$
> A=
> \begin{bmatrix}
> a_{11}&a_{12}&\cdots&a_{1n}\\
> a_{21}&a_{22}&\cdots&a_{2n}\\
> \vdots&\vdots&\ddots&\vdots\\
> a_{m1}&a_{m2}&\cdots&a_{mn}
> \end{bmatrix}
> \in\mathbb{F}^{m\times n}
> $$
>
> Where:
> - $m$: Number of rows.
> - $n$: Number of columns.
> - $a_{ij}$: Entry in row $i$, column $j$.
> - $\mathbb{F}$: Underlying scalar field.

## 2. Matrix Classification

> [!info] Common Matrix Types
> - **Row matrix:** A matrix with one row.
> - **Column matrix:** A matrix with one column.
> - **Square matrix:** A matrix with equal numbers of rows and columns.
> - **Zero matrix:** Every entry is zero.
> - **Diagonal matrix:** All off-diagonal entries are zero.
> - **Identity matrix:** A diagonal matrix whose diagonal entries are all one.
> - **Upper triangular matrix:** Entries below the main diagonal are zero.
> - **Lower triangular matrix:** Entries above the main diagonal are zero.
> - **Symmetric matrix:** $A^T=A$.
> - **Skew-symmetric matrix:** $A^T=-A$.

## 3. Identity Matrix

> [!definition] Identity Matrix
> The $n\times n$ identity matrix is:
>
> $$
> I_n=
> \begin{bmatrix}
> 1&0&\cdots&0\\
> 0&1&\cdots&0\\
> \vdots&\vdots&\ddots&\vdots\\
> 0&0&\cdots&1
> \end{bmatrix}
> $$
>
> It satisfies:
>
> $$
> AI_n=A,\qquad I_mA=A
> $$
>
> whenever the matrix dimensions are compatible.

## 4. Matrix Equality

> [!definition] Equality
> Two matrices $A,B\in\mathbb{F}^{m\times n}$ are equal if and only if:
>
> $$
> a_{ij}=b_{ij}
> $$
>
> for every valid pair of indices $(i,j)$.

## 5. Important Distinctions

> [!warning] Matrix Versus Linear Transformation
> A matrix is an array of scalar entries. A linear transformation is a function between vector spaces that preserves linear combinations.
>
> A matrix can represent a linear transformation after bases have been selected, but the two concepts are not identical.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Vectors and Vector Spaces** — provides the vector and scalar structures used in linear algebra.
- **Fields and Number Systems** — establishes the domain of matrix entries.

### Downstream Knowledge
- **Matrix Operations** — defines algebraic operations on matrices.
- **Matrix Multiplication** — develops matrix products.
- **Matrix Transpose** — studies row-column interchange.
- **Matrix Inverse** — studies multiplicative inverses.
- **Matrix Rank** — measures the dimension of the column space and row space.

## 7. References

- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.
- Meyer, Carl D. *Matrix Analysis and Applied Linear Algebra*, 2000.