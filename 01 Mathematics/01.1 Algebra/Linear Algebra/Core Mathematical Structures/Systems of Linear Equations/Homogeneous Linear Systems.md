---
type: technical-term
title: "Homogeneous Linear Systems"
aliases:
  - Homogeneous Systems
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
  - homogeneous-systems
sources:
  - "Lay, David C., Linear Algebra and Its Applications, 5th ed., 2016."
  - "Strang, Gilbert, Introduction to Linear Algebra, 6th ed., 2023."
related: []
projects: []
---

> [!abstract] Definition
> A **homogeneous linear system** is a linear system in which every equation has a zero constant term.
>
> Its matrix representation is:
>
> $$
> A\mathbf{x}=\mathbf{0}
> $$

## 1. Mathematical Representation

> [!math] General Form
> A homogeneous system with $m$ equations and $n$ unknowns is:
>
> $$
> \begin{aligned}
> a_{11}x_1+\cdots+a_{1n}x_n &= 0\\
> a_{21}x_1+\cdots+a_{2n}x_n &= 0\\
> &\vdots\\
> a_{m1}x_1+\cdots+a_{mn}x_n &= 0
> \end{aligned}
> $$
>
> In matrix form:
>
> $$
> A\mathbf{x}=\mathbf{0}
> $$

## 2. Trivial Solution

> [!important] Trivial Solution
> Every homogeneous linear system has at least one solution:
>
> $$
> \mathbf{x}=\mathbf{0}
> $$
>
> This is called the **trivial solution**.
>
> It follows directly because:
>
> $$
> A\mathbf{0}=\mathbf{0}
> $$

## 3. Nontrivial Solutions

> [!abstract] Definition
> A **nontrivial solution** is any solution other than the zero vector:
>
> $$
> \mathbf{x}\neq\mathbf{0}
> $$
>
> A homogeneous system may have only the trivial solution or infinitely many solutions.

## 4. Condition for Nontrivial Solutions

> [!important] Rank Criterion
> A homogeneous system with $n$ unknowns has a nontrivial solution if and only if:
>
> $$
> \operatorname{rank}(A)<n
> $$
>
> Equivalently, it must have at least one free variable.
>
> By the rank-nullity theorem:
>
> $$
> \operatorname{nullity}(A)
> =
> n-\operatorname{rank}(A)
> $$
>
> Therefore, nontrivial solutions exist precisely when the nullity is positive.

## 5. Square Systems and Determinants

> [!note] Special Case
> If $A$ is an $n\times n$ square matrix, then:
>
> - If $\det(A)\neq0$, the only solution is the trivial solution.
> - If $\det(A)=0$, nontrivial solutions exist.
>
> The determinant criterion applies specifically to square matrices.

## 6. Solution Space

> [!important] Null Space
> The set of all solutions to a homogeneous system is:
>
> $$
> \operatorname{Null}(A)
> =
> \{\mathbf{x}\in\mathbb{F}^n:
> A\mathbf{x}=\mathbf{0}\}
> $$
>
> This set is a subspace of $\mathbb{F}^n$.
>
> It is closed under vector addition and scalar multiplication.
>
> Its dimension is called the nullity of $A$.

## 7. Important Properties

> [!important] Fundamental Properties
> - Every homogeneous system is consistent.
> - Every homogeneous system has the trivial solution.
> - Nontrivial solutions exist if and only if there is at least one free variable.
> - The solution set is the null space of the coefficient matrix.
> - The solution set is a vector space, not merely an affine subspace.
> - Every linear combination of solutions is also a solution.

## 8. Relationship to Nonhomogeneous Systems

> [!math] Associated Homogeneous System
> Consider a nonhomogeneous system:
>
> $$
> A\mathbf{x}=\mathbf{b}
> $$
>
> Its associated homogeneous system is:
>
> $$
> A\mathbf{x}=\mathbf{0}
> $$
>
> If the nonhomogeneous system is consistent and $\mathbf{x}_p$ is a particular solution, then its complete solution set is:
>
> $$
> \mathbf{x}
> =
> \mathbf{x}_p+\operatorname{Null}(A)
> $$
>
> Thus, the homogeneous system describes the directions in which a particular solution can vary while continuing to satisfy the original system.

## 9. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Linear Systems:** Establishes the general structure of simultaneous linear equations.
> - **Matrices:** Provides the coefficient matrix representation.
> - **Null Space and Column Space:** The solution set of a homogeneous system is precisely the null space.

> [!info] Relevant
> - **Linear Independence:** Determines whether nonzero solutions can exist.
> - **Matrix Rank:** Determines the number of free variables.
> - **Rank-Nullity Theorem:** Relates the number of unknowns to the dimension of the solution space.

### Downstream Knowledge

> [!info] Relevant
> - **Consistency and Solution Sets:** Homogeneous systems are always consistent and have a vector-space solution set.
> - **Kernel and Image:** A homogeneous matrix equation describes the kernel of the associated linear transformation.

> [!info] Advanced
> - **Eigenvalues and Eigenvectors:** Eigenvectors can be characterized as nonzero solutions of $(A-\lambda I)\mathbf{x}=\mathbf{0}$.
> - **Differential Equations:** Homogeneous linear systems of differential equations use related linear-algebraic structures, although their solution theory is a separate subject.

## 10. References

> [!bibliography]
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., 2016.
> - Strang, Gilbert. *Introduction to Linear Algebra*, 6th ed., 2023.