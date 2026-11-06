---
type: technical-term
title: "Gauss-Jordan Elimination"
aliases:
  - Gauss–Jordan Elimination
abbreviation: ""
field:
  - Mathematics
subfield:
  - Linear Algebra
status: learning
confidence: 1
created: 2026-11-04
updated: 2026-11-04
tags:
  - technical-term
  - linear-algebra
  - elimination-methods
sources:
  - "Lay, David C., Linear Algebra and Its Applications, 5th ed., 2016."
related: []
projects: []
---

> [!abstract] Definition
> **Gauss–Jordan elimination** is a matrix elimination algorithm that applies elementary row operations to transform an augmented matrix into reduced row echelon form (RREF).
>
> Unlike Gaussian elimination, it eliminates entries both below and above each pivot, allowing solutions to be read directly from the resulting matrix without back substitution.

## 1. Mathematical Foundation

> [!important] Elementary Row Operations
> Gauss–Jordan elimination uses the same three elementary row operations as Gaussian elimination:
>
> 1. Row interchange.
> 2. Multiplication of a row by a nonzero scalar.
> 3. Addition of a multiple of one row to another row.
>
> Each operation preserves the solution set of the corresponding system.

## 2. Reduced Row Echelon Form

> [!abstract] Definition
> A matrix is in **reduced row echelon form (RREF)** if:
>
> 1. It is already in row echelon form.
> 2. Every pivot is equal to $1$.
> 3. Every pivot is the only nonzero entry in its column.
>
> In particular, all entries both above and below each pivot are zero.

## 3. Gauss–Jordan Elimination Procedure

> [!example] General Algorithm
> Given an augmented matrix $[A\mid\mathbf{b}]$:
>
> 1. Construct the augmented matrix.
> 2. Select a nonzero pivot in the leftmost available column.
> 3. Interchange rows if necessary.
> 4. Scale the pivot row so that the pivot equals $1$.
> 5. Eliminate all other entries in the pivot column.
> 6. Move to the next pivot position.
> 7. Repeat until the matrix reaches RREF.
> 8. Read the solution directly from the resulting matrix, identifying any free variables.

## 4. Interpretation of the Result

> [!important] Solution Extraction
> In the RREF of an augmented matrix:
>
> - A row representing $0=c$, where $c\neq0$, indicates inconsistency.
> - A pivot in every variable column indicates a unique solution if the system is consistent.
> - One or more non-pivot variable columns indicate free variables and infinitely many solutions if the system is consistent.
>
> RREF exposes the pivot and free variables directly.

## 5. Important Properties

> [!important] Properties
> - Gauss–Jordan elimination preserves the solution set.
> - Every matrix has exactly one RREF.
> - The number of pivots equals the rank of the matrix.
> - The RREF of a matrix reveals its pivot columns and free-variable columns.
> - Gauss–Jordan elimination does not require back substitution.
>
> The uniqueness of RREF makes it useful for comparing equivalent matrices.

## 6. Gaussian vs. Gauss–Jordan Elimination

> [!note] Comparison
> | Property | Gaussian Elimination | Gauss–Jordan Elimination |
> |---|---|---|
> | Target form | REF | RREF |
> | Elimination | Below pivots | Above and below pivots |
> | Pivot normalization | Not required | Required |
> | Final solution step | Back substitution | Direct reading |
> | Reduced form unique? | No | Yes |
>
> Gauss–Jordan elimination performs additional elimination operations after reaching REF.

## 7. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Matrices:** Provides the matrix representation of a system.
> - **Elementary Row Operations:** Defines the transformations used in elimination.
> - **Row Echelon Form:** Provides the intermediate structure before RREF.

> [!info] Relevant
> - **Gaussian Elimination:** Provides the closely related elimination procedure.
> - **Matrix Rank:** Determines the number of pivots.

### Downstream Knowledge

> [!info] Relevant
> - **Consistency and Solution Sets:** RREF makes solution classification explicit.
> - **Homogeneous Linear Systems:** RREF reveals the structure of the null space.
> - **Matrix Inverse:** Gauss–Jordan elimination can be used to compute inverses of nonsingular square matrices by reducing $[A\mid I]$.

## 8. References

> [!bibliography]
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., 2016.
> - Strang, Gilbert. *Introduction to Linear Algebra*, 6th ed., 2023.