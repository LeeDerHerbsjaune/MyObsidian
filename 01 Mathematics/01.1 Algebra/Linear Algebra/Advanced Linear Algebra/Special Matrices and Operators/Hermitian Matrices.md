---
type: technical-term
title: "Hermitian Matrices"
aliases:
  - Hermitian Matrix
  - Self-Adjoint Matrix
abbreviation: ""
field:
  - Mathematics
subfield:
  - Linear Algebra
  - Complex Linear Algebra
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
> A **Hermitian matrix** is a complex square matrix equal to its conjugate transpose.
>
> It generalizes real symmetric matrices to complex vector spaces and has real eigenvalues and a unitary eigenvector basis.

## 1. Mathematical Definition

> [!definition] Hermitian Matrix
> A matrix $A\in\mathbb{C}^{n\times n}$ is Hermitian if:
>
> $$A^*=A$$
>
> where $A^*=\overline{A}^{\,T}$ is the conjugate transpose.
>
> Entrywise:
>
> $$a_{ij}=\overline{a_{ji}}$$

> [!note] Real Special Case
> If $A$ has only real entries, then conjugation has no effect:
>
> $$A^*=A^T$$
>
> Therefore, a real Hermitian matrix is exactly a real symmetric matrix.

## 2. Properties

> [!important] Real Eigenvalues
> Every eigenvalue of a Hermitian matrix is real.

> [!important] Orthogonality of Eigenvectors
> Eigenvectors associated with distinct eigenvalues are orthogonal under the standard complex inner product.

> [!important] Spectral Theorem
> Every Hermitian matrix is unitarily diagonalizable:
>
> $$A=U\Lambda U^*$$
>
> where:
> - $U$ is unitary.
> - $\Lambda$ is a real diagonal matrix.
>
> The unitary matrix satisfies:
>
> $$U^*U=UU^*=I$$

> [!important] Real Quadratic Form
> For every $x\in\mathbb{C}^n$:
>
> $$x^*Ax\in\mathbb{R}$$
>
> This property makes Hermitian matrices fundamental in complex quadratic-form theory.

## 3. Algebraic Properties

> [!note] Closure Properties
> - $A+B$ is Hermitian if $A$ and $B$ are Hermitian.
> - $cA$ is Hermitian if $A$ is Hermitian and $c\in\mathbb{R}$.
> - $A^k$ is Hermitian for nonnegative integer $k$.
> - $AB$ is Hermitian if $A$ and $B$ are Hermitian and commute.
>
> In general:
>
> $$(AB)^*=B^*A^*=BA$$
>
> Thus, the product of two Hermitian matrices is not necessarily Hermitian.

## 4. Knowledge Relationships

### Foundation Knowledge
- **Complex Numbers** — provide complex conjugation.
- **Conjugate Transpose** — defines the Hermitian condition.
- **Inner Product Spaces** — establish the complex inner-product structure.
- **Eigenvalues and Eigenvectors** — explain spectral properties.

### Downstream Knowledge
- **Normal Matrices** — every Hermitian matrix is normal.
- **Positive Definite Matrices** — are defined through Hermitian or symmetric structure and positivity.
- **Spectral Theorem** — establishes unitary diagonalization.
- **Quantum Mechanics** — uses Hermitian operators to represent observables; this is an application rather than part of the matrix definition.

## 5. References
1. Axler, Sheldon. *Linear Algebra Done Right*. 3rd ed., Springer, 2015.
2. Horn, Roger A., and Charles R. Johnson. *Matrix Analysis*. 2nd ed., Cambridge University Press, 2012.