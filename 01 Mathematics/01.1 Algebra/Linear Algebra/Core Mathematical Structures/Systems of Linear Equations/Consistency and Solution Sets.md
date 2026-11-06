---
type: technical-term
title: "Consistency and Solution Sets"
aliases:
  - Consistency of Linear Systems
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
  - solution-sets
sources:
  - "Lay, David C., Linear Algebra and Its Applications, 5th ed., 2016."
  - "Strang, Gilbert, Introduction to Linear Algebra, 6th ed., 2023."
related: []
projects: []
---
> [!abstract] Definition
> **Consistency** describes whether a linear system has at least one solution.
>
> The **solution set** is the set of all vectors that satisfy every equation in the system.

## 1. Consistency

> [!important] Classification
> A linear system is:
>
> - **Consistent** if at least one solution exists.
> - **Inconsistent** if no solution exists.
>
> Every consistent linear system has either exactly one solution or infinitely many solutions.

## 2. Rank Criterion for Consistency

> [!math] Rouché–Capelli Theorem
> For a linear system:
>
> $$
> A\mathbf{x}=\mathbf{b}
> $$
>
> the system is consistent if and only if:
>
> $$
> \operatorname{rank}(A)
> =
> \operatorname{rank}([A\mid\mathbf{b}])
> $$
>
> Here, $[A\mid\mathbf{b}]$ is the augmented matrix.

## 3. Number of Solutions

> [!important] Complete Classification
> Let $A$ have $n$ columns, corresponding to $n$ unknown variables.
>
> If:
>
> $$
> \operatorname{rank}(A)
> \neq
> \operatorname{rank}([A\mid\mathbf{b}])
> $$
>
> then the system has no solution.
>
> If the ranks are equal:
>
> - A unique solution exists when $\operatorname{rank}(A)=n$.
> - Infinitely many solutions exist when $\operatorname{rank}(A)<n$.
>
> For a consistent system, the number of free variables is:
>
> $$
> n-\operatorname{rank}(A)
> $$

## 4. Geometric Interpretation

> [!note] Geometric Meaning
> The solution set is the intersection of the geometric sets represented by the equations.
>
> - No intersection means an inconsistent system.
> - A single intersection point means a unique solution.
> - An intersection containing infinitely many points means infinitely many solutions.
>
> The geometric interpretation depends on the dimension of the ambient real vector space.

## 5. Solution Sets and Parametric Form

> [!abstract] Parametric Representation
> When a consistent system has free variables, its solutions can be expressed using parameters.
>
> For example, if a solution depends on two free parameters $s$ and $t$, the solution vector may be written as:
>
> $$
> \mathbf{x}
> =
> \mathbf{p}
> +s\mathbf{v}_1
> +t\mathbf{v}_2
> $$
>
> Here:
> - $\mathbf{p}$ is a particular solution.
> - $\mathbf{v}_1$ and $\mathbf{v}_2$ describe independent directions of variation.
> - $s,t\in\mathbb{R}$ are arbitrary parameters.
>
> More generally, every consistent system has a solution set that is an affine subspace.

## 6. Connection to the Null Space

> [!important] General Solution Structure
> If $A\mathbf{x}=\mathbf{b}$ is consistent and $\mathbf{x}_p$ is one particular solution, then every solution has the form:
>
> $$
> \mathbf{x}
> =
> \mathbf{x}_p+\mathbf{z}
> $$
>
> where:
>
> $$
> \mathbf{z}\in\operatorname{Null}(A)
> $$
>
> Equivalently:
>
> $$
> \boxed{
> \mathbf{x}
> =
> \mathbf{x}_p+\operatorname{Null}(A)
> }
> $$
>
> This means the solution set is a translation of the null space.

## 7. Important Consequences

> [!important] Key Results
> - A system with more equations than unknowns may still be consistent.
> - A system with fewer equations than unknowns may still have no solution.
> - The number of equations alone does not determine the number of solutions.
> - The rank of the coefficient and augmented matrices determines consistency.
> - A consistent system has a unique solution precisely when there are no free variables.

## 8. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Linear Systems:** Defines the mathematical objects being classified.
> - **Gaussian Elimination:** Provides a method for exposing inconsistency and free variables.
> - **Matrix Rank:** Determines consistency and the number of free variables.

> [!info] Relevant
> - **Linear Independence:** Helps explain the relationship between pivots and independent constraints.
> - **Null Space and Column Space:** Provides the subspaces used to characterize solution sets.

### Downstream Knowledge

> [!info] Relevant
> - **Homogeneous Linear Systems:** A special case whose solution set is the null space.
> - **Rank-Nullity Theorem:** Determines the dimension of the null space.
> - **Least Squares:** Addresses systems that are inconsistent by finding approximate solutions.

## 9. References

> [!bibliography]
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., 2016.
> - Strang, Gilbert. *Introduction to Linear Algebra*, 6th ed., 2023.