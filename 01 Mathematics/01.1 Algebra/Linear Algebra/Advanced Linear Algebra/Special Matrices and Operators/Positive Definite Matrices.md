---
type: technical-term
title: "Positive Definite Matrices"
aliases:
  - Positive Definite Matrix
abbreviation: "PD"
field:
  - Mathematics
subfield:
  - Linear Algebra
  - Matrix Analysis
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
  - "Meyer, Carl D. Matrix Analysis and Applied Linear Algebra. 2000."
related: []
projects: []
---

> [!abstract] Definition
> A **positive definite matrix** is a Hermitian matrix whose quadratic form is strictly positive for every nonzero vector.
>
> Positive definiteness connects matrix structure to positivity, invertibility, eigenvalues, optimization, and Cholesky factorization.

## 1. Mathematical Definition

> [!definition] Positive Definite Matrix
> A Hermitian matrix $A\in\mathbb{C}^{n\times n}$ is positive definite if:
>
> $$x^*Ax>0\quad\forall x\in\mathbb{C}^n,\ x\neq 0$$
>
> For real symmetric matrices:
>
> $$x^TAx>0\quad\forall x\in\mathbb{R}^n,\ x\neq 0$$
>
> We write:
>
> $$A\succ 0$$

## 2. Spectral Characterization

> [!important] Positive Eigenvalues
> A Hermitian matrix is positive definite if and only if all its eigenvalues are strictly positive:
>
> $$\lambda_i>0\quad\forall i$$
>
> By the spectral theorem:
>
> $$A=U\Lambda U^*$$
>
> where $\Lambda$ is diagonal and contains positive eigenvalues.

## 3. Equivalent Characterizations

> [!important] Sylvester's Criterion
> A real symmetric or complex Hermitian matrix is positive definite if and only if all its leading principal minors are positive:
>
> $$\det(A_k)>0,\quad k=1,\ldots,n$$
>
> where $A_k$ is the upper-left $k\times k$ principal submatrix.

> [!important] Cholesky Characterization
> A matrix is Hermitian positive definite if and only if it admits a Cholesky factorization:
>
> $$A=LL^*$$
>
> with $L$ nonsingular and lower triangular.
>
> The conventional Cholesky factor is uniquely determined by requiring its diagonal entries to be positive real numbers.

> [!important] Positive Square Root
> Every positive-definite matrix has a unique Hermitian positive-definite square root:
>
> $$A=A^{1/2}A^{1/2}$$
>
> It can be constructed through spectral decomposition.

## 4. Important Properties

> [!important] Invertibility
> Every positive-definite matrix is invertible:
>
> $$A\succ0\implies\det(A)>0$$

> [!important] Principal Submatrices
> Every principal submatrix of a positive-definite matrix is positive definite.

> [!important] Closure Under Addition
> If $A\succ0$ and $B\succ0$, then:
>
> $$A+B\succ0$$
>
> For every positive real scalar $c$:
>
> $$cA\succ0$$

> [!important] Quadratic Form Bounds
> For Hermitian positive-definite $A$:
>
> $$\lambda_{\min}\|x\|_2^2
> \leq x^*Ax
> \leq\lambda_{\max}\|x\|_2^2$$
>
> where $\lambda_{\min}$ and $\lambda_{\max}$ are the smallest and largest eigenvalues.

## 5. Related Matrix Classes

> [!note] Positive Semidefinite
> A Hermitian matrix is positive semidefinite if:
>
> $$x^*Ax\geq0\quad\forall x$$
>
> It may have zero eigenvalues and need not be invertible.
>
> Positive definiteness requires strict positivity for every nonzero vector.

> [!note] Indefinite Matrix
> A Hermitian matrix is indefinite if its quadratic form takes both positive and negative values.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Hermitian Matrices** — provide the required self-adjoint structure.
- **Quadratic Forms** — define the positivity condition.
- **Eigenvalues and Eigenvectors** — provide the spectral characterization.

### Downstream Knowledge
- **Cholesky Decomposition** — factors positive-definite matrices.
- **Matrix Inequalities** — develop positive-definite ordering.
- **Convex Optimization** — uses positive-definite Hessians in conditions for strict convexity.
- **Covariance Matrices** — are positive semidefinite and positive definite when nonsingular.

## 7. References
1. Horn, Roger A., and Charles R. Johnson. *Matrix Analysis*. 2nd ed., Cambridge University Press, 2012.
2. Meyer, Carl D. *Matrix Analysis and Applied Linear Algebra*. SIAM, 2000.