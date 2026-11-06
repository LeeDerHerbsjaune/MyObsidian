---
type: technical-term
title: "Cayley-Hamilton Theorem"
aliases:
  - Cayley–Hamilton Theorem
abbreviation: "CH Theorem"
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
  - matrix-theorems
sources:
  - "Axler, Sheldon, Linear Algebra Done Right, 3rd ed., 2015."
  - "Horn, Roger A., and Charles R. Johnson, Matrix Analysis, 2nd ed., 2013."
related: []
projects: []
---

> [!abstract] Definition
> The **Cayley–Hamilton theorem** states that every square matrix satisfies its own characteristic polynomial.
>
> In other words, substituting a square matrix into its characteristic polynomial produces the zero matrix.

## 1. Mathematical Formulation

> [!math] Theorem
> Let $A\in\mathbb{F}^{n\times n}$ have characteristic polynomial:
>
> $$
> p_A(t)=
> t^n+c_{n-1}t^{n-1}
> +\cdots+c_1t+c_0
> $$
>
> Then:
>
> $$
> \boxed{
> p_A(A)=
> A^n+c_{n-1}A^{n-1}
> +\cdots+c_1A+c_0I=0
> }
> $$
>
> Here, the constant term $c_0$ is multiplied by the identity matrix, not treated as a scalar matrix entry.

## 2. Understanding Polynomial Evaluation

> [!important] Matrix Substitution
> For a polynomial:
>
> $$
> p(t)=a_nt^n+\cdots+a_1t+a_0
> $$
>
> its evaluation at a square matrix $A$ is:
>
> $$
> p(A)=a_nA^n+\cdots+a_1A+a_0I
> $$
>
> The constant term is interpreted as $a_0I$ so that all terms are square matrices of the same order.

## 3. Example: 2 × 2 Matrix

> [!example] Verification
> Consider:
>
> $$
> A=
> \begin{bmatrix}
> 1&2\\
> 0&3
> \end{bmatrix}
> $$
>
> Its characteristic polynomial is:
>
> $$
> p_A(t)=(t-1)(t-3)
> =t^2-4t+3
> $$
>
> By the Cayley–Hamilton theorem:
>
> $$
> A^2-4A+3I=0
> $$
>
> Calculate:
>
> $$
> A^2=
> \begin{bmatrix}
> 1&8\\
> 0&9
> \end{bmatrix}
> $$
>
> Therefore:
>
> $$
> A^2-4A+3I
> =
> \begin{bmatrix}
> 1&8\\
> 0&9
> \end{bmatrix}
> -
> \begin{bmatrix}
> 4&8\\
> 0&12
> \end{bmatrix}
> +
> \begin{bmatrix}
> 3&0\\
> 0&3
> \end{bmatrix}
> =
> \begin{bmatrix}
> 0&0\\
> 0&0
> \end{bmatrix}
> $$

## 4. Consequences

> [!important] Reduction of Matrix Powers
> Suppose:
>
> $$
> A^n+c_{n-1}A^{n-1}
> +\cdots+c_0I=0
> $$
>
> Then:
>
> $$
> A^n=
> -c_{n-1}A^{n-1}
> -\cdots-c_0I
> $$
>
> Consequently, every higher power of $A$ can be expressed as a linear combination of lower powers:
>
> $$
> I,A,A^2,\ldots,A^{n-1}
> $$
>
> This is useful for simplifying matrix polynomial expressions.

## 5. Computing the Inverse

> [!note] Inverse from the Characteristic Polynomial
> Suppose $A$ is invertible and:
>
> $$
> p_A(t)=
> t^n+c_{n-1}t^{n-1}
> +\cdots+c_1t+c_0
> $$
>
> Since $A$ is invertible, $c_0=(-1)^n\det(A)\neq0$.
>
> From Cayley–Hamilton:
>
> $$
> A^n+c_{n-1}A^{n-1}
> +\cdots+c_1A+c_0I=0
> $$
>
> Multiplying by $A^{-1}$:
>
> $$
> A^{n-1}+c_{n-1}A^{n-2}
> +\cdots+c_1I+c_0A^{-1}=0
> $$
>
> Therefore:
>
> $$
> \boxed{
> A^{-1}
> =
> -\frac{1}{c_0}
> \left(
> A^{n-1}+c_{n-1}A^{n-2}
> +\cdots+c_1I
> \right)
> }
> $$
>
> This expresses the inverse as a polynomial in $A$.

## 6. Relationship to the Minimal Polynomial

> [!note] Minimal Polynomial
> The **minimal polynomial** of a matrix $A$ is the monic polynomial of smallest positive degree satisfying:
>
> $$
> m_A(A)=0
> $$
>
> The Cayley–Hamilton theorem guarantees that such a polynomial exists and divides the characteristic polynomial:
>
> $$
> \boxed{
> m_A(t)\mid p_A(t)
> }
> $$
>
> The minimal polynomial contains important information about the algebraic structure of the matrix and its diagonalizability.

## 7. Important Properties

> [!important] Key Results
> - Every square matrix satisfies its characteristic polynomial.
> - The characteristic polynomial annihilates the matrix.
> - Every polynomial that annihilates a matrix is divisible by its minimal polynomial.
> - The minimal polynomial divides the characteristic polynomial.
> - Higher powers of a matrix can be reduced to lower-degree polynomial expressions.
> - For an invertible matrix, the inverse can be expressed as a polynomial in the matrix.

## 8. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Characteristic Polynomial:** Defines the polynomial evaluated at the matrix.
> - **Determinants:** Required to construct the characteristic polynomial.
> - **Matrices:** Provides the objects to which polynomial expressions are applied.

> [!info] Relevant
> - **Polynomial Algebra:** Provides polynomial evaluation and divisibility.
> - **Matrix Multiplication:** Required for matrix powers.

### Downstream Knowledge

> [!info] Relevant
> - **Minimal Polynomial:** Develops the smallest polynomial that annihilates a matrix.
> - **Matrix Inverse:** Cayley–Hamilton can express an inverse as a polynomial in the matrix.
> - **Matrix Powers:** Enables reduction of higher powers.

> [!info] Advanced
> - **Jordan Canonical Form:** The minimal polynomial and its factor multiplicities characterize important aspects of Jordan structure.
> - **Matrix Functions:** Polynomial identities help simplify and evaluate functions of matrices.

## 9. References

> [!bibliography]
> - Axler, Sheldon. *Linear Algebra Done Right*, 3rd ed., Springer, 2015.
> - Horn, Roger A., and Charles R. Johnson. *Matrix Analysis*, 2nd ed., Cambridge University Press, 2013.