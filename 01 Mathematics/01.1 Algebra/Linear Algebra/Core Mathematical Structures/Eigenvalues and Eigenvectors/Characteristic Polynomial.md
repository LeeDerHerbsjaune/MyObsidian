---
type: technical-term
title: "Characteristic Polynomial"
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
  - characteristic-polynomial
sources:
  - "Lay, David C., Linear Algebra and Its Applications, 5th ed., 2016."
  - "Axler, Sheldon, Linear Algebra Done Right, 3rd ed., 2015."
related: []
projects: []
---

> [!abstract] Definition
> The **characteristic polynomial** of a square matrix $A$ is the polynomial obtained by taking the determinant of $\lambda I-A$:
>
> $$
> \boxed{
> p_A(\lambda)=\det(\lambda I-A)
> }
> $$
>
> Its roots are the eigenvalues of $A$, counted with algebraic multiplicity.

## 1. Mathematical Structure

> [!math] General Form
> For an $n\times n$ matrix:
>
> $$
> p_A(\lambda)=
> \lambda^n+c_{n-1}\lambda^{n-1}
> +\cdots+c_1\lambda+c_0
> $$
>
> It is a monic polynomial of degree $n$.

## 2. Characteristic Polynomial of a 2 × 2 Matrix

> [!example] Derivation
> Let:
>
> $$
> A=
> \begin{bmatrix}
> a&b\\
> c&d
> \end{bmatrix}
> $$
>
> Then:
>
> $$
> p_A(\lambda)
> =
> \det
> \begin{bmatrix}
> \lambda-a&-b\\
> -c&\lambda-d
> \end{bmatrix}
> $$
>
> Therefore:
>
> $$
> \boxed{
> p_A(\lambda)
> =
> \lambda^2-\operatorname{tr}(A)\lambda+\det(A)
> }
> $$

## 3. Eigenvalues as Polynomial Roots

> [!important] Characteristic Equation
> A scalar $\lambda$ is an eigenvalue of $A$ if and only if:
>
> $$
> p_A(\lambda)=0
> $$
>
> Therefore, finding eigenvalues is equivalent to finding the roots of the characteristic polynomial.

## 4. Trace and Determinant

> [!math] Coefficients
> For an $n\times n$ matrix:
>
> $$
> p_A(\lambda)=
> \lambda^n-\operatorname{tr}(A)\lambda^{n-1}
> +\cdots+(-1)^n\det(A)
> $$
>
> The coefficient of $\lambda^{n-1}$ is the negative trace, and the constant term is $(-1)^n\det(A)$.

## 5. Similarity Invariance

> [!important] Similar Matrices
> If $B=P^{-1}AP$ for an invertible matrix $P$, then:
>
> $$
> p_B(\lambda)=p_A(\lambda)
> $$
>
> Therefore, similar matrices have the same characteristic polynomial and the same eigenvalues, including algebraic multiplicities.

## 6. Cayley–Hamilton Connection

> [!note] Polynomial Evaluation
> The characteristic polynomial is not only used to find eigenvalues.
>
> The Cayley–Hamilton theorem states that:
>
> $$
> p_A(A)=0
> $$
>
> Thus, the polynomial also defines an identity satisfied by the matrix itself.

## 7. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Determinants:** Required to define the characteristic polynomial.
> - **Matrices:** Provides the square matrix and identity matrix.
> - **Polynomial Algebra:** Required to analyze polynomial roots.

> [!info] Relevant
> - **Eigenvalues:** The roots of the characteristic polynomial are precisely the eigenvalues.

### Downstream Knowledge

> [!info] Relevant
> - **Eigenspaces:** Uses eigenvalues to construct the matrices $A-\lambda I$.
> - **Algebraic and Geometric Multiplicity:** Algebraic multiplicity is determined by root multiplicity.
> - **Cayley–Hamilton Theorem:** Applies the characteristic polynomial to its matrix.

> [!info] Advanced
> - **Minimal Polynomial:** Develops a related polynomial characterization of a matrix.
> - **Jordan Canonical Form:** Uses characteristic-polynomial information to analyze matrix structure.

## 8. References

> [!bibliography]
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., 2016.
> - Axler, Sheldon. *Linear Algebra Done Right*, 3rd ed., 2015.