---
type: technical-term
title: "Determinants and Invertibility"
aliases:
  - Determinant Criterion for Invertibility
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
  - determinants
  - matrix-invertibility
sources:
  - "Lay, David C., Linear Algebra and Its Applications, 5th ed., 2016."
  - "Axler, Sheldon, Linear Algebra Done Right, 3rd ed., 2015."
related: []
projects: []
---

> [!abstract] Definition
> **Determinants and invertibility** describes the relationship between the determinant of a square matrix and the existence of its multiplicative inverse.
>
> A square matrix is invertible if and only if its determinant is nonzero.

## 1. Fundamental Criterion

> [!important] Invertibility Theorem
> Let $A\in\mathbb{F}^{n\times n}$ be a square matrix over a field $\mathbb{F}$.
>
> Then:
>
> $$
> \boxed{
> A\text{ is invertible}
> \iff
> \det(A)\neq0
> }
> $$
>
> Consequently:
>
> - If $\det(A)\neq0$, then $A$ is nonsingular and possesses a unique inverse.
> - If $\det(A)=0$, then $A$ is singular and has no inverse.

## 2. Algebraic Interpretation

> [!note] Multiplicative Identity
> If $A$ is invertible, there exists a matrix $A^{-1}$ satisfying:
>
> $$
> AA^{-1}=A^{-1}A=I
> $$
>
> Taking determinants:
>
> $$
> \det(A)\det(A^{-1})=\det(I)=1
> $$
>
> Therefore:
>
> $$
> \det(A)\neq0
> $$
>
> Conversely, if $\det(A)\neq0$, the adjugate identity gives:
>
> $$
> A^{-1}
> =
> \frac{1}{\det(A)}
> \operatorname{adj}(A)
> $$
>
> Thus, the inverse exists.

## 3. Relationship to Linear Independence

> [!important] Column Independence
> For a square matrix $A\in\mathbb{F}^{n\times n}$:
>
> $$
> \det(A)\neq0
> $$
>
> if and only if its columns are linearly independent.
>
> Since $A$ has exactly $n$ columns in $\mathbb{F}^n$, linear independence means that the columns form a basis of $\mathbb{F}^n$.
>
> Equivalently, the linear transformation represented by $A$ is bijective.

## 4. Relationship to Matrix Rank

> [!math] Rank Criterion
> A square matrix $A\in\mathbb{F}^{n\times n}$ is invertible if and only if:
>
> $$
> \boxed{
> \operatorname{rank}(A)=n
> }
> $$
>
> Therefore:
>
> $$
> \det(A)\neq0
> \iff
> \operatorname{rank}(A)=n
> $$
>
> If $\det(A)=0$, the matrix has rank strictly less than $n$.

## 5. Relationship to Linear Transformations

> [!abstract] Geometric Interpretation
> Consider the linear transformation:
>
> $$
> T:\mathbb{R}^n\rightarrow\mathbb{R}^n
> $$
>
> represented by:
>
> $$
> T(\mathbf{x})=A\mathbf{x}
> $$
>
> If $\det(A)\neq0$:
> - The transformation is injective.
> - The transformation is surjective.
> - The transformation is bijective.
> - The transformation preserves the dimension of the space.
> - An inverse transformation exists.
>
> If $\det(A)=0$, the transformation maps $\mathbb{R}^n$ into a lower-dimensional subspace and is not bijective.

## 6. Relationship to Linear Systems

> [!important] Unique Solution Criterion
> Consider a square linear system:
>
> $$
> A\mathbf{x}=\mathbf{b}
> $$
>
> where $A\in\mathbb{F}^{n\times n}$.
>
> The system has a unique solution for every right-hand-side vector $\mathbf{b}$ if and only if:
>
> $$
> \boxed{\det(A)\neq0}
> $$
>
> In this case:
>
> $$
> \mathbf{x}=A^{-1}\mathbf{b}
> $$
>
> If $\det(A)=0$, the system cannot have a unique solution:
> - It may have no solution.
> - It may have infinitely many solutions.
>
> The determinant alone does not distinguish these two cases.

## 7. Equivalent Conditions for Invertibility

> [!important] Invertible Matrix Theorem
> For a square matrix $A\in\mathbb{F}^{n\times n}$, the following conditions are equivalent:
>
> 1. $A$ is invertible.
> 2. $\det(A)\neq0$.
> 3. $\operatorname{rank}(A)=n$.
> 4. The columns of $A$ are linearly independent.
> 5. The columns of $A$ span $\mathbb{F}^n$.
> 6. The rows of $A$ are linearly independent.
> 7. The null space of $A$ contains only the zero vector.
> 8. The equation $A\mathbf{x}=\mathbf{b}$ has a unique solution for every $\mathbf{b}\in\mathbb{F}^n$.
> 9. The linear transformation represented by $A$ is bijective.
> 10. The reduced row echelon form of $A$ is $I_n$.
>
> These conditions express the same underlying property from different perspectives.

## 8. Important Limitations

> [!warning] Scope and Interpretation
> - The determinant is defined only for square matrices.
> - The determinant criterion for invertibility applies to square matrices over a field.
> - A nonzero determinant guarantees a unique solution for every right-hand-side vector in a square system.
> - A zero determinant does not automatically mean that a system has no solution.
> - Computing a determinant is not generally the preferred numerical method for deciding invertibility in large computational problems. Numerical methods typically use factorization and rank-revealing techniques.

## 9. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Determinants:** Provides the scalar criterion for invertibility.
> - **Matrix Inverse:** Defines the existence and properties of multiplicative inverses.
> - **Matrix Rank:** Provides an equivalent algebraic criterion for invertibility.

> [!info] Relevant
> - **Linear Independence:** Explains the relationship between nonzero determinants and independent columns.
> - **Kernel and Image:** Provides the injectivity and surjectivity interpretation.
> - **Linear Transformations:** Connects matrix invertibility to bijective transformations.

### Downstream Knowledge

> [!info] Relevant
> - **Systems of Linear Equations:** Determines when square systems have unique solutions.
> - **Change of Basis:** Requires invertible coordinate transformation matrices.
> - **Eigenvalues and Eigenvectors:** Uses determinant-based singularity conditions to find eigenvalues.

> [!info] Advanced
> - **Characteristic Polynomial:** Uses $\det(\lambda I-A)$ to characterize eigenvalues.
> - **Spectral Theory:** Develops the relationship between eigenvalues, matrix structure, and linear transformations.

## 10. References

> [!bibliography]
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., Pearson, 2016.
> - Axler, Sheldon. *Linear Algebra Done Right*, 3rd ed., Springer, 2015.
> - Strang, Gilbert. *Introduction to Linear Algebra*, 6th ed., Wellesley-Cambridge Press, 2023.