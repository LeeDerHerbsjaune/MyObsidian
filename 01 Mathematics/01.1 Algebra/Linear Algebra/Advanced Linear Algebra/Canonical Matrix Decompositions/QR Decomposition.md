---
type: technical-term
title: "QR Decomposition"
aliases:
  - QR Factorization
abbreviation: "QR"
field:
  - Mathematics
subfield:
  - Linear Algebra
  - Numerical Linear Algebra
status: learning
confidence: 1
created: 2026-11-04
updated: 2026-11-04
tags:
  - technical-term
  - linear-algebra
  - matrix-decompositions
sources:
  - "Golub, Gene H., and Charles F. Van Loan. Matrix Computations. 4th ed., 2013."
  - "Trefethen, Lloyd N., and David Bau III. Numerical Linear Algebra. 1997."
related: []
projects: []
---

> [!abstract] Definition
> **QR Decomposition** is a matrix factorization that expresses a matrix as the product of an orthogonal or unitary matrix and an upper triangular matrix.
>
> It is closely connected to orthonormal bases, Gram-Schmidt orthogonalization, and least-squares problems.

## 1. Mathematical Definition

> [!definition] QR Factorization
> For a real matrix $A\in\mathbb{R}^{m\times n}$, a QR factorization has the form:
>
> $$A=QR$$
>
> where:
> - $Q$ has orthonormal columns.
> - $R$ is upper triangular in the full-column-rank reduced formulation.
>
> The orthonormality condition is:
>
> $$Q^TQ=I$$

> [!note] Complex Matrices
> For complex matrices:
>
> $$A=QR,\qquad Q^*Q=I$$
>
> where $Q^*$ is the conjugate transpose.
>
> The matrix $Q$ is unitary in the square case and has orthonormal columns in the rectangular case.

## 2. Reduced and Full QR Factorizations

> [!important] Reduced QR
> For $A\in\mathbb{R}^{m\times n}$ with $m\geq n$ and full column rank:
>
> $$A=Q_1R$$
>
> where:
> - $Q_1\in\mathbb{R}^{m\times n}$ has orthonormal columns.
> - $R\in\mathbb{R}^{n\times n}$ is upper triangular and nonsingular.

> [!important] Full QR
> Extend the columns of $Q_1$ to an orthonormal basis of $\mathbb{R}^m$:
>
> $$Q=[Q_1\ Q_2]$$
>
> Then:
>
> $$A=Q
> \begin{bmatrix}
> R\\
> 0
> \end{bmatrix}$$
>
> Here $Q\in\mathbb{R}^{m\times m}$ is orthogonal.

## 3. Construction Methods

> [!note] Gram-Schmidt Process
> QR can be constructed by applying Gram-Schmidt orthogonalization to the columns of $A$.
>
> The orthonormalized columns form $Q$, while the projection coefficients form $R$.
>
> Classical Gram-Schmidt can suffer from loss of orthogonality in finite-precision arithmetic.

> [!note] Householder Transformations
> Householder reflections are orthogonal transformations that introduce zeros below selected diagonal entries.
>
> Repeated Householder transformations reduce $A$ to upper triangular form.
>
> This method is generally preferred for dense numerical QR factorization because of its numerical stability.

> [!note] Givens Rotations
> Givens rotations eliminate individual entries using rotations in coordinate planes.
>
> They are particularly useful for sparse matrices and incremental or structured computations.

## 4. QR and Least Squares

> [!important] Least-Squares Solution
> Consider an overdetermined system:
>
> $$Ax\approx b$$
>
> Suppose $A$ has full column rank and:
>
> $$A=QR$$
>
> with $Q^TQ=I$.
>
> The least-squares solution satisfies:
>
> $$R\hat{x}=Q^Tb$$
>
> Thus:
>
> $$\hat{x}=R^{-1}Q^Tb$$
>
> Computationally, solve the triangular system rather than explicitly computing the inverse.

## 5. Important Properties

> [!important] Orthogonal Norm Preservation
> For orthogonal $Q$:
>
> $$\|Qx\|_2=\|x\|_2$$
>
> Orthogonal transformations preserve Euclidean lengths and angles.

> [!important] Determinant
> For square orthogonal $Q$:
>
> $$\det(Q)\in\{-1,1\}$$
>
> Consequently, orthogonal transformations preserve volume magnitude.

> [!important] Uniqueness
> QR factorization is not unique without additional conventions.
>
> For a full-column-rank matrix, requiring the diagonal entries of $R$ to be positive gives a unique reduced QR factorization.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Inner Product Spaces** — provide the geometric foundation for orthogonality.
- **Orthonormal Bases** — provide the structure of $Q$.
- **Gram-Schmidt Process** — provides a direct construction of QR.
- **Matrix Multiplication** — defines the factorization.

### Downstream Knowledge
- **Least Squares** — QR gives an efficient solution method.
- **Numerical Linear Algebra** — studies stable QR algorithms.
- **QR Algorithm** — uses repeated QR factorizations to compute eigenvalues.
- **Singular Value Decomposition** — is related to orthogonal transformations and orthonormal bases.

## 7. References
1. Golub, Gene H., and Charles F. Van Loan. *Matrix Computations*. 4th ed., Johns Hopkins University Press, 2013.
2. Trefethen, Lloyd N., and David Bau III. *Numerical Linear Algebra*. SIAM, 1997.