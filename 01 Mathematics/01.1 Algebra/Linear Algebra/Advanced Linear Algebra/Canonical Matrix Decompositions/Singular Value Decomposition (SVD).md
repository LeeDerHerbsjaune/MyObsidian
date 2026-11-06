---
type: technical-term
title: "Singular Value Decomposition"
aliases:
  - SVD
  - Singular Value Factorization
abbreviation: "SVD"
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
  - "Strang, Gilbert. Introduction to Linear Algebra. 5th ed., 2016."
related: []
projects: []
---

> [!abstract] Definition
> **Singular Value Decomposition (SVD)** is a factorization that expresses any real or complex matrix as a product of two orthogonal or unitary matrices and a diagonal matrix of nonnegative singular values.
>
> It reveals the geometric action of a linear transformation, including its rank, range, null space, and principal directions of stretching.

## 1. Mathematical Definition

> [!definition] Singular Value Decomposition
> For any matrix $A\in\mathbb{R}^{m\times n}$, there exist orthogonal matrices $U\in\mathbb{R}^{m\times m}$ and $V\in\mathbb{R}^{n\times n}$ such that:
>
> $$A=U\Sigma V^T$$
>
> where:
> - $U$ is an orthogonal matrix.
> - $V$ is an orthogonal matrix.
> - $\Sigma\in\mathbb{R}^{m\times n}$ is diagonal in the rectangular sense.
> - The diagonal entries of $\Sigma$ are nonnegative and ordered from largest to smallest.
>
> For complex matrices:
>
> $$A=U\Sigma V^*$$
>
> where $U$ and $V$ are unitary.

## 2. Singular Values

> [!definition] Singular Values
> The diagonal entries of $\Sigma$ are called the singular values:
>
> $$\sigma_1\geq\sigma_2\geq\cdots\geq\sigma_r>0$$
>
> The remaining diagonal entries, if any, are zero.
>
> Here:
>
> $$r=\operatorname{rank}(A)$$
>
> Singular values quantify the amount of stretching produced by the linear transformation along mutually orthogonal directions.

> [!important] Connection to Eigenvalues
> The right singular vectors are eigenvectors of $A^*A$, while the left singular vectors are eigenvectors of $AA^*$:
>
> $$A^*Av_i=\sigma_i^2v_i$$
>
> $$AA^*u_i=\sigma_i^2u_i$$
>
> Therefore, the singular values are the nonnegative square roots of the eigenvalues of $A^*A$ or $AA^*$.

## 3. Geometric Interpretation

> [!important] Transformation Structure
> The SVD separates a linear transformation into three stages:
>
> 1. $V^*$ transforms the input into an orthonormal coordinate system.
> 2. $\Sigma$ scales the coordinates along mutually orthogonal directions.
> 3. $U$ transforms the result into the output coordinate system.
>
> Thus, a general linear transformation can be understood as an orthogonal or unitary transformation, followed by directional scaling, followed by another orthogonal or unitary transformation.

## 4. Full and Reduced SVD

> [!note] Full SVD
> $$A=U\Sigma V^*$$
>
> with:
> - $U\in\mathbb{C}^{m\times m}$.
> - $\Sigma\in\mathbb{R}^{m\times n}$.
> - $V\in\mathbb{C}^{n\times n}$.

> [!note] Reduced SVD
> A reduced representation keeps only the singular directions associated with nonzero singular values:
>
> $$A=U_r\Sigma_rV_r^*$$
>
> where:
> - $U_r\in\mathbb{C}^{m\times r}$.
> - $\Sigma_r\in\mathbb{R}^{r\times r}$.
> - $V_r\in\mathbb{C}^{n\times r}$.
>
> Here $r=\operatorname{rank}(A)$.

## 5. Important Properties

> [!important] Rank
> The rank of a matrix equals the number of nonzero singular values:
>
> $$\operatorname{rank}(A)=\#\{i:\sigma_i>0\}$$

> [!important] Matrix Norms
> The spectral norm is the largest singular value:
>
> $$\|A\|_2=\sigma_1$$
>
> The Frobenius norm is:
>
> $$\|A\|_F=\sqrt{\sum_i\sigma_i^2}$$

> [!important] Condition Number
> For a full-rank square matrix:
>
> $$\kappa_2(A)=\frac{\sigma_{\max}}{\sigma_{\min}}$$
>
> A large condition number indicates that the matrix is sensitive to perturbations in its input or data.

> [!important] Best Low-Rank Approximation
> The truncated SVD:
>
> $$A_k=\sum_{i=1}^{k}\sigma_i u_i v_i^*$$
>
> is a best rank-$k$ approximation to $A$ in both the spectral norm and Frobenius norm.
>
> This is the Eckart-Young-Mirsky theorem.

> [!important] Pseudoinverse
> The Moore-Penrose pseudoinverse is obtained from the SVD by reciprocating nonzero singular values:
>
> $$A^+=V_r\Sigma_r^{-1}U_r^*$$

## 6. Computational Methods

> [!note] Numerical Computation
> Practical SVD algorithms commonly use:
> - Bidiagonal reduction.
> - Iterative diagonalization of the bidiagonal matrix.
> - Divide-and-conquer or related specialized algorithms.
>
> Directly forming $A^*A$ is generally avoided in numerical SVD algorithms because it can square the condition number and reduce numerical accuracy.

## 7. Knowledge Relationships

### Foundation Knowledge
- **Matrices and Linear Transformations** — define the linear map represented by $A$.
- **Inner Product Spaces** — establish orthogonality and orthonormal bases.
- **Eigenvalues and Eigenvectors** — explain the relationship between singular vectors and $A^*A$, $AA^*$.
- **Matrix Rank** — is revealed by the nonzero singular values.

### Downstream Knowledge
- **Low-Rank Approximation** — uses truncated SVD to construct optimal approximations.
- **Moore-Penrose Pseudoinverse** — is directly constructed from the SVD.
- **Numerical Linear Algebra** — studies SVD algorithms and their stability.
- **Principal Component Analysis** — uses SVD to analyze directions of variation in data.
- **Conditioning and Sensitivity Analysis** — use singular values to quantify numerical sensitivity.

## 8. References
1. Golub, Gene H., and Charles F. Van Loan. *Matrix Computations*. 4th ed., Johns Hopkins University Press, 2013.
2. Trefethen, Lloyd N., and David Bau III. *Numerical Linear Algebra*. SIAM, 1997.
3. Strang, Gilbert. *Introduction to Linear Algebra*. 5th ed., Wellesley-Cambridge Press, 2016.