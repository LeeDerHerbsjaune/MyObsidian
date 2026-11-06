---
type: technical-term
title: "Projection Matrices"
aliases:
  - Projection Matrix
  - Idempotent Matrix
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
  - "Strang, Gilbert. Introduction to Linear Algebra. 5th ed., 2016."
  - "Meyer, Carl D. Matrix Analysis and Applied Linear Algebra. 2000."
related: []
projects: []
---

> [!abstract] Definition
> A **projection matrix** is an idempotent matrix representing a linear transformation that projects vectors onto a subspace.
>
> Applying the transformation repeatedly produces the same result after the first projection.

## 1. Mathematical Definition

> [!definition] Idempotent Matrix
> A square matrix $P\in\mathbb{F}^{n\times n}$ is idempotent if:
>
> $$P^2=P$$
>
> Such a matrix represents a projection operator.

> [!important] Projection Behavior
> For any vector $x$:
>
> $$P(Px)=Px$$
>
> Once a vector has been projected, applying the same projection again does not change it.

## 2. Range and Null Space

> [!important] Range
> The range of $P$ is the subspace onto which vectors are projected:
>
> $$\operatorname{Range}(P)=\{Px:x\in\mathbb{F}^n\}$$

> [!important] Null Space
> The null space contains the vectors eliminated by the projection:
>
> $$\operatorname{Null}(P)=\{x:Px=0\}$$

> [!important] Direct-Sum Decomposition
> Every idempotent matrix gives:
>
> $$\mathbb{F}^n=
> \operatorname{Range}(P)\oplus\operatorname{Null}(P)$$
>
> The decomposition is direct, but the two subspaces need not be orthogonal.

## 3. Orthogonal and Oblique Projections

> [!definition] Orthogonal Projection
> A projection matrix is an orthogonal projection if it is also Hermitian:
>
> $$P^2=P,\qquad P^*=P$$
>
> For real matrices:
>
> $$P^2=P,\qquad P^T=P$$
>
> In this case, the null space is the orthogonal complement of the range.

> [!definition] Oblique Projection
> A projection is oblique if it is not self-adjoint.
>
> Its range and null space are complementary subspaces, but they are not generally orthogonal.

## 4. Matrix Construction

> [!important] Projection onto a Column Space
> Let $A\in\mathbb{R}^{m\times n}$ have full column rank.
>
> The orthogonal projection onto $\operatorname{Col}(A)$ is:
>
> $$P=A(A^TA)^{-1}A^T$$
>
> This matrix satisfies:
>
> $$P^T=P,\qquad P^2=P$$

> [!note] Orthonormal Basis Form
> If $Q$ has orthonormal columns spanning the target subspace:
>
> $$Q^TQ=I$$
>
> then:
>
> $$P=QQ^T$$
>
> This avoids explicitly computing $(A^TA)^{-1}$.

## 5. Important Properties

> [!important] Eigenvalues
> Every eigenvalue of an idempotent matrix is either zero or one:
>
> $$\lambda^2=\lambda$$
>
> $$\lambda\in\{0,1\}$$

> [!important] Rank and Trace
> For every idempotent matrix:
>
> $$\operatorname{rank}(P)=\operatorname{tr}(P)$$
>
> Both equal the dimension of the projected subspace.

> [!important] Diagonalizability
> Every idempotent matrix is diagonalizable because its minimal polynomial divides:
>
> $$t(t-1)$$
>
> This polynomial has distinct roots.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Linear Transformations** — provide the operator interpretation.
- **Subspaces** — define the range and null space.
- **Matrix Multiplication** — defines idempotence.
- **Orthogonality and Inner Products** — distinguish orthogonal projections from oblique projections.

### Downstream Knowledge
- **Orthogonal Projections** — develop the geometric theory.
- **Least Squares** — uses orthogonal projection onto a column space.
- **Direct-Sum Decomposition** — describes the decomposition into range and null space.
- **Spectral Theory** — studies projection operators as self-adjoint idempotents.

## 7. References
1. Strang, Gilbert. *Introduction to Linear Algebra*. 5th ed., Wellesley-Cambridge Press, 2016.
2. Meyer, Carl D. *Matrix Analysis and Applied Linear Algebra*. SIAM, 2000.