---
type: technical-term
title: "Algebraic and Geometric Multiplicity"
aliases:
  - Eigenvalue Multiplicity
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
  - eigenvalue-multiplicity
sources:
  - "Lay, David C., Linear Algebra and Its Applications, 5th ed., 2016."
  - "Axler, Sheldon, Linear Algebra Done Right, 3rd ed., 2015."
related: []
projects: []
---

> [!abstract] Definition
> **Algebraic multiplicity** and **geometric multiplicity** describe two different aspects of an eigenvalue.
>
> - Algebraic multiplicity measures how many times an eigenvalue occurs as a root of the characteristic polynomial.
> - Geometric multiplicity measures the dimension of its eigenspace.

## 1. Algebraic Multiplicity

> [!abstract] Definition
> The algebraic multiplicity of an eigenvalue $\lambda$ is its multiplicity as a root of the characteristic polynomial.
>
> If:
>
> $$
> p_A(t)=(t-\lambda)^kq(t)
> $$
>
> where $q(\lambda)\neq0$, then:
>
> $$
> \boxed{\operatorname{AM}(\lambda)=k}
> $$

## 2. Geometric Multiplicity

> [!abstract] Definition
> The geometric multiplicity of an eigenvalue $\lambda$ is the dimension of its eigenspace:
>
> $$
> \boxed{
> \operatorname{GM}(\lambda)
> =
> \dim\operatorname{Null}(A-\lambda I)
> }
> $$
>
> It counts the maximum number of linearly independent eigenvectors associated with that eigenvalue.

## 3. Fundamental Inequality

> [!important] Multiplicity Theorem
> For every eigenvalue $\lambda$:
>
> $$
> \boxed{
> 1\leq
> \operatorname{GM}(\lambda)
> \leq
> \operatorname{AM}(\lambda)
> }
> $$
>
> The geometric multiplicity cannot exceed the algebraic multiplicity.
>
> Both multiplicities are positive integers.

## 4. Relationship to Diagonalizability

> [!important] Diagonalizability Criterion
> An $n\times n$ matrix over a field is diagonalizable if and only if:
>
> $$
> \boxed{
> \sum_{\lambda}
> \operatorname{GM}(\lambda)=n
> }
> $$
>
> where the sum is over all distinct eigenvalues.
>
> Equivalently, the matrix must have a basis consisting of eigenvectors.
>
> Since:
>
> $$
> \operatorname{GM}(\lambda)
> \leq\operatorname{AM}(\lambda)
> $$
>
> and the sum of algebraic multiplicities is $n$ when the characteristic polynomial splits over the field, diagonalizability is equivalent to:
>
> $$
> \operatorname{GM}(\lambda)
> =
> \operatorname{AM}(\lambda)
> $$
>
> for every distinct eigenvalue, provided the characteristic polynomial splits over the field.

## 5. Example of Multiplicity

> [!example] Repeated Eigenvalue
> Consider:
>
> $$
> A=
> \begin{bmatrix}
> 2&0\\
> 0&2
> \end{bmatrix}
> $$
>
> Its characteristic polynomial is:
>
> $$
> p_A(t)=(t-2)^2
> $$
>
> Therefore:
>
> $$
> \operatorname{AM}(2)=2
> $$
>
> Since:
>
> $$
> A-2I=
> \begin{bmatrix}
> 0&0\\
> 0&0
> \end{bmatrix}
> $$
>
> its null space is $\mathbb{R}^2$:
>
> $$
> \operatorname{GM}(2)=2
> $$
>
> Both multiplicities are equal, so the matrix is diagonalizable.

## 6. When Multiplicities Differ

> [!warning] Non-Diagonalizable Case
> If an eigenvalue has:
>
> $$
> \operatorname{GM}(\lambda)
> <
> \operatorname{AM}(\lambda)
> $$
>
> then the matrix does not have enough linearly independent eigenvectors to be diagonalizable.
>
> Such a matrix is called **defective**.

## 7. Knowledge Relationships

### Foundation Knowledge

> [!info] Essential
> - **Characteristic Polynomial:** Determines algebraic multiplicity.
> - **Eigenspaces:** Provides the vector spaces whose dimensions determine geometric multiplicity.
> - **Eigenvalues:** Establishes the scalar whose multiplicities are being measured.

> [!info] Relevant
> - **Rank-Nullity Theorem:** Determines eigenspace dimensions through nullity.

### Downstream Knowledge

> [!info] Relevant
> - **Diagonalization:** Uses the relationship between algebraic and geometric multiplicities to determine diagonalizability.

> [!info] Advanced
> - **Jordan Canonical Form:** Describes the structure of matrices when geometric and algebraic multiplicities differ.
> - **Minimal Polynomial:** Provides another criterion for diagonalizability through the multiplicities of its polynomial factors.

## 8. References

> [!bibliography]
> - Lay, David C. *Linear Algebra and Its Applications*, 5th ed., 2016.
> - Axler, Sheldon. *Linear Algebra Done Right*, 3rd ed., 2015.