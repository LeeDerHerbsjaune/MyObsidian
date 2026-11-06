---
type: technical-term
title: "Quadratic Forms"
aliases:
  - Quadratic Form
abbreviation: ""
field:
  - Mathematics
subfield:
  - Linear Algebra
  - Multilinear Algebra
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - linear-algebra
  - quadratic-forms
sources:
  - "Roman, Steven. Advanced Linear Algebra, 3rd ed., 2008."
  - "Horn, Roger A., and Charles R. Johnson. Matrix Analysis, 2nd ed., 2013."
related: []
projects: []
---

> [!abstract] Definition
> Let $V$ be a vector space over a field $\mathbb{F}$.
>
> A **quadratic form** is a function:
>
> $$Q:V\rightarrow\mathbb{F}$$
>
> that can be expressed as a homogeneous polynomial of degree two in vector coordinates.
>
> In finite-dimensional coordinates:
>
> $$Q(x)=x^T A x$$
>
> for some matrix $A$.
>
> Over fields of characteristic different from two, $A$ can always be chosen symmetric.

> [!info] Core Concept
> A quadratic form assigns a scalar to each vector using expressions that are quadratic in its components.
>
> Unlike a bilinear form, it takes one vector as its argument. Its algebraic structure is closely related to symmetric bilinear forms.

> [!important] Associated Symmetric Bilinear Form
> If the field has characteristic different from two, a quadratic form determines a unique symmetric bilinear form:
>
> $$B_Q(u,v)=\frac{1}{2}\left(Q(u+v)-Q(u)-Q(v)\right)$$
>
> This is called the **polarization identity**.
>
> Conversely, a symmetric bilinear form $B$ defines a quadratic form:
>
> $$Q(v)=B(v,v)$$
>
> Therefore, over fields of characteristic different from two, quadratic forms and symmetric bilinear forms are naturally equivalent descriptions of the same structure.

> [!important] Matrix Representation
> Let $x\in\mathbb{F}^n$ and let $A$ be symmetric.
>
> Then:
>
> $$Q(x)=x^T A x$$
>
> For example:
>
> $$Q(x_1,x_2)=3x_1^2+2x_1x_2+4x_2^2$$
>
> can be represented by:
>
> $$A=\begin{bmatrix}3&1\\1&4\end{bmatrix}$$
>
> The off-diagonal entries are half the coefficient of the mixed term.

> [!important] Change of Coordinates
> Suppose:
>
> $$x=Py$$
>
> for an invertible change-of-coordinate matrix $P$.
>
> Then:
>
> $$Q(x)=y^T(P^TAP)y$$
>
> Thus, the matrix transforms by:
>
> $$A'=P^TAP$$
>
> This transformation is called **matrix congruence**.
>
> It differs from similarity:
>
> $$A'=P^{-1}AP$$
>
> which describes a change of basis for a linear operator.

> [!important] Classification over the Real Numbers
> A real symmetric matrix can be orthogonally diagonalized:
>
> $$A=Q\Lambda Q^T$$
>
> Consequently, under an orthogonal coordinate transformation:
>
> $$Q(x)=\lambda_1y_1^2+\cdots+\lambda_ny_n^2$$
>
> where $\lambda_i$ are the eigenvalues of $A$.
>
> More generally, Sylvester's law of inertia states that every real quadratic form can be reduced by an invertible change of coordinates to a diagonal form whose numbers of positive, negative, and zero coefficients are invariant.

> [!important] Definiteness
> A real quadratic form is:
>
> - **Positive definite** if $Q(x)>0$ for every $x\neq0$.
> - **Positive semidefinite** if $Q(x)\geq0$ for every $x$.
> - **Negative definite** if $Q(x)<0$ for every $x\neq0$.
> - **Negative semidefinite** if $Q(x)\leq0$ for every $x$.
> - **Indefinite** if it takes both positive and negative values.
>
> For a real symmetric matrix $A$, positive definiteness is equivalent to all eigenvalues being positive.

> [!example] Example
> Consider:
>
> $$Q(x_1,x_2)=x_1^2+4x_2^2$$
>
> Its matrix is:
>
> $$A=\begin{bmatrix}1&0\\0&4\end{bmatrix}$$
>
> Since both eigenvalues are positive:
>
> $$Q(x_1,x_2)>0$$
>
> for every nonzero vector. Therefore, $Q$ is positive definite.

> [!warning] Field Characteristic
> The polarization identity requires division by two.
>
> In characteristic two, a quadratic form cannot generally be recovered uniquely from its associated bilinear form. The relationship between quadratic and bilinear forms therefore requires a different treatment.

> [!warning] Quadratic Forms Are Not Necessarily Norms
> A quadratic form does not automatically satisfy the axioms required of a norm.
>
> For example, it may be negative for some nonzero vectors or may vanish on nonzero vectors.

> [!success] Foundation Knowledge
> - **Vector Spaces:** Defines the domain of the quadratic form.
> - **Bilinear Forms:** Provides the associated symmetric bilinear structure.
> - **Matrices:** Provides coordinate representation.
> - **Eigenvalues and Eigenvectors:** Supports diagonalization and definiteness analysis.
> - **Change of Basis:** Explains the transformation of quadratic-form matrices under coordinate changes.

> [!success] Downstream Knowledge
> - **Relevant — Classification of Quadratic Forms:** Studies canonical forms and invariants under congruence.
> - **Relevant — Positive Definite Matrices:** Develops the matrix conditions associated with positive-definite quadratic forms.
> - **Relevant — Sylvester's Law of Inertia:** Establishes the invariance of positive, negative, and zero indices under invertible coordinate transformations.
> - **Advanced — Quadratic Optimization:** Uses quadratic forms to represent quadratic objective functions.
> - **Advanced — Quadratic Spaces:** Studies vector spaces equipped with quadratic forms.

> [!quote] References
> - Roman, Steven. *Advanced Linear Algebra*, 3rd ed., 2008.
> - Horn, Roger A., and Charles R. Johnson. *Matrix Analysis*, 2nd ed., 2013.E