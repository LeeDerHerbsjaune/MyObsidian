---
type: technical-term
title: "Elementary Row Operations"
aliases:
  - Row Operations
  - Elementary Row Transformations
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
  - row-operations
sources:
  - "Strang, Introduction to Linear Algebra, 5th Edition, 2016"
related: []
projects: []
---
> [!abstract] Definition
> Elementary row operations are three reversible operations performed on the rows of a matrix.
>
> They are used to simplify matrices while preserving the solution set of the corresponding homogeneous or augmented linear system.

## 1. Three Elementary Row Operations

> [!definition] Type I — Row Interchange
> Exchange two rows:
>
> $$
> R_i\leftrightarrow R_j
> $$

> [!definition] Type II — Row Scaling
> Multiply a row by a nonzero scalar:
>
> $$
> R_i\leftarrow\alpha R_i,
> \qquad \alpha\neq 0
> $$

> [!definition] Type III — Row Replacement
> Add a scalar multiple of one row to another:
>
> $$
> R_i\leftarrow R_i+\alpha R_j
> $$

## 2. Elementary Matrices

> [!definition] Elementary Matrix
> An elementary matrix is obtained by applying one elementary row operation to an identity matrix.
>
> Applying a row operation to $A$ is equivalent to left multiplication:
>
> $$
> EA
> $$
>
> where $E$ is the corresponding elementary matrix.

## 3. Reversibility

> [!important] Invertibility
> Every elementary row operation is reversible.
>
> Therefore, every elementary matrix is invertible.

## 4. Row Equivalence

> [!definition] Row-Equivalent Matrices
> Two matrices are row-equivalent if one can be transformed into the other through a finite sequence of elementary row operations.
>
> Row-equivalent matrices have the same row space, rank, and homogeneous solution set.

## 5. Applications

- Solving systems of linear equations.
- Computing matrix rank.
- Obtaining row echelon form.
- Obtaining reduced row echelon form.
- Computing matrix inverses using Gauss–Jordan elimination.

<LearningViz type_id="ELEMENTARY_ROW_OPERATIONS" />

## 6. Knowledge Relationships

### Foundation Knowledge
- **Matrices** — defines rows and matrix structure.
- **Matrix Operations** — provides algebraic manipulation.
- **Linear Systems** — explains why row operations preserve solutions.

### Downstream Knowledge
- **Row Echelon Form** — uses row operations to produce a structured matrix.
- **Reduced Row Echelon Form** — applies row operations to obtain a canonical form.
- **Matrix Rank** — counts pivots after reduction.
- **Matrix Inverse** — uses row reduction to calculate inverses.

## 7. References

- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.
- Meyer, Carl D. *Matrix Analysis and Applied Linear Algebra*, 2000.