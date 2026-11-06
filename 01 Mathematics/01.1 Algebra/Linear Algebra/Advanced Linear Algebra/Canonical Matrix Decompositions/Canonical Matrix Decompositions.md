---
type: technical-term
title: Canonical Matrix Decompositions
aliases:
  - Matrix Decompositions
  - Matrix Factorizations and Canonical Forms
abbreviation: ""
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
  - Golub, Gene H., and Charles F. Van Loan. Matrix Computations. 4th ed., 2013.
  - Trefethen, Lloyd N., and David Bau III. Numerical Linear Algebra. 1997.
  - Axler, Sheldon. Linear Algebra Done Right. 3rd ed., 2015.
related:
  - "[[LU Decomposition]]"
  - "[[QR Decomposition]]"
  - "[[Jordan Canonical Form]]"
  - "[[Singular Value Decomposition (SVD)]]"
  - "[[Cholesky Decomposition]]"
projects: []
---
> [!abstract] Definition
> **Canonical Matrix Decompositions** is the study of representing matrices using structured factors or canonical forms that reveal their algebraic, geometric, and computational properties.
>
> A matrix decomposition expresses a matrix in terms of simpler matrices whose structures make particular operations or theoretical properties easier to analyze.

## 1. Scope and Mathematical Structure

> [!definition] Matrix Decomposition
> A matrix decomposition expresses a matrix $A$ as a product of two or more matrices:
>
> $$A=F_1F_2\cdots F_k$$
>
> The factors are selected to expose useful structure, such as:
> - Triangular structure.
> - Orthogonality.
> - Symmetry and positive definiteness.
> - Singular values and invariant subspaces.
> - Eigenvalue and generalized eigenvector structure.
>
> A canonical form, in contrast, represents a matrix in a standardized form under a specified equivalence relation.

> [!important] Two Different Ideas
> **Matrix factorization**
> - Expresses a matrix as a product of structured factors.
> - Often supports numerical computation.
> - Examples: LU, QR, Cholesky, and SVD.
>
> **Canonical matrix form**
> - Represents a matrix in a standardized form under an equivalence relation.
> - Reveals structural properties and classifies matrices.
> - Example: Jordan Canonical Form, obtained through similarity transformations.

## 2. Content of This Subject

> [!abstract] Main Topics
> 1. **LU Decomposition** — factors a matrix into lower and upper triangular matrices.
> 2. **QR Decomposition** — factors a matrix into an orthogonal or unitary matrix and an upper triangular matrix.
> 3. **Cholesky Decomposition** — factors a Hermitian positive-definite matrix into a triangular factor and its conjugate transpose.
> 4. **Singular Value Decomposition (SVD)** — represents any real or complex matrix using orthonormal singular vectors and nonnegative singular values.
> 5. **Jordan Canonical Form** — represents a square matrix in a canonical block-diagonal form under similarity.

## 3. Conceptual Classification

> [!note] Triangular Factorizations
> **LU Decomposition**
> - Separates a matrix into lower and upper triangular factors.
> - Primarily supports solving linear systems and repeated factorization-based computations.
>
> **Cholesky Decomposition**
> - Specializes triangular factorization to positive-definite Hermitian matrices.
> - Exploits symmetry and positive definiteness.

> [!note] Orthogonal Factorization
> **QR Decomposition**
> - Separates a matrix into an orthogonal or unitary factor and an upper triangular factor.
> - Preserves Euclidean norms and is central to least-squares computation.

> [!note] Singular-Value Representation
> **Singular Value Decomposition**
> - Uses orthonormal bases in both the domain and codomain.
> - Reveals rank, range, null space, and low-rank approximation structure.
> - Applies to rectangular as well as square matrices.

> [!note] Canonical Similarity Form
> **Jordan Canonical Form**
> - Describes the structure of a square matrix under similarity.
> - Extends diagonalization to matrices that may not have enough linearly independent eigenvectors.

## 4. Mathematical Significance

> [!important] Different Decompositions Reveal Different Properties
> No single decomposition is universally best.
>
> - LU exposes triangular structure and supports linear-system solving.
> - QR exposes orthogonal structure and supports least-squares computation.
> - Cholesky exploits positive definiteness for efficient factorization.
> - SVD reveals singular values, rank, and optimal low-rank approximations.
> - Jordan form reveals eigenvalue and generalized-eigenvector structure.

> [!warning] Existence and Uniqueness
> The conditions under which a decomposition exists and whether its factors are unique depend on the decomposition and the matrix.
>
> For example:
> - LU without pivoting is not guaranteed to exist for every matrix.
> - QR exists for every real or complex matrix, although rank deficiency affects uniqueness and some formulations.
> - Cholesky exists for Hermitian positive-definite matrices.
> - SVD exists for every real or complex matrix.
> - Jordan form exists over an algebraically closed field, such as $\mathbb{C}$, but is not generally available over $\mathbb{R}$ in the same complex-block form.

## 5. Knowledge Relationships

### Foundation Knowledge

> [!note] Essential
> - **Matrices** — provide the objects being factorized or represented.
> - **Matrix Multiplication** — is the operation underlying matrix factorizations.
> - **Matrix Inverse and Matrix Rank** — are important for understanding invertibility, rank conditions, and factorization properties.
> - **Linear Transformations** — provide the abstract interpretation of matrix representations.
> - **Eigenvalues and Eigenvectors** — are essential for understanding Jordan Canonical Form and relevant to several structural properties of SVD.

> [!note] Relevant
> - **Orthogonality and Orthonormal Bases** — provide the foundation for QR and SVD.
> - **Inner Product Spaces** — establish the geometric structure underlying orthogonality and singular vectors.
> - **Positive-Definite Matrices** — are essential for understanding Cholesky Decomposition.
> - **Systems of Linear Equations** — motivate LU and Cholesky factorization.
> - **Least Squares** — motivates QR-based solution methods.

### Downstream Knowledge

> [!note] Relevant
> - **Numerical Linear Algebra** — studies the stability, conditioning, and computational implementation of matrix factorizations.
> - **Iterative Methods for Linear Systems** — use factorization-based preconditioners and structured matrix representations.
> - **Low-Rank Approximation** — develops optimal approximation methods from SVD.
> - **Matrix Functions** — use eigenvalue-based representations and canonical forms to study functions of matrices.

> [!note] Advanced
> - **Spectral Theory** — studies eigenvalue structure and its relationship to matrix representations.
> - **Generalized Eigenvalue Problems** — extend eigenvalue analysis to matrix pairs.
> - **Schur Decomposition** — provides a numerically stable unitary similarity representation.
> - **Perron-Frobenius Theory** — studies eigenvalue properties of nonnegative matrices.

## 6. Scope Boundaries

> [!warning] Topics Kept Separate
> The following are related but deserve independent notes or subjects:
>
> - **Spectral Decomposition** — represents suitable normal or symmetric/Hermitian matrices through orthonormal eigenvectors.
> - **Schur Decomposition** — gives a unitary triangularization of square matrices.
> - **Polar Decomposition** — separates a matrix into unitary/orthogonal and positive-semidefinite factors.
> - **Matrix Functions** — studies functions defined on matrices.
> - **Numerical Linear Algebra** — studies numerical algorithms, error, stability, and conditioning in greater depth.
>
> These topics should be connected to this subject without being absorbed into its individual decomposition notes.

## 7. References

1. Golub, Gene H., and Charles F. Van Loan. *Matrix Computations*. 4th ed., Johns Hopkins University Press, 2013.
2. Trefethen, Lloyd N., and David Bau III. *Numerical Linear Algebra*. SIAM, 1997.
3. Axler, Sheldon. *Linear Algebra Done Right*. 3rd ed., Springer, 2015.
4. Meyer, Carl D. *Matrix Analysis and Applied Linear Algebra*. SIAM, 2000.