---
type: technical-term
title: "LU Decomposition"
aliases:
  - LU Factorization
abbreviation: "LU"
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
> **LU Decomposition** is a matrix factorization that expresses a square matrix as the product of a lower triangular matrix and an upper triangular matrix.
>
> It transforms a general linear-system problem into two triangular-system problems, which can be solved efficiently using forward and backward substitution.

## 1. Mathematical Definition

> [!definition] LU Factorization
> A square matrix $A\in\mathbb{F}^{n\times n}$ has an LU factorization if:
>
> $$A=LU$$
>
> where:
> - $L$ is a lower triangular matrix.
> - $U$ is an upper triangular matrix.
>
> A lower triangular matrix has zero entries above its main diagonal:
>
> $$L_{ij}=0\quad\text{if }i<j$$
>
> An upper triangular matrix has zero entries below its main diagonal:
>
> $$U_{ij}=0\quad\text{if }i>j$$

## 2. Factorization Conventions

> [!note] Doolittle and Crout Forms
> Two common conventions are:
>
> **Doolittle form**
> - $L$ has ones on its main diagonal.
> - $U$ contains the remaining scaling factors.
>
> **Crout form**
> - $U$ has ones on its main diagonal.
> - $L$ contains the remaining scaling factors.
>
> The choice is a convention; both represent the same general factorization idea.

> [!important] Pivoting
> An LU factorization without pivoting does not exist for every nonsingular matrix.
>
> To improve existence and numerical reliability, row permutations are introduced:
>
> $$PA=LU$$
>
> where $P$ is a permutation matrix.
>
> This is commonly called LU factorization with partial pivoting when the permutation is selected through row pivoting.

## 3. Solving Linear Systems

> [!important] LU-Based Solution
> Consider:
>
> $$Ax=b$$
>
> Given:
>
> $$PA=LU$$
>
> the system becomes:
>
> $$LUx=Pb$$
>
> Introduce an intermediate vector $y$:
>
> $$Ly=Pb$$
>
> Solve this lower triangular system using forward substitution, then solve:
>
> $$Ux=y$$
>
> using backward substitution.

> [!example] Repeated Right-Hand Sides
> If the same matrix $A$ is used with several right-hand sides:
>
> $$Ax_1=b_1,\quad Ax_2=b_2,\quad\ldots$$
>
> The LU factorization can be computed once and reused.
>
> This is more efficient than independently solving every system from the original matrix.

## 4. Important Properties

> [!important] Determinant
> If $A=LU$, then:
>
> $$\det(A)=\det(L)\det(U)$$
>
> If $L$ has a unit diagonal:
>
> $$\det(L)=1$$
>
> Therefore:
>
> $$\det(A)=\prod_{i=1}^{n}u_{ii}$$
>
> For a pivoted factorization $PA=LU$:
>
> $$\det(A)=\det(P)\det(L)\det(U)$$

> [!important] Computational Complexity
> For a dense $n\times n$ matrix, standard LU factorization requires approximately:
>
> $$\frac{2}{3}n^3$$
>
> floating-point operations, excluding lower-order terms.

> [!warning] Limitations
> - LU without pivoting may fail even for nonsingular matrices.
> - Pivoting improves numerical robustness but does not eliminate every conditioning problem.
> - The factorization is not generally orthogonal, so it does not preserve Euclidean norms.

## 5. Knowledge Relationships

### Foundation Knowledge
- **Matrices and Matrix Multiplication** — define the factorization operation.
- **Elementary Row Operations** — connect elimination procedures to triangular factors.
- **Systems of Linear Equations** — provide the main computational motivation.

### Downstream Knowledge
- **Gaussian Elimination** — produces the triangular structure underlying LU.
- **Numerical Linear Algebra** — studies pivoting, stability, and efficient implementation.
- **Iterative Methods and Preconditioning** — use incomplete LU factorizations in large sparse systems.

## 6. References
1. Golub, Gene H., and Charles F. Van Loan. *Matrix Computations*. 4th ed., Johns Hopkins University Press, 2013.
2. Trefethen, Lloyd N., and David Bau III. *Numerical Linear Algebra*. SIAM, 1997.