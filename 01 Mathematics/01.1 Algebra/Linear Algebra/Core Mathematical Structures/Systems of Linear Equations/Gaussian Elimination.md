---
type: technical-term
title: "Gaussian Elimination"
aliases: []
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
> **Gaussian elimination** is a systematic algorithm for solving linear systems by applying elementary row operations to an augmented matrix until it reaches row echelon form (REF).
>
> The resulting triangular structure makes it possible to solve for the unknown variables using back substitution.

## 1. Mathematical Foundation

> [!important] Equivalent Systems
> Gaussian elimination relies on elementary row operations, which preserve the solution set of a linear system.
>
> The three elementary row operations are:
>
> 1. **Row replacement:** Add a multiple of one row to another row.
> 2. **Row interchange:** Exchange two rows.
> 3. **Row scaling:** Multiply a row by a nonzero scalar.
>
> These operations produce an equivalent system with exactly the same solutions.

## 2. Row Echelon Form

> [!abstract] Definition
> A matrix is in **row echelon form (REF)** if:
>
> 1. All nonzero rows appear above any zero rows.
> 2. The leading entry of each nonzero row is strictly to the right of the leading entry in the row above it.
> 3. Every entry below a leading entry is zero.
>
> The leading nonzero entry of a row is called a pivot.

## 3. Gaussian Elimination Procedure

> [!example] General Algorithm
> Given a system $A\mathbf{x}=\mathbf{b}$:
>
> 1. Construct the augmented matrix $[A\mid\mathbf{b}]$.
> 2. Select a pivot in the leftmost available column.
> 3. If necessary, interchange rows to obtain a nonzero pivot.
> 4. Eliminate entries below the pivot using row replacement.
> 5. Move to the next pivot position.
> 6. Continue until the augmented matrix reaches REF.
> 7. Determine consistency and solve using back substitution.

## 4. Pivot and Free Variables

> [!important] Variable Classification
> - **Pivot variable:** A variable corresponding to a pivot column in the coefficient matrix.
> - **Free variable:** A variable corresponding to a non-pivot column in the coefficient matrix.
>
> Free variables are parameters that can take arbitrary values when the system is consistent.
>
> The number of free variables is:
>
> $$
> n-\operatorname{rank}(A)
> $$
>
> where $n$ is the number of unknowns.

## 5. Back Substitution

> [!abstract] Definition
> **Back substitution** solves a system in echelon form by determining variables from the last nonzero equation upward.
>
> The final equation is solved first. Its result is then substituted into the preceding equations until all pivot variables have been determined.

## 6. Important Properties

> [!important] Properties
> - Elementary row operations preserve the solution set of the system.
> - Gaussian elimination transforms a system into an equivalent system.
> - REF is not unique: different valid elimination sequences may produce different echelon forms.
> - The number of pivots equals the rank of the coefficient matrix.
> - An inconsistent system contains a row of the form:
>
> $$
> \begin{bmatrix}
> 0&\cdots&0&\mid&c
> \end{bmatrix},
> \qquad c\neq 0
> $$
>
> Such a row represents the contradiction $0=c$.

## 7. Computational Considerations

> [!warning] Numerical Considerations
> In exact arithmetic, Gaussian elimination determines the exact solution structure.
>
> In floating-point arithmetic, rounding errors can affect numerical accuracy. Pivoting strategies, especially partial pivoting, are commonly used to improve numerical stability.
>
> Numerical stability and error analysis are topics developed further in numerical linear algebra.

## 8. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Matrices:** Required to construct and manipulate augmented matrices.
> - **Elementary Row Operations:** The fundamental operations used by the algorithm.
> - **Row Echelon Form:** The target structure of Gaussian elimination.

> [!info] Relevant
> - **Matrix Rank:** Determines the number of pivots.
> - **Linear Systems:** Provides the equations being solved.

### Downstream Knowledge

> [!info] Relevant
> - **Gauss–Jordan Elimination:** Extends elimination until reduced row echelon form is obtained.
> - **Consistency and Solution Sets:** Uses the echelon form to classify solutions.
> - **Homogeneous Linear Systems:** Applies elimination to systems with zero right-hand sides.

> [!info] Advanced
> - **LU Decomposition:** Expresses a matrix as a product of triangular matrices, closely related to Gaussian elimination.
> - **Numerical Linear Algebra:** Studies efficient and stable implementations of elimination algorithms.

## 9. References

> [!bibliography]
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., 2016.
> - Golub, Gene H., and Charles F. Van Loan. *Matrix Computations*, 4th ed., 2013.