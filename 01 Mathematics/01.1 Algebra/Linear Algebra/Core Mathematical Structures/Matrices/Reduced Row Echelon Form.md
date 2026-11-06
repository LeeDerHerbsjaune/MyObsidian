---
type: technical-term
title: "Reduced Row Echelon Form"
aliases:
  - RREF
  - Reduced Echelon Form
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
  - reduced-row-echelon-form
sources:
  - "Strang, Introduction to Linear Algebra, 5th Edition, 2016"
related: []
projects: []
---
> [!abstract] Definition
> Reduced row echelon form (RREF) is a special form of row echelon form in which every pivot is equal to one and is the only nonzero entry in its column.

## 1. Formal Conditions

> [!important] RREF Conditions
> A matrix is in RREF if it satisfies all REF conditions and:
>
> 1. Every pivot equals one.
> 2. Every pivot is the only nonzero entry in its column.

## 2. Example

$$
\begin{bmatrix}
1&0&2&0\\
0&1&-3&0\\
0&0&0&1\\
0&0&0&0
\end{bmatrix}
$$

This matrix is in RREF.

## 3. Relationship with REF

> [!important] Comparison
> **REF**
> - Pivots need not equal one.
> - Entries above pivots may be nonzero.
> - The form is generally not unique.
>
> **RREF**
> - Every pivot equals one.
> - Every pivot column has zeros elsewhere.
> - The RREF of a matrix is unique.

## 4. Computing RREF

> [!method] Gauss–Jordan Elimination
> 1. Use elementary row operations to create pivots.
> 2. Scale each pivot to one.
> 3. Eliminate entries below each pivot.
> 4. Eliminate entries above each pivot.
>
> The result is RREF.

## 5. Uniqueness Theorem

> [!theorem] Uniqueness of RREF
> Every matrix is row-equivalent to exactly one reduced row echelon form.
>
> Consequently, the RREF is independent of the particular valid sequence of elementary row operations.

## 6. Applications

- Solving systems of linear equations.
- Identifying pivot and free variables.
- Determining matrix rank.
- Computing matrix inverses.
- Identifying linear dependence among columns.

## 7. Knowledge Relationships

### Foundation Knowledge
- **Matrices** — provides matrix structure.
- **Elementary Row Operations** — provides the reversible operations used in reduction.
- **Row Echelon Form** — establishes the weaker echelon conditions.

### Downstream Knowledge
- **Matrix Rank** — counts pivots.
- **Matrix Inverse** — uses RREF of an augmented matrix.
- **Linear Systems** — expresses solution sets in terms of pivot and free variables.
- **Null Space** — can be determined from the reduced system.

## 8. References

- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.
- Lay, Lay, and McDonald. *Linear Algebra and Its Applications*, 5th Edition, 2016.