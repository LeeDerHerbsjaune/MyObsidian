---
type: technical-term
title: Systems of Linear Equations
aliases:
  - Linear Systems
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
  - systems-of-equations
sources:
  - Lay, David C., Linear Algebra and Its Applications, 5th ed., 2016.
  - Strang, Gilbert, Introduction to Linear Algebra, 6th ed., 2023.
related:
  - "[[Consistency and Solution Sets]]"
  - "[[Systems of Linear Equations|Linear Systems]]"
  - "[[Gaussian Elimination]]"
  - "[[Homogeneous Linear Systems]]"
  - "[[Gauss–Jordan Elimination|Gauss–Jordan Elimination]]"
projects: []
---

> [!abstract] Definition
> A **system of linear equations** is a collection of linear equations involving the same set of unknown variables. A solution is an assignment of values to the variables that satisfies every equation simultaneously.

> [!info] Scope
> This subject covers the mathematical structure of linear systems, their matrix representation, solution methods based on elementary row operations, the classification of solution sets, and the special properties of homogeneous systems.
>
> The focus is on finite systems over a field, typically the real numbers $\mathbb{R}$.

## 1. General Structure

> [!math] General Linear System
> A system of $m$ linear equations in $n$ unknowns has the form:
>
> $$
> \begin{aligned}
> a_{11}x_1+\cdots+a_{1n}x_n &= b_1\\
> a_{21}x_1+\cdots+a_{2n}x_n &= b_2\\
> &\vdots\\
> a_{m1}x_1+\cdots+a_{mn}x_n &= b_m
> \end{aligned}
> $$
>
> Where:
> - $x_1,\ldots,x_n$ are the unknown variables.
> - $a_{ij}$ are the coefficients.
> - $b_i$ are the constant terms.
> - $m$ is the number of equations.
> - $n$ is the number of unknowns.

## 2. Matrix Representation

> [!important] Matrix Form
> Every linear system can be represented as:
>
> $$
> A\mathbf{x}=\mathbf{b}
> $$
>
> Where:
> - $A\in\mathbb{F}^{m\times n}$ is the coefficient matrix.
> - $\mathbf{x}\in\mathbb{F}^{n}$ is the unknown vector.
> - $\mathbf{b}\in\mathbb{F}^{m}$ is the right-hand-side vector.
>
> The corresponding augmented matrix is:
>
> $$
> [A\mid\mathbf{b}]
> $$
>
> The augmented matrix provides a compact representation on which elimination methods operate.

## 3. Core Topics

> [!note] Content of Subject

- Linear Systems
- Gaussian Elimination
- Gauss–Jordan Elimination
- Consistency and Solution Sets
- Homogeneous Linear Systems

## 4. Conceptual Organization

> [!abstract] Mathematical Structure
> **Linear Systems**
> - Define equations, coefficients, unknowns, and matrix representations.
>
> **Elimination Methods**
> - Gaussian Elimination
> - Gauss–Jordan Elimination
>
> **Solution Classification**
> - Consistency and Solution Sets
>
> **Special Class of Systems**
> - Homogeneous Linear Systems

## 5. Fundamental Classification

> [!important] Three Possible Outcomes
> A linear system has exactly one of the following solution structures:
>
> 1. **Unique solution:** Exactly one vector satisfies all equations.
> 2. **Infinitely many solutions:** A family of vectors satisfies all equations.
> 3. **No solution:** No vector satisfies all equations.
>
> A system is **consistent** if it has at least one solution and **inconsistent** if it has no solution.

## 6. Fundamental Theoretical Connection

> [!important] Rank Criterion
> For a system $A\mathbf{x}=\mathbf{b}$, the system is consistent if and only if:
>
> $$
> \operatorname{rank}(A)
> =
> \operatorname{rank}([A\mid\mathbf{b}])
> $$
>
> If the system is consistent, the number of free variables is:
>
> $$
> n-\operatorname{rank}(A)
> $$
>
> Therefore:
> - A unique solution exists when $\operatorname{rank}(A)=n$.
> - Infinitely many solutions exist when $\operatorname{rank}(A)<n$.
>
> These conclusions assume a finite-dimensional system over a field.

## 7. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Matrices:** Required for coefficient matrices, augmented matrices, and matrix-based representations.
> - **Matrix Operations:** Provides the algebraic background for manipulating matrix representations.
> - **Elementary Row Operations:** Required to understand elimination methods.

> [!info] Relevant
> - **Linear Combinations:** Each equation represents a linear constraint on the unknown variables.
> - **Linear Independence:** Helps explain pivot variables, free variables, and uniqueness.
> - **Matrix Rank:** Determines consistency and the dimension of solution spaces.

### Downstream Knowledge

> [!info] Relevant
> - **Kernel and Image:** Homogeneous solutions are elements of the kernel of the coefficient matrix.
> - **Null Space and Column Space:** The solution structure is directly related to the null space, while consistency is determined by whether the right-hand side belongs to the column space.
> - **Rank-Nullity Theorem:** Establishes the relationship between the number of unknowns, rank, and nullity.

> [!info] Advanced
> - **Numerical Linear Algebra:** Develops stable and efficient computational methods for solving linear systems.
> - **Least Squares:** Extends the study to inconsistent systems by finding approximate solutions.
> - **LU Decomposition:** Develops matrix factorization methods closely connected to Gaussian elimination.

## 8. References

> [!bibliography] Recommended Sources
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., Pearson, 2016.
> - Strang, Gilbert. *Introduction to Linear Algebra*, 6th ed., Wellesley-Cambridge Press, 2023.
> - Axler, Sheldon. *Linear Algebra Done Right*, 3rd ed., Springer, 2015.