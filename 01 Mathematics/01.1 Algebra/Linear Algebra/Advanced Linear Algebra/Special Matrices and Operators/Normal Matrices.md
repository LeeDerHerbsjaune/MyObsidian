---
type: technical-term
title: "Normal Matrices"
aliases:
  - Normal Matrix
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
> A **normal matrix** is a square matrix that commutes with its conjugate transpose.
>
> Normality is the exact condition characterizing unitary diagonalizability over the complex numbers.

## 1. Mathematical Definition

> [!definition] Normal Matrix
> A matrix $A\in\mathbb{C}^{n\times n}$ is normal if:
>
> $$A^*A=AA^*$$
>
> For real matrices:
>
> $$A^TA=AA^T$$

## 2. Spectral Theorem for Normal Matrices

> [!important] Unitary Diagonalization
> A complex square matrix is normal if and only if it is unitarily diagonalizable:
>
> $$A=U\Lambda U^*$$
>
> where:
> - $U$ is unitary.
> - $\Lambda$ is diagonal and may contain complex eigenvalues.
>
> Unlike Hermitian matrices, normal matrices do not necessarily have real eigenvalues.

## 3. Important Subclasses

> [!note] Hermitian Matrices
> If:
>
> $$A=A^*$$
>
> then:
>
> $$A^*A=AA^*=A^2$$
>
> Therefore, every Hermitian matrix is normal.

> [!note] Skew-Hermitian Matrices
> If:
>
> $$A^*=-A$$
>
> then $A$ is normal. Its eigenvalues are purely imaginary or zero.

> [!note] Unitary Matrices
> If:
>
> $$A^*A=AA^*=I$$
>
> then $A$ is normal. Its eigenvalues have absolute value one.

> [!important] General Relationship
> Hermitian, skew-Hermitian, and unitary matrices are all normal, but not every normal matrix belongs to one of these subclasses.

## 4. Important Properties

> [!important] Orthogonality of Eigenspaces
> Eigenvectors associated with distinct eigenvalues of a normal matrix are orthogonal.

> [!important] Normality and Diagonalizability
> Every normal matrix is diagonalizable over $\mathbb{C}$.
>
> The converse is not generally true: a diagonalizable matrix need not be normal.

> [!important] Spectral Norm
> For a normal matrix:
>
> $$\|A\|_2=\max_i|\lambda_i|$$
>
> Its spectral norm equals its spectral radius.

## 5. Knowledge Relationships

### Foundation Knowledge
- **Conjugate Transpose** — defines normality.
- **Eigenvalues and Eigenvectors** — provide the spectral interpretation.
- **Inner Product Spaces** — explain orthogonality of eigenvectors.

### Downstream Knowledge
- **Spectral Theorem** — characterizes unitary diagonalization.
- **Hermitian Matrices** — form an important subclass.
- **Unitary Matrices** — form another important subclass.
- **Matrix Functions** — exploit normal spectral representations.

## 6. References
1. Axler, Sheldon. *Linear Algebra Done Right*. 3rd ed., Springer, 2015.
2. Horn, Roger A., and Charles R. Johnson. *Matrix Analysis*. 2nd ed., Cambridge University Press, 2012.