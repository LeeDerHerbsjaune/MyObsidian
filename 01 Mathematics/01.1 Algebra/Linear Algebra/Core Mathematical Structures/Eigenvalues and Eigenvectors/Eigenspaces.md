---
type: technical-term
title: "Eigenspaces"
aliases:
  - Eigenvector Spaces
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
  - eigenspaces
sources:
  - "Lay, David C., Linear Algebra and Its Applications, 5th ed., 2016."
  - "Axler, Sheldon, Linear Algebra Done Right, 3rd ed., 2015."
related: []
projects: []
---

> [!abstract] Definition
> An **eigenspace** associated with an eigenvalue $\lambda$ of a square matrix $A$ is the set of all vectors satisfying the eigenvalue equation, including the zero vector.
>
> It is defined as:
>
> $$
> \boxed{
> E_\lambda=\operatorname{Null}(A-\lambda I)
> }
> $$
>
> Equivalently:
>
> $$
> E_\lambda=
> \{\mathbf{v}\in\mathbb{F}^n:
> (A-\lambda I)\mathbf{v}=\mathbf{0}\}
> $$

## 1. Mathematical Structure

> [!important] Eigenspace as a Subspace
> An eigenspace is a subspace of the vector space on which the matrix acts.
>
> It contains:
> - The zero vector.
> - Every eigenvector associated with $\lambda$.
> - Every linear combination of its vectors.
>
> The zero vector belongs to the eigenspace but is not itself an eigenvector.

## 2. Finding an Eigenspace

> [!example] General Procedure
> Given a matrix $A$ and an eigenvalue $\lambda$:
>
> 1. Construct $A-\lambda I$.
> 2. Solve the homogeneous system:
>
> $$
> (A-\lambda I)\mathbf{v}=\mathbf{0}
> $$
>
> 3. Determine the null space of $A-\lambda I$.
> 4. Express the null space using a basis or parametric representation.
>
> The resulting subspace is the eigenspace associated with $\lambda$.

## 3. Dimension of an Eigenspace

> [!math] Geometric Multiplicity
> The dimension of the eigenspace associated with $\lambda$ is its geometric multiplicity:
>
> $$
> \boxed{
> \operatorname{GM}(\lambda)=\dim(E_\lambda)
> }
> $$
>
> By the rank-nullity theorem:
>
> $$
> \operatorname{GM}(\lambda)
> =
> n-\operatorname{rank}(A-\lambda I)
> $$

## 4. Eigenspaces for Distinct Eigenvalues

> [!important] Linear Independence
> Eigenvectors corresponding to distinct eigenvalues are linearly independent.
>
> Consequently, if $\lambda_1,\ldots,\lambda_k$ are distinct eigenvalues, then their corresponding eigenspaces form a direct sum:
>
> $$
> E_{\lambda_1}\oplus\cdots\oplus E_{\lambda_k}
> $$
>
> This means that a vector in their combined span has a unique decomposition into components from the respective eigenspaces.

## 5. Eigenspaces and Diagonalization

> [!note] Basis of Eigenvectors
> A matrix is diagonalizable if its eigenspaces collectively provide enough linearly independent eigenvectors to form a basis of the entire vector space.
>
> For an $n\times n$ matrix:
>
> $$
> \sum_{\lambda}
> \dim(E_\lambda)=n
> $$
>
> where the sum is over distinct eigenvalues.

## 6. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Eigenvalues:** Determines which scalar defines the eigenspace.
> - **Null Space and Column Space:** An eigenspace is the null space of $A-\lambda I$.
> - **Homogeneous Linear Systems:** Provides the method for computing eigenspaces.

> [!info] Relevant
> - **Linear Independence:** Determines the number of independent eigenvectors.

### Downstream Knowledge

> [!info] Relevant
> - **Algebraic and Geometric Multiplicity:** The dimension of an eigenspace is geometric multiplicity.
> - **Diagonalization:** Combines bases of eigenspaces to construct an eigenvector basis.

> [!info] Advanced
> - **Jordan Canonical Form:** Analyzes eigenspace dimensions when a matrix is not diagonalizable.

## 7. References

> [!bibliography]
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., 2016.
> - Axler, Sheldon. *Linear Algebra Done Right*, 3rd ed., 2015.