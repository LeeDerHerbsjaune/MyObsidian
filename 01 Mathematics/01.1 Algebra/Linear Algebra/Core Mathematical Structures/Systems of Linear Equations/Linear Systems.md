---
type: technical-term
title: "Linear Systems"
aliases:
  - Systems of Linear Equations
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
  - linear-systems
sources:
  - "Lay, David C., Linear Algebra and Its Applications, 5th ed., 2016."
related: []
projects: []
---

> [!abstract] Definition
> A **linear system** is a finite collection of linear equations involving a common set of unknown variables. Its solution is a vector that simultaneously satisfies every equation in the system.

## 1. Mathematical Representation

> [!math] General Form
> A linear system with $m$ equations and $n$ unknowns can be written as:
>
> $$
> A\mathbf{x}=\mathbf{b}
> $$
>
> Where:
>
> $$
> A=
> \begin{bmatrix}
> a_{11}&\cdots&a_{1n}\\
> \vdots&\ddots&\vdots\\
> a_{m1}&\cdots&a_{mn}
> \end{bmatrix}
> $$
>
> $$
> \mathbf{x}=
> \begin{bmatrix}
> x_1\\\vdots\\x_n
> \end{bmatrix},
> \qquad
> \mathbf{b}=
> \begin{bmatrix}
> b_1\\\vdots\\b_m
> \end{bmatrix}
> $$

## 2. Definition of a Linear Equation

> [!important] Linearity
> A linear equation in $n$ variables has the form:
>
> $$
> a_1x_1+a_2x_2+\cdots+a_nx_n=b
> $$
>
> The variables appear only to the first power and are not multiplied by one another.
>
> Expressions such as $x_1x_2$, $x_1^2$, or $\sin(x_1)$ do not define linear equations in the unknown variables.

## 3. Geometric Interpretation

> [!note] Geometric Meaning
> Over $\mathbb{R}$:
> - One linear equation in two variables generally represents a line in $\mathbb{R}^2$.
> - One linear equation in three variables generally represents a plane in $\mathbb{R}^3$.
> - More generally, a nontrivial linear equation in $\mathbb{R}^n$ defines a hyperplane.
>
> A system's solution set is the intersection of the sets defined by its individual equations.

## 4. Column Interpretation

> [!math] Linear Combination Form
> The matrix equation can also be interpreted as:
>
> $$
> x_1\mathbf{a}_1+
> x_2\mathbf{a}_2+\cdots+
> x_n\mathbf{a}_n=\mathbf{b}
> $$
>
> Where $\mathbf{a}_j$ is the $j$-th column of $A$.
>
> Therefore, the system is consistent if and only if $\mathbf{b}$ belongs to the column space of $A$.

## 5. Solution Classification

> [!important] Fundamental Possibilities
> A linear system can have:
>
> - No solution.
> - Exactly one solution.
> - Infinitely many solutions.
>
> It cannot have exactly two, three, or any other finite number greater than one of distinct solutions over a field.

## 6. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Matrices:** Provides the coefficient matrix and augmented matrix representations.
> - **Linear Combinations:** Explains the relationship between the coefficient columns and the right-hand-side vector.

> [!info] Relevant
> - **Vector Spaces:** Provides the setting for interpreting solution sets as subsets of vector spaces.
> - **Matrix Rank:** Helps classify the number and structure of solutions.

### Downstream Knowledge

> [!info] Relevant
> - **Gaussian Elimination:** A systematic method for solving linear systems.
> - **Gauss–Jordan Elimination:** Reduces an augmented matrix to reduced row echelon form.
> - **Consistency and Solution Sets:** Classifies the possible solution structures.
> - **Homogeneous Linear Systems:** Studies systems whose right-hand-side vector is zero.

## 7. References

> [!bibliography]
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., 2016.
> - Strang, Gilbert. *Introduction to Linear Algebra*, 6th ed., 2023.