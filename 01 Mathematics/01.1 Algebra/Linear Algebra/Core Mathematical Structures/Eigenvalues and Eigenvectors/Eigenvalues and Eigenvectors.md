---
type: technical-term
title: Eigenvalues and Eigenvectors
aliases:
  - Spectral Theory of Matrices
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
  - eigenvectors
sources:
  - Lay, David C., Linear Algebra and Its Applications, 5th ed., 2016.
  - Strang, Gilbert, Introduction to Linear Algebra, 6th ed., 2023.
  - Axler, Sheldon, Linear Algebra Done Right, 3rd ed., 2015.
related:
  - "[[Cayley–Hamilton Theorem|Cayley–Hamilton Theorem]]"
  - "[[Diagonalization]]"
  - "[[Eigenspaces]]"
  - "[[Eigenvalues]]"
  - "[[Eigenvectors]]"
  - "[[Characteristic Polynomial]]"
  - "[[Algebraic and Geometric Multiplicity]]"
projects: []
---

> [!abstract] Definition
> **Eigenvalues and eigenvectors** describe special directions of a linear transformation that remain unchanged in direction under the transformation, although their magnitude may change.
>
> For a linear transformation $T:V\rightarrow V$, a nonzero vector $\mathbf{v}\in V$ is an eigenvector if there exists a scalar $\lambda$ such that:
>
> $$
> T(\mathbf{v})=\lambda\mathbf{v}
> $$
>
> The scalar $\lambda$ is called the corresponding eigenvalue.

## 1. Mathematical Foundation

> [!important] Matrix Representation
> For a square matrix $A\in\mathbb{F}^{n\times n}$, an eigenvalue-eigenvector pair satisfies:
>
> $$
> A\mathbf{v}=\lambda\mathbf{v}
> $$
>
> Rearranging:
>
> $$
> (A-\lambda I)\mathbf{v}=\mathbf{0}
> $$
>
> Since an eigenvector must be nonzero, this equation has a nontrivial solution only when:
>
> $$
> \det(A-\lambda I)=0
> $$
>
> This equation is called the characteristic equation.

## 2. Characteristic Polynomial

> [!abstract] Definition
> The **characteristic polynomial** of a square matrix $A$ is:
>
> $$
> p_A(\lambda)=\det(\lambda I-A)
> $$
>
> Its roots are the eigenvalues of $A$, counted with algebraic multiplicity.
>
> The characteristic polynomial is a monic polynomial of degree $n$ for an $n\times n$ matrix.

## 3. Eigenspaces

> [!abstract] Definition
> The **eigenspace** associated with an eigenvalue $\lambda$ is the null space:
>
> $$
> E_\lambda=\operatorname{Null}(A-\lambda I)
> $$
>
> Equivalently:
>
> $$
> E_\lambda=
> \{\mathbf{v}\in\mathbb{F}^n:
> A\mathbf{v}=\lambda\mathbf{v}\}
> $$
>
> It contains the zero vector and all eigenvectors associated with $\lambda$.

## 4. Multiplicity

> [!important] Two Types of Multiplicity
> **Algebraic multiplicity** is the multiplicity of an eigenvalue as a root of the characteristic polynomial.
>
> **Geometric multiplicity** is the dimension of its eigenspace:
>
> $$
> \operatorname{GM}(\lambda)
> =
> \dim\operatorname{Null}(A-\lambda I)
> $$
>
> For every eigenvalue:
>
> $$
> 1\leq
> \operatorname{GM}(\lambda)
> \leq
> \operatorname{AM}(\lambda)
> $$

## 5. Diagonalization

> [!abstract] Definition
> A square matrix $A$ is **diagonalizable** if it is similar to a diagonal matrix.
>
> That is, there exist an invertible matrix $P$ and a diagonal matrix $D$ such that:
>
> $$
> A=PDP^{-1}
> $$
>
> The columns of $P$ are linearly independent eigenvectors of $A$, while the corresponding eigenvalues appear on the diagonal of $D$.

## 6. Cayley–Hamilton Theorem

> [!abstract] Definition
> The **Cayley–Hamilton theorem** states that every square matrix satisfies its own characteristic polynomial.
>
> If:
>
> $$
> p_A(\lambda)
> =
> \lambda^n+c_{n-1}\lambda^{n-1}
> +\cdots+c_1\lambda+c_0
> $$
>
> then:
>
> $$
> \boxed{
> p_A(A)=
> A^n+c_{n-1}A^{n-1}
> +\cdots+c_1A+c_0I=0
> }
> $$

## 7. Content of Subject

> [!abstract] Core Topics
> 1. Eigenvalues
> 2. Eigenvectors
> 3. Characteristic Polynomial
> 4. Eigenspaces
> 5. Algebraic and Geometric Multiplicity
> 6. Diagonalization
> 7. Cayley–Hamilton Theorem

## 8. Conceptual Organization

> [!note] Mathematical Structure
> **Eigenvalue-Eigenvector Fundamentals**
> - Eigenvalues
> - Eigenvectors
>
> **Algebraic Characterization**
> - Characteristic Polynomial
> - Eigenspaces
>
> **Eigenvalue Structure**
> - Algebraic and Geometric Multiplicity
>
> **Matrix Simplification**
> - Diagonalization
>
> **Polynomial Properties of Matrices**
> - Cayley–Hamilton Theorem

## 9. Fundamental Theoretical Connections

> [!important] Determinants and Invertibility
> Eigenvalues are roots of the characteristic polynomial:
>
> $$
> \det(\lambda I-A)=0
> $$
>
> In particular, zero is an eigenvalue if and only if $A$ is singular.
>
> Therefore:
>
> $$
> 0\text{ is an eigenvalue of }A
> \iff
> \det(A)=0
> $$

> [!important] Trace and Determinant
> Over the complex numbers, the characteristic polynomial encodes the eigenvalues, including their algebraic multiplicities.
>
> For an $n\times n$ matrix:
>
> $$
> \operatorname{tr}(A)=\sum_{i=1}^{n}\lambda_i
> $$
>
> $$
> \det(A)=\prod_{i=1}^{n}\lambda_i
> $$
>
> These identities count eigenvalues with algebraic multiplicity.

## 10. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Matrices:** Provides the square matrices whose eigenvalues and eigenvectors are studied.
> - **Determinants:** Required to construct and solve the characteristic equation.
> - **Linear Transformations:** Provides the abstract interpretation of eigenvectors as invariant directions.
> - **Null Space and Column Space:** Eigenspaces are null spaces of shifted matrices $A-\lambda I$.

> [!info] Relevant
> - **Linear Independence:** Determines whether a collection of eigenvectors forms a basis.
> - **Matrix Inverse:** Connects zero eigenvalues to singularity and invertibility.
> - **Polynomial Algebra:** Provides the background for characteristic polynomials and matrix polynomial identities.

### Downstream Knowledge

> [!info] Relevant
> - **Spectral Decomposition:** Develops matrix representations using eigenvalues and orthogonal eigenvectors under appropriate conditions.
> - **Symmetric Matrices:** Have particularly strong eigenvalue and diagonalization properties over the real numbers.
> - **Matrix Powers:** Diagonalization can simplify the computation of powers of matrices.

> [!info] Advanced
> - **Jordan Canonical Form:** Extends diagonalization to matrices that may not possess enough linearly independent eigenvectors.
> - **Spectral Theory:** Generalizes eigenvalue concepts to broader linear operators and infinite-dimensional spaces.
> - **Singular Value Decomposition:** Develops a related but more general matrix factorization that does not require the matrix to be square.

## 11. References

> [!bibliography]
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., Pearson, 2016.
> - Strang, Gilbert. *Introduction to Linear Algebra*, 6th ed., Wellesley-Cambridge Press, 2023.
> - Axler, Sheldon. *Linear Algebra Done Right*, 3rd ed., Springer, 2015.