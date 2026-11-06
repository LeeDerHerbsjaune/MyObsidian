---
type: technical-term
title: "Eigenvalues"
aliases: []
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
  - eigenvalues
sources:
  - "Lay, David C., Linear Algebra and Its Applications, 5th ed., 2016."
related: []
projects: []
---

> [!abstract] Definition
> An **eigenvalue** of a square matrix $A$ is a scalar $\lambda$ for which there exists a nonzero vector $\mathbf{v}$ satisfying:
>
> $$
> A\mathbf{v}=\lambda\mathbf{v}
> $$
>
> The eigenvalue describes the scaling factor applied to its associated eigenvectors by the linear transformation represented by $A$.

## 1. Characteristic Equation

> [!math] Eigenvalue Condition
> Rearranging the eigenvalue equation:
>
> $$
> (A-\lambda I)\mathbf{v}=\mathbf{0}
> $$
>
> Since $\mathbf{v}\neq\mathbf{0}$, the matrix $A-\lambda I$ must be singular.
>
> Therefore:
>
> $$
> \boxed{\det(A-\lambda I)=0}
> $$
>
> The solutions $\lambda$ are the eigenvalues of $A$.

## 2. Eigenvalues of a 2 × 2 Matrix

> [!example] Characteristic Equation
> Consider:
>
> $$
> A=
> \begin{bmatrix}
> a&b\\
> c&d
> \end{bmatrix}
> $$
>
> Its characteristic equation is:
>
> $$
> \det(A-\lambda I)=
> \begin{vmatrix}
> a-\lambda&b\\
> c&d-\lambda
> \end{vmatrix}=0
> $$
>
> Expanding:
>
> $$
> \lambda^2-(a+d)\lambda+(ad-bc)=0
> $$
>
> Thus, the eigenvalues are the roots of this quadratic equation.

## 3. Eigenvalue Properties

> [!important] Fundamental Properties
> For an $n\times n$ matrix over an algebraically closed field such as $\mathbb{C}$:
>
> - There are exactly $n$ eigenvalues when counted with algebraic multiplicity.
> - Eigenvalues may be repeated.
> - Eigenvalues may be complex, even when the matrix has only real entries.
> - The sum of eigenvalues, counted with algebraic multiplicity, equals the trace:
>
> $$
> \sum_{i=1}^{n}\lambda_i=\operatorname{tr}(A)
> $$
>
> - Their product, counted with algebraic multiplicity, equals the determinant:
>
> $$
> \prod_{i=1}^{n}\lambda_i=\det(A)
> $$

## 4. Special Eigenvalues

> [!note] Important Cases
> **Zero eigenvalue**
>
> $$
> 0\text{ is an eigenvalue}
> \iff
> \det(A)=0
> $$
>
> **Eigenvalue of the identity matrix**
>
> $$
> A=I\implies\lambda=1
> $$
>
> **Eigenvalues of a triangular matrix**
>
> The eigenvalues of an upper or lower triangular matrix are its diagonal entries, counted with algebraic multiplicity.

## 5. Eigenvalues Under Matrix Operations

> [!important] Useful Identities
> If $\lambda$ is an eigenvalue of $A$:
>
> - For $A+cI$, the corresponding eigenvalue is $\lambda+c$.
> - For $cA$, the corresponding eigenvalue is $c\lambda$.
> - For $A^k$, the corresponding eigenvalue is $\lambda^k$, for positive integers $k$.
> - For $A^{-1}$, the corresponding eigenvalue is $\lambda^{-1}$, provided $A$ is invertible.
>
> These identities apply to the corresponding eigenvectors.

## 6. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Determinants:** Used to derive the characteristic equation.
> - **Matrices:** Provides the square matrix being studied.
> - **Characteristic Polynomial:** Encodes eigenvalues as polynomial roots.

> [!info] Relevant
> - **Matrix Inverse:** Explains why zero eigenvalues correspond to singular matrices.

### Downstream Knowledge

> [!info] Relevant
> - **Eigenvectors:** Eigenvalues determine the scaling factors in the eigenvalue equation.
> - **Eigenspaces:** Groups all eigenvectors associated with a particular eigenvalue.
> - **Algebraic and Geometric Multiplicity:** Measures the occurrence and eigenspace dimension of eigenvalues.
> - **Diagonalization:** Uses a sufficient collection of linearly independent eigenvectors.

## 7. References

> [!bibliography]
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., 2016.
> - Axler, Sheldon. *Linear Algebra Done Right*, 3rd ed., 2015.