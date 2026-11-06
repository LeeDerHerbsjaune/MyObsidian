---
type: technical-term
title: "Bilinear Forms"
aliases:
  - Bilinear Form
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
  - multilinear-algebra
sources:
  - "Greub, Werner H. Multilinear Algebra, 2nd ed., 1978."
  - "Roman, Steven. Advanced Linear Algebra, 3rd ed., 2008."
related: []
projects: []
---

> [!abstract] Definition
> Let $V$ be a vector space over a field $\mathbb{F}$.
>
> A **bilinear form** is a function:
>
> $$B:V\times V\rightarrow\mathbb{F}$$
>
> that is linear in each argument when the other argument is held fixed.
>
> Specifically:
>
> $$B(u+v,w)=B(u,w)+B(v,w)$$
>
> $$B(au,v)=aB(u,v)$$
>
> $$B(u,v+w)=B(u,v)+B(u,w)$$
>
> $$B(u,av)=aB(u,v)$$

> [!info] Core Concept
> A bilinear form takes two vectors and produces a scalar.
>
> Unlike a linear functional, which acts on one vector, a bilinear form is linear independently in two vector arguments.

> [!important] Matrix Representation
> Let $V$ be finite-dimensional with an ordered basis:
>
> $$B=(v_1,\ldots,v_n)$$
>
> Define the matrix $A$ by:
>
> $$A_{ij}=B(v_i,v_j)$$
>
> If vectors $u,v$ have coordinate columns $[u]_B$ and $[v]_B$, then:
>
> $$B(u,v)=[u]_B^T A[v]_B$$
>
> Thus, a bilinear form can be represented by a matrix once a basis is chosen.

> [!important] Symmetric Bilinear Forms
> A bilinear form is **symmetric** if:
>
> $$B(u,v)=B(v,u)$$
>
> for all $u,v\in V$.
>
> In matrix representation, this is equivalent to:
>
> $$A^T=A$$

> [!important] Alternating Bilinear Forms
> A bilinear form is **alternating** if:
>
> $$B(v,v)=0$$
>
> for every $v\in V$.
>
> Over a field of characteristic different from two, an alternating bilinear form is skew-symmetric:
>
> $$B(u,v)=-B(v,u)$$
>
> Equivalently:
>
> $$A^T=-A$$
>
> In characteristic two, skew-symmetry alone does not necessarily imply alternation.

> [!important] Nondegeneracy
> A bilinear form $B$ is **nondegenerate** if:
>
> $$B(v,w)=0\quad\forall w\in V$$
>
> implies:
>
> $$v=0$$
>
> Equivalently, the linear map:
>
> $$\Phi_B:V\rightarrow V^*$$
>
> defined by:
>
> $$\Phi_B(v)(w)=B(v,w)$$
>
> is injective.
>
> If $V$ is finite-dimensional, nondegeneracy is equivalent to $\Phi_B$ being an isomorphism, and to the matrix $A$ being invertible.

> [!example] Example
> On $\mathbb{R}^2$, define:
>
> $$B(u,v)=u_1v_1+u_2v_2$$
>
> Its matrix in the standard basis is:
>
> $$A=\begin{bmatrix}1&0\\0&1\end{bmatrix}$$
>
> This is a symmetric, nondegenerate bilinear form.

> [!warning] Bilinear Forms and Inner Products
> Every real inner product is a symmetric positive-definite bilinear form.
>
> However, not every bilinear form is an inner product: a general bilinear form need not be symmetric, positive-definite, or even nondegenerate.
>
> Complex inner products are sesquilinear rather than bilinear under the usual convention: they involve complex conjugation in one argument.

> [!success] Foundation Knowledge
> - **Vector Spaces:** Defines the arguments of the form.
> - **Dual Vector Spaces:** Provides the space of linear functionals associated with each argument.
> - **Tensor Products:** Provides the natural algebraic setting for representing bilinear forms as linear functionals on tensor products.
> - **Matrices:** Supports coordinate representations and nondegeneracy tests.

> [!success] Downstream Knowledge
> - **Relevant — Quadratic Forms:** Obtains scalar-valued degree-two functions from bilinear forms.
> - **Relevant — Symmetric Bilinear Forms:** Studies classification and structural properties of symmetric forms.
> - **Relevant — Alternating Forms:** Develops skew-symmetric and alternating structures.
> - **Advanced — Classification of Bilinear Forms:** Studies equivalence and canonical representations under changes of basis.
> - **Advanced — Symplectic Linear Algebra:** Studies nondegenerate alternating bilinear forms.

> [!quote] References
> - Greub, Werner H. *Multilinear Algebra*, 2nd ed., 1978.
> - Roman, Steven. *Advanced Linear Algebra*, 3rd ed., 2008.