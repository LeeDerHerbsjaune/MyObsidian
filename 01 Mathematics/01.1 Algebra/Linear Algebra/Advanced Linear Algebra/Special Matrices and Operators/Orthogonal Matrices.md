---
type: technical-term
title: "Orthogonal Matrices"
aliases:
  - Orthogonal Matrix
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
  - "Golub, Gene H., and Charles F. Van Loan. Matrix Computations. 4th ed., 2013."
  - "Axler, Sheldon. Linear Algebra Done Right. 3rd ed., 2015."
related: []
projects: []
---

> [!abstract] Definition
> An **orthogonal matrix** is a real square matrix whose columns and rows form orthonormal sets.
>
> It represents a linear transformation that preserves Euclidean inner products, lengths, and angles.

## 1. Mathematical Definition

> [!definition] Orthogonal Matrix
> A matrix $Q\in\mathbb{R}^{n\times n}$ is orthogonal if:
>
> $$Q^TQ=QQ^T=I$$
>
> Equivalently:
>
> $$Q^{-1}=Q^T$$
>
> Its columns form an orthonormal basis of $\mathbb{R}^n$.

## 2. Geometric Interpretation

> [!important] Inner-Product Preservation
> For all $x,y\in\mathbb{R}^n$:
>
> $$\langle Qx,Qy\rangle=\langle x,y\rangle$$
>
> Therefore, orthogonal transformations preserve:
> - Vector lengths.
> - Angles between vectors.
> - Euclidean distances.
> - Orthogonality.
>
> They represent rigid rotations, reflections, or combinations of these transformations about the origin.

## 3. Important Properties

> [!important] Determinant
> Taking determinants of $Q^TQ=I$ gives:
>
> $$\det(Q)^2=1$$
>
> Therefore:
>
> $$\det(Q)\in\{-1,1\}$$
>
> - $\det(Q)=1$: orientation-preserving orthogonal transformation.
> - $\det(Q)=-1$: orientation-reversing orthogonal transformation.

> [!important] Eigenvalues
> Every complex eigenvalue $\lambda$ of a real orthogonal matrix satisfies:
>
> $$|\lambda|=1$$
>
> Real eigenvalues must therefore be $1$ or $-1$.

> [!note] Closure
> - The product of orthogonal matrices is orthogonal.
> - The inverse of an orthogonal matrix is orthogonal.
> - The transpose of an orthogonal matrix is orthogonal.

## 4. Knowledge Relationships

### Foundation Knowledge
- **Inner Products** — define the preservation condition.
- **Orthonormal Bases** — provide the column structure.
- **Matrix Transpose and Inverse** — establish the defining equation.

### Downstream Knowledge
- **QR Decomposition** — uses matrices with orthonormal columns.
- **Orthogonal Transformations** — generalize the geometric interpretation.
- **Spectral Theorem** — uses orthogonal matrices to diagonalize real symmetric matrices.
- **Numerical Linear Algebra** — exploits norm preservation in stable algorithms.

## 5. References
1. Golub, Gene H., and Charles F. Van Loan. *Matrix Computations*. 4th ed., Johns Hopkins University Press, 2013.
2. Axler, Sheldon. *Linear Algebra Done Right*. 3rd ed., Springer, 2015.