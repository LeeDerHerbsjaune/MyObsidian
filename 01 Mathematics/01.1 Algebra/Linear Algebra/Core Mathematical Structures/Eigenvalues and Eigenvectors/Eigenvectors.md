---
type: technical-term
title: "Eigenvectors"
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
  - eigenvectors
sources:
  - "Lay, David C., Linear Algebra and Its Applications, 5th ed., 2016."
  - "Strang, Gilbert, Introduction to Linear Algebra, 6th ed., 2023."
related: []
projects: []
---

> [!abstract] Definition
> An **eigenvector** of a square matrix $A$ is a nonzero vector $\mathbf{v}$ whose direction is preserved by the linear transformation represented by $A$.
>
> It satisfies:
>
> $$
> A\mathbf{v}=\lambda\mathbf{v}
> $$
>
> where $\lambda$ is the corresponding eigenvalue.

## 1. Mathematical Interpretation

> [!important] Invariant Direction
> Applying $A$ to an eigenvector changes its magnitude by a factor of $\lambda$ without changing its span.
>
> For real eigenvalues:
> - $\lambda>1$: magnitude increases.
> - $0<\lambda<1$: magnitude decreases.
> - $\lambda<0$: direction is reversed, with magnitude scaled by $|\lambda|$.
> - $\lambda=0$: the vector is mapped to the zero vector.
>
> An eigenvector is not necessarily a unit vector.

## 2. Finding Eigenvectors

> [!math] Eigenvector Equation
> Once an eigenvalue $\lambda$ is known, its eigenvectors are obtained by solving:
>
> $$
> (A-\lambda I)\mathbf{v}=\mathbf{0}
> $$
>
> This is a homogeneous linear system.
>
> Its nonzero solutions are the eigenvectors associated with $\lambda$.

## 3. Eigenvector Properties

> [!important] Fundamental Properties
> - An eigenvector must be nonzero.
> - Every nonzero scalar multiple of an eigenvector is also an eigenvector associated with the same eigenvalue.
> - The zero vector belongs to the eigenspace but is not an eigenvector.
> - Eigenvectors corresponding to distinct eigenvalues are linearly independent.
> - Eigenvectors associated with the same eigenvalue form a vector space together with the zero vector.

## 4. Geometric Interpretation

> [!note] Geometric Meaning
> In $\mathbb{R}^2$, an eigenvector determines a line through the origin that is mapped into itself by the linear transformation.
>
> In $\mathbb{R}^3$, an eigenvector similarly determines an invariant line.
>
> The vector may be stretched, compressed, reversed, or mapped to zero, depending on its eigenvalue.

## 5. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Eigenvalues:** Determines the scalar associated with an eigenvector.
> - **Null Space and Column Space:** Eigenvectors are nonzero vectors in the null space of $A-\lambda I$.
> - **Homogeneous Linear Systems:** Provides the method for finding eigenvectors.

> [!info] Relevant
> - **Linear Independence:** Determines whether eigenvectors can form a basis.

### Downstream Knowledge

> [!info] Relevant
> - **Eigenspaces:** Organizes all eigenvectors associated with each eigenvalue.
> - **Algebraic and Geometric Multiplicity:** Studies the dimension and multiplicity of eigenvector spaces.
> - **Diagonalization:** Uses linearly independent eigenvectors as a basis.

## 6. References

> [!bibliography]
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., 2016.
> - Strang, Gilbert. *Introduction to Linear Algebra*, 6th ed., 2023.