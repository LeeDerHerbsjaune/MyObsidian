---
type: technical-term
title: "Symmetric Matrices"
aliases:
  - Symmetric Matrix
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
  - special-matrices
sources:
  - "Axler, Sheldon. Linear Algebra Done Right. 3rd ed., 2015."
  - "Horn, Roger A., and Charles R. Johnson. Matrix Analysis. 2nd ed., 2012."
related: []
projects: []
---

> [!abstract] Definition
> A **symmetric matrix** is a real square matrix that is equal to its transpose.
>
> Symmetry imposes a strong structural constraint on a matrix and guarantees real eigenvalues and orthogonal diagonalizability.

## 1. Mathematical Definition

> [!definition] Symmetric Matrix
> A matrix $A\in\mathbb{R}^{n\times n}$ is symmetric if:
>
> $$A^T=A$$
>
> Equivalently, its entries satisfy:
>
> $$a_{ij}=a_{ji}$$
>
> for all $i,j$.

## 2. Properties

> [!important] Real Eigenvalues
> Every eigenvalue of a real symmetric matrix is real.

> [!important] Orthogonal Eigenvectors
> Eigenvectors corresponding to distinct eigenvalues are orthogonal.

> [!important] Spectral Theorem
> Every real symmetric matrix can be orthogonally diagonalized:
>
> $$A=Q\Lambda Q^T$$
>
> where:
> - $Q$ is orthogonal.
> - $\Lambda$ is a real diagonal matrix containing the eigenvalues.
>
> Consequently:
>
> $$Q^TQ=QQ^T=I$$

> [!important] Quadratic Forms
> A real symmetric matrix defines a quadratic form:
>
> $$q(x)=x^TAx$$
>
> Its eigenvalues determine whether the quadratic form is positive definite, negative definite, or indefinite.

## 3. Algebraic Properties

> [!note] Closure Properties
> If $A$ and $B$ are symmetric matrices of compatible square dimensions, then:
>
> - $A+B$ is symmetric.
> - $cA$ is symmetric for real scalar $c$.
> - $A^k$ is symmetric for nonnegative integer $k$.
>
> However, $AB$ is not necessarily symmetric.
>
> In fact:
>
> $$(AB)^T=B A$$
>
> Therefore, $AB$ is symmetric exactly when $AB=BA$.

## 4. Knowledge Relationships

### Foundation Knowledge
- **Matrices and Transpose** — define the symmetry condition.
- **Eigenvalues and Eigenvectors** — provide the spectral interpretation.
- **Inner Product Spaces** — explain orthogonality of eigenvectors.

### Downstream Knowledge
- **Spectral Theorem** — establishes orthogonal diagonalization.
- **Positive Definite Matrices** — form an important subclass of symmetric matrices.
- **Quadratic Forms** — use symmetric matrices to represent real quadratic expressions.
- **Cholesky Decomposition** — applies to symmetric positive-definite matrices.

## 5. References
1. Axler, Sheldon. *Linear Algebra Done Right*. 3rd ed., Springer, 2015.
2. Horn, Roger A., and Charles R. Johnson. *Matrix Analysis*. 2nd ed., Cambridge University Press, 2012.