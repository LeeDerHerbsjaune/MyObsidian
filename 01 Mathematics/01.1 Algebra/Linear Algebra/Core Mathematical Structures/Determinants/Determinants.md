---
type: technical-term
title: Determinants
aliases: []
abbreviation: det
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
  - determinants
sources:
  - Lay, David C., Linear Algebra and Its Applications, 5th ed., 2016.
  - Strang, Gilbert, Introduction to Linear Algebra, 6th ed., 2023.
  - Axler, Sheldon, Linear Algebra Done Right, 3rd ed., 2015.
related:
  - "[[Determinants and Invertibility]]"
  - "[[Cofactor Expansion]]"
  - "[[Properties of Determinants]]"
projects: []
---

> [!abstract] Definition
> The **determinant** is a scalar-valued function defined on square matrices. It assigns a scalar to each square matrix and provides information about properties of the matrix, including invertibility, linear independence of its columns, and the volume-scaling behavior of the associated linear transformation.
>
> For a square matrix $A$, its determinant is denoted by:
>
> $$
> \det(A)
> $$
>
> or:
>
> $$
> |A|
> $$

## 1. Mathematical Definition

> [!math] Determinant of a Square Matrix
> For a matrix $A\in\mathbb{F}^{n\times n}$, the determinant is a scalar:
>
> $$
> \det:\mathbb{F}^{n\times n}\rightarrow\mathbb{F}
> $$
>
> The determinant is defined recursively or through equivalent algebraic formulations, such as the permutation formula.
>
> For $A=(a_{ij})$:
>
> $$
> \det(A)
> =
> \sum_{\sigma\in S_n}
> \operatorname{sgn}(\sigma)
> \prod_{i=1}^{n}a_{i,\sigma(i)}
> $$
>
> Where:
> - $S_n$ is the set of all permutations of $\{1,\ldots,n\}$.
> - $\operatorname{sgn}(\sigma)$ is the sign of the permutation.
> - Each permutation contributes a signed product of matrix entries.

## 2. Basic Determinants

> [!example] Determinant of a 1 × 1 Matrix
> For:
>
> $$
> A=[a]
> $$
>
> The determinant is:
>
> $$
> \det(A)=a
> $$

> [!example] Determinant of a 2 × 2 Matrix
> For:
>
> $$
> A=
> \begin{bmatrix}
> a&b\\
> c&d
> \end{bmatrix}
> $$
>
> The determinant is:
>
> $$
> \det(A)=ad-bc
> $$

> [!example] Determinant of a 3 × 3 Matrix
> For:
>
> $$
> A=
> \begin{bmatrix}
> a&b&c\\
> d&e&f\\
> g&h&i
> \end{bmatrix}
> $$
>
> Its determinant is:
>
> $$
> \det(A)
> =
> a(ei-fh)-b(di-fg)+c(dh-eg)
> $$

## 3. Geometric Interpretation

> [!important] Signed Volume Scaling
> A square matrix $A$ represents a linear transformation from $\mathbb{R}^n$ to $\mathbb{R}^n$.
>
> The absolute value of its determinant describes how the transformation scales $n$-dimensional volume:
>
> $$
> V_{\text{transformed}}
> =
> |\det(A)|V_{\text{original}}
> $$
>
> The sign describes orientation:
>
> - $\det(A)>0$: orientation is preserved.
> - $\det(A)<0$: orientation is reversed.
> - $\det(A)=0$: the transformation collapses the space into a lower-dimensional subspace, so $n$-dimensional volume becomes zero.

## 4. Fundamental Properties

> [!important] Core Properties
> For square matrices $A$ and $B$ of the same order:
>
> **Identity matrix**
>
> $$
> \det(I)=1
> $$
>
> **Product**
>
> $$
> \det(AB)=\det(A)\det(B)
> $$
>
> **Transpose**
>
> $$
> \det(A^T)=\det(A)
> $$
>
> **Scalar multiplication**
>
> $$
> \det(cA)=c^n\det(A)
> $$
>
> where $A$ is an $n\times n$ matrix.
>
> **Inverse**
>
> If $A$ is invertible:
>
> $$
> \det(A^{-1})=\frac{1}{\det(A)}
> $$

## 5. Relationship to Matrix Invertibility

> [!important] Fundamental Theorem
> A square matrix $A\in\mathbb{F}^{n\times n}$ is invertible if and only if:
>
> $$
> \boxed{\det(A)\neq0}
> $$
>
> If:
>
> $$
> \det(A)=0
> $$
>
> then $A$ is singular and has no inverse.

## 6. Relationship to Linear Independence

> [!note] Linear Independence Criterion
> The columns of a square matrix $A$ are linearly independent if and only if:
>
> $$
> \det(A)\neq0
> $$
>
> Equivalently:
> - Nonzero determinant: columns form a basis of $\mathbb{F}^n$.
> - Zero determinant: columns are linearly dependent.

## 7. Content of Subject

> [!abstract] Core Topics
> 1. Determinants — General definition and mathematical interpretation.
> 2. Properties of Determinants — Algebraic properties and computational consequences.
> 3. Cofactor Expansion — Recursive calculation using minors and cofactors.
> 4. Determinants and Invertibility — The relationship between nonzero determinants and matrix invertibility.

## 8. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Matrices:** Determinants are defined for square matrices.
> - **Matrix Operations:** Matrix multiplication and transpose are involved in determinant identities.
>
> [!info] Relevant
> - **Linear Independence:** Provides the algebraic meaning of a nonzero determinant.
> - **Linear Transformations:** Provides the geometric interpretation of determinants as signed volume-scaling factors.
> - **Elementary Row Operations:** Provides computational techniques for evaluating determinants.

### Downstream Knowledge

> [!info] Relevant
> - **Matrix Inverse:** A nonzero determinant characterizes invertibility for square matrices.
> - **Systems of Linear Equations:** Determinants provide criteria for unique solutions in square systems.
> - **Change of Basis:** Determinants describe how volume changes under changes of coordinates.
>
> [!info] Advanced
> - **Eigenvalues and Eigenvectors:** The characteristic polynomial is defined using a determinant.
> - **Spectral Theory:** Determinants connect to eigenvalue products and characteristic polynomials.
> - **Numerical Linear Algebra:** Develops computational methods for determinant-related problems and matrix factorization.

## 9. References

> [!bibliography]
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., Pearson, 2016.
> - Strang, Gilbert. *Introduction to Linear Algebra*, 6th ed., Wellesley-Cambridge Press, 2023.
> - Axler, Sheldon. *Linear Algebra Done Right*, 3rd ed., Springer, 2015.