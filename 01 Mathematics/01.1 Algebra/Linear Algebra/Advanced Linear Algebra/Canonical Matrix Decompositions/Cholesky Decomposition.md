---
type: technical-term
title: "Cholesky Decomposition"
aliases:
  - Cholesky Factorization
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
  - "Golub, Gene H., and Charles F. Van Loan. Matrix Computations. 4th ed., 2013."
  - "Trefethen, Lloyd N., and David Bau III. Numerical Linear Algebra. 1997."
related: []
projects: []
---

> [!abstract] Definition
> **Cholesky Decomposition** is a matrix factorization for Hermitian positive-definite matrices.
>
> It expresses such a matrix as the product of a triangular matrix and its conjugate transpose.
>
> It is computationally efficient because it exploits symmetry and positive definiteness.

## 1. Mathematical Definition

> [!definition] Cholesky Factorization
> Let $A\in\mathbb{C}^{n\times n}$ be Hermitian positive definite:
>
> $$A=A^*$$
>
> $$x^*Ax>0\quad\text{for all }x\neq 0$$
>
> Then there exists a unique lower triangular matrix $L$ with positive real diagonal entries such that:
>
> $$A=LL^*$$
>
> For real symmetric positive-definite matrices:
>
> $$A=LL^T$$

> [!note] Upper Triangular Convention
> An equivalent convention uses an upper triangular matrix $R$:
>
> $$A=R^*R$$
>
> In the real case:
>
> $$A=R^TR$$

## 2. Positive Definiteness

> [!important] Characterization
> A real symmetric matrix $A$ is positive definite if:
>
> $$x^TAx>0\quad\text{for all }x\neq 0$$
>
> Equivalent characterizations include:
> - All eigenvalues of $A$ are positive.
> - All leading principal minors are positive.
> - A Cholesky factorization with positive diagonal entries exists.
>
> For complex Hermitian matrices, use conjugate transposes and Hermitian positive definiteness.

## 3. Construction

> [!note] Cholesky Algorithm
> For a real symmetric positive-definite matrix, the entries of $L$ can be computed column by column:
>
> $$L_{jj}=
> \sqrt{a_{jj}-\sum_{k=1}^{j-1}L_{jk}^2}$$
>
> For $i>j$:
>
> $$L_{ij}=
> \frac{1}{L_{jj}}
> \left(a_{ij}-\sum_{k=1}^{j-1}L_{ik}L_{jk}\right)$$
>
> Positive definiteness guarantees that the diagonal square-root quantities are positive in exact arithmetic.

## 4. Solving Linear Systems

> [!important] Cholesky-Based Solution
> Consider:
>
> $$Ax=b$$
>
> With:
>
> $$A=LL^T$$
>
> solve the two triangular systems:
>
> $$Ly=b$$
>
> $$L^Tx=y$$
>
> This uses forward and backward substitution.

## 5. Important Properties

> [!important] Uniqueness
> The Cholesky factorization $A=LL^T$ is unique when $L$ is required to have a positive diagonal.

> [!important] Computational Complexity
> For a dense $n\times n$ matrix, Cholesky factorization requires approximately:
>
> $$\frac{1}{3}n^3$$
>
> floating-point operations, roughly half the leading-order cost of standard LU factorization.

> [!important] Determinant
> Since $A=LL^T$:
>
> $$\det(A)=\det(L)^2$$
>
> Therefore:
>
> $$\det(A)=\prod_{i=1}^{n}L_{ii}^2$$

> [!warning] Limitations
> - Standard Cholesky requires positive definiteness, not merely symmetry.
> - Positive-semidefinite matrices may require modified or pivoted variants.
> - Indefinite symmetric or Hermitian matrices require other factorizations, such as $LDL^*$ with suitable pivoting.
> - Floating-point implementations may need safeguards against loss of positive definiteness caused by numerical errors.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Matrices and Matrix Multiplication** — define the factorization.
- **Symmetric and Hermitian Matrices** — provide the required matrix structure.
- **Positive-Definite Matrices** — establish the existence condition.
- **Triangular Systems** — provide the solution procedure after factorization.

### Downstream Knowledge
- **Numerical Linear Algebra** — studies stable Cholesky algorithms.
- **Covariance Matrices** — are positive semidefinite and often admit Cholesky-based representations when positive definite.
- **Gaussian Processes and Numerical Optimization** — use positive-definite matrix systems computationally.

## 7. References
1. Golub, Gene H., and Charles F. Van Loan. *Matrix Computations*. 4th ed., Johns Hopkins University Press, 2013.
2. Trefethen, Lloyd N., and David Bau III. *Numerical Linear Algebra*. SIAM, 1997.