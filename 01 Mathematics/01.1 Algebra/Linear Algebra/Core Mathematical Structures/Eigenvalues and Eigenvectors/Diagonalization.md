---
type: technical-term
title: "Diagonalization"
aliases:
  - Matrix Diagonalization
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
  - diagonalization
sources:
  - "Lay, David C., Linear Algebra and Its Applications, 5th ed., 2016."
  - "Strang, Gilbert, Introduction to Linear Algebra, 6th ed., 2023."
  - "Axler, Sheldon, Linear Algebra Done Right, 3rd ed., 2015."
related: []
projects: []
---

> [!abstract] Definition
> **Diagonalization** is the process of expressing a square matrix as a matrix similar to a diagonal matrix.
>
> A matrix $A\in\mathbb{F}^{n\times n}$ is diagonalizable if there exists an invertible matrix $P$ and a diagonal matrix $D$ such that:
>
> $$
> \boxed{A=PDP^{-1}}
> $$

## 1. Mathematical Structure

> [!important] Eigenvector Decomposition
> In the diagonalization:
>
> - $P$ contains linearly independent eigenvectors of $A$ as its columns.
> - $D$ contains the corresponding eigenvalues along its diagonal.
> - $P^{-1}$ converts vectors into the eigenvector coordinate system.
>
> Specifically:
>
> $$
> P=
> \begin{bmatrix}
> |&|&&|\\
> \mathbf{v}_1&\mathbf{v}_2&\cdots&\mathbf{v}_n\\
> |&|&&|
> \end{bmatrix}
> $$
>
> $$
> D=
> \begin{bmatrix}
> \lambda_1&0&\cdots&0\\
> 0&\lambda_2&\cdots&0\\
> \vdots&\vdots&\ddots&\vdots\\
> 0&0&\cdots&\lambda_n
> \end{bmatrix}
> $$

## 2. Why Diagonalization Works

> [!note] Derivation
> If the columns of $P$ are eigenvectors:
>
> $$
> A\mathbf{v}_i=\lambda_i\mathbf{v}_i
> $$
>
> Combining these equations:
>
> $$
> AP=PD
> $$
>
> Since $P$ is invertible:
>
> $$
> \boxed{A=PDP^{-1}}
> $$
>
> Thus, diagonalization expresses the transformation in a basis consisting entirely of eigenvectors.

## 3. Diagonalizability Criterion

> [!important] Fundamental Theorem
> An $n\times n$ matrix is diagonalizable over a field $\mathbb{F}$ if and only if it has $n$ linearly independent eigenvectors over $\mathbb{F}$.
>
> Equivalently, the sum of the dimensions of its distinct eigenspaces must equal $n$:
>
> $$
> \sum_{\lambda}\dim(E_\lambda)=n
> $$

## 4. Sufficient Conditions

> [!important] Useful Criteria
> A matrix is diagonalizable if:
>
> **1. It has $n$ distinct eigenvalues.**
>
> Distinct eigenvalues guarantee linearly independent corresponding eigenvectors.
>
> **2. It is real symmetric.**
>
> Every real symmetric matrix is orthogonally diagonalizable:
>
> $$
> A=QDQ^T
> $$
>
> where $Q$ is orthogonal:
>
> $$
> Q^{-1}=Q^T
> $$
>
> More generally, a complex Hermitian matrix is unitarily diagonalizable.

## 5. Computational Procedure

> [!example] Diagonalization Algorithm
> Given a square matrix $A$:
>
> 1. Compute the characteristic polynomial:
>
> $$
> p_A(\lambda)=\det(\lambda I-A)
> $$
>
> 2. Find its eigenvalues.
> 3. For each eigenvalue, solve:
>
> $$
> (A-\lambda I)\mathbf{v}=\mathbf{0}
> $$
>
> 4. Determine a basis for each eigenspace.
> 5. Collect $n$ linearly independent eigenvectors as the columns of $P$.
> 6. Construct $D$ using the corresponding eigenvalues in the same column order.
> 7. Verify:
>
> $$
> AP=PD
> $$
>
> If $P$ is invertible, then:
>
> $$
> A=PDP^{-1}
> $$

## 6. Applications of Diagonalization

> [!important] Matrix Powers
> If:
>
> $$
> A=PDP^{-1}
> $$
>
> then:
>
> $$
> \boxed{
> A^k=PD^kP^{-1}
> }
> $$
>
> Since $D$ is diagonal, its powers are easy to calculate:
>
> $$
> D^k=
> \begin{bmatrix}
> \lambda_1^k&0&\cdots&0\\
> 0&\lambda_2^k&\cdots&0\\
> \vdots&\vdots&\ddots&\vdots\\
> 0&0&\cdots&\lambda_n^k
> \end{bmatrix}
> $$
>
> This is particularly useful when calculating high powers of a matrix.

> [!note] Matrix Functions
> When a suitable matrix function is defined:
>
> $$
> f(A)=Pf(D)P^{-1}
> $$
>
> where:
>
> $$
> f(D)=
> \operatorname{diag}
> (f(\lambda_1),\ldots,f(\lambda_n))
> $$
>
> This provides a useful way to compute functions of diagonalizable matrices.

## 7. Limitations

> [!warning] Non-Diagonalizable Matrices
> Not every square matrix is diagonalizable.
>
> A matrix may have repeated eigenvalues but insufficient linearly independent eigenvectors.
>
> In that case, it cannot be expressed as $PDP^{-1}$ with diagonal $D$.
>
> Jordan canonical form provides a more general representation over an algebraically closed field.

## 8. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Eigenvalues:** Provides the diagonal entries of $D$.
> - **Eigenvectors:** Provides the columns of $P$.
> - **Eigenspaces:** Provides the candidate eigenvectors.
> - **Algebraic and Geometric Multiplicity:** Determines whether enough independent eigenvectors exist.

> [!info] Relevant
> - **Change of Basis:** Diagonalization is a change of basis to an eigenvector basis.
> - **Similarity Transformations:** Diagonalization is a special case of matrix similarity.

### Downstream Knowledge

> [!info] Relevant
> - **Matrix Powers:** Diagonalization simplifies repeated matrix multiplication.
> - **Spectral Decomposition:** Develops diagonal representations under additional structural conditions.

> [!info] Advanced
> - **Jordan Canonical Form:** Extends matrix simplification to non-diagonalizable matrices.
> - **Singular Value Decomposition:** Provides a general matrix decomposition without requiring diagonalizability.

## 9. References

> [!bibliography]
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., 2016.
> - Strang, Gilbert. *Introduction to Linear Algebra*, 6th ed., 2023.
> - Axler, Sheldon. *Linear Algebra Done Right*, 3rd ed., 2015.