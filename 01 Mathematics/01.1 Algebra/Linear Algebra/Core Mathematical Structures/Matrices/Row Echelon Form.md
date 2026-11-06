---
type: technical-term
title: "Row Echelon Form"
aliases:
  - REF
  - Echelon Form
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
  - row-echelon-form
sources:
  - "Strang, Introduction to Linear Algebra, 5th Edition, 2016"
related: []
projects: []
---
> [!abstract] Definition
> A matrix is in row echelon form (REF) if its nonzero rows are above all zero rows and the leading entry of each nonzero row is strictly to the right of the leading entry in the row above it.
>
> Every entry below a leading entry must be zero.

## 1. Formal Conditions

A matrix is in REF if:

> [!important] REF Conditions
> 1. All zero rows are located below nonzero rows.
> 2. The leading entry of each nonzero row is to the right of the leading entry in the row above.
> 3. All entries below each leading entry are zero.

## 2. Example

$$
\begin{bmatrix}
1&2&3&4\\
0&2&5&6\\
0&0&3&7\\
0&0&0&0
\end{bmatrix}
$$

This matrix is in REF.

## 3. Pivot Positions

> [!definition] Pivot
> A pivot is the leading nonzero entry of a nonzero row in echelon form.
>
> The number of pivots equals the rank of the matrix.

## 4. Properties

- Every matrix can be transformed into REF using elementary row operations.
- REF is generally not unique.
- The number of nonzero rows in REF equals the rank.
- REF supports back substitution when solving linear systems.

## 5. Applications

- Gaussian elimination.
- Computing matrix rank.
- Identifying pivot and free variables.
- Determining consistency of linear systems.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Matrices** — provides matrix structure.
- **Elementary Row Operations** — provides the transformations used to obtain REF.

### Downstream Knowledge
- **Reduced Row Echelon Form** — adds stronger normalization conditions.
- **Matrix Rank** — derives rank from pivot positions.
- **Linear Systems** — uses REF for back substitution.

## 7. References

- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.
- Lay, Lay, and McDonald. *Linear Algebra and Its Applications*, 5th Edition, 2016.