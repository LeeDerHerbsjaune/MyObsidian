---
type: technical-term
title: "Unitary Matrices"
aliases:
  - Unitary Matrix
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
  - "Horn, Roger A., and Charles R. Johnson. Matrix Analysis. 2nd ed., 2012."
  - "Axler, Sheldon. Linear Algebra Done Right. 3rd ed., 2015."
related: []
projects: []
---

> [!abstract] Definition
> A **unitary matrix** is a complex square matrix whose conjugate transpose is its inverse.
>
> It generalizes orthogonal matrices to complex vector spaces and preserves complex inner products and norms.

## 1. Mathematical Definition

> [!definition] Unitary Matrix
> A matrix $U\in\mathbb{C}^{n\times n}$ is unitary if:
>
> $$U^*U=UU^*=I$$
>
> Equivalently:
>
> $$U^{-1}=U^*$$
>
> Its columns and rows form orthonormal bases of $\mathbb{C}^n$.

## 2. Geometric Interpretation

> [!important] Inner-Product Preservation
> For all $x,y\in\mathbb{C}^n$:
>
> $$\langle Ux,Uy\rangle=\langle x,y\rangle$$
>
> Therefore:
>
> $$\|Ux\|_2=\|x\|_2$$
>
> A unitary transformation preserves lengths, angles, distances, and orthogonality under the standard complex inner product.

## 3. Important Properties

> [!important] Determinant
> $$|\det(U)|=1$$
>
> The determinant lies on the unit circle in the complex plane.

> [!important] Eigenvalues
> Every eigenvalue $\lambda$ of a unitary matrix satisfies:
>
> $$|\lambda|=1$$

> [!note] Closure
> - The product of unitary matrices is unitary.
> - The inverse of a unitary matrix is unitary.
> - The conjugate transpose of a unitary matrix is unitary.

> [!important] Real Special Case
> A real unitary matrix is exactly an orthogonal matrix because conjugation has no effect on real entries.

## 4. Knowledge Relationships

### Foundation Knowledge
- **Complex Numbers** — define conjugation.
- **Conjugate Transpose** — defines unitarity.
- **Inner Product Spaces** — provide the complex geometric structure.
- **Orthonormal Bases** — provide the column and row structure.

### Downstream Knowledge
- **Hermitian Matrices** — are unitarily diagonalizable.
- **Normal Matrices** — include all unitary matrices.
- **Singular Value Decomposition** — uses unitary factors in complex spaces.
- **Quantum Information Theory** — uses unitary matrices to represent transformations of quantum states.

## 5. References
1. Horn, Roger A., and Charles R. Johnson. *Matrix Analysis*. 2nd ed., Cambridge University Press, 2012.
2. Axler, Sheldon. *Linear Algebra Done Right*. 3rd ed., Springer, 2015.