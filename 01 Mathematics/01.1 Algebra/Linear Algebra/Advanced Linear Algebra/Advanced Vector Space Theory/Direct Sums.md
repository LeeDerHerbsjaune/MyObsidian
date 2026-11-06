---
type: technical-term
title: "Direct Sums"
aliases:
  - Direct Sum of Vector Spaces
abbreviation: ""
field:
  - Mathematics
subfield:
  - Linear Algebra
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - linear-algebra
  - vector-spaces
sources:
  - "Axler, Sheldon. Linear Algebra Done Right, 3rd ed., 2015."
  - "Roman, Steven. Advanced Linear Algebra, 3rd ed., 2008."
related: []
projects: []
---

> [!abstract] Definition
> A vector space $V$ is the **direct sum** of subspaces $U$ and $W$ if every vector in $V$ can be expressed uniquely as:
>
> $$v=u+w,\quad u\in U,\ w\in W$$
>
> This is denoted by:
>
> $$V=U\oplus W$$

> [!info] Core Concept
> A direct sum combines vector spaces while preserving the independence of their components.
>
> The uniqueness of the decomposition is the defining property: each vector has exactly one representation as a sum of components from the constituent subspaces.

> [!important] Internal Direct Sum
> For subspaces $U,W\subseteq V$:
>
> $$V=U\oplus W$$
>
> if and only if:
>
> $$V=U+W$$
>
> and:
>
> $$U\cap W=\{0\}$$
>
> The first condition guarantees that the subspaces span $V$. The second guarantees that their intersection contains only the zero vector, ensuring uniqueness.

> [!important] Multiple Subspaces
> For subspaces $U_1,\ldots,U_k$:
>
> $$V=U_1\oplus\cdots\oplus U_k$$
>
> means every $v\in V$ has a unique decomposition:
>
> $$v=u_1+\cdots+u_k,\quad u_i\in U_i$$
>
> For a finite family, this is equivalent to:
>
> $$V=U_1+\cdots+U_k$$
>
> together with the condition that the sum is independent: if
>
> $$u_1+\cdots+u_k=0$$
>
> with $u_i\in U_i$, then every $u_i=0$.

> [!example] Example
> Let:
>
> $$V=\mathbb{R}^3$$
>
> $$U=\operatorname{span}\{(1,0,0),(0,1,0)\}$$
>
> $$W=\operatorname{span}\{(0,0,1)\}$$
>
> Then:
>
> $$\mathbb{R}^3=U\oplus W$$
>
> Every vector $(x,y,z)$ has the unique decomposition:
>
> $$(x,y,z)=(x,y,0)+(0,0,z)$$

> [!important] Dimension Formula
> For finite-dimensional subspaces:
>
> $$\dim(U+W)=\dim(U)+\dim(W)-\dim(U\cap W)$$
>
> Therefore, if $V=U\oplus W$:
>
> $$\dim(V)=\dim(U)+\dim(W)$$

> [!note] External Direct Sum
> Given vector spaces $V_1,\ldots,V_n$, their external direct sum is:
>
> $$V_1\oplus\cdots\oplus V_n$$
>
> Its elements are tuples:
>
> $$(v_1,\ldots,v_n),\quad v_i\in V_i$$
>
> Addition and scalar multiplication are componentwise.
>
> For a finite family, the direct sum and direct product of vector spaces are naturally isomorphic.

> [!important] Projection Associated with a Direct Sum
> If $V=U\oplus W$, each vector has a unique decomposition $v=u+w$.
>
> Define:
>
> $$P_U(v)=u,\qquad P_W(v)=w$$
>
> These are linear projections satisfying:
>
> $$P_U^2=P_U,\qquad P_W^2=P_W$$
>
> $$P_U+P_W=I$$
>
> $$P_UP_W=P_WP_U=0$$
>
> These projections need not be orthogonal projections.

> [!warning] Direct Sum Is Not Necessarily Orthogonal
> A direct-sum decomposition requires unique algebraic decomposition, not perpendicular subspaces.
>
> Orthogonality requires additional inner-product structure.

> [!success] Foundation Knowledge
> - **Vector Spaces:** Provides the underlying algebraic structure.
> - **Subspaces:** Defines the components of an internal direct sum.
> - **Linear Independence:** Explains the uniqueness of decomposition.
> - **Spanning Sets and Basis:** Establishes existence and uniqueness of representations.

> [!success] Downstream Knowledge
> - **Relevant — Projection Operators:** Constructs linear projections associated with direct-sum decompositions.
> - **Relevant — Complementary Subspaces:** Studies subspaces whose direct sum equals the ambient space.
> - **Advanced — Invariant Subspace Decomposition:** Decomposes vector spaces into subspaces preserved by linear operators.
> - **Advanced — Primary Decomposition Theorem:** Decomposes finite-dimensional spaces into invariant subspaces associated with distinct factors of an operator's minimal polynomial.

> [!quote] References
> - Axler, Sheldon. *Linear Algebra Done Right*, 3rd ed., 2015.
> - Roman, Steven. *Advanced Linear Algebra*, 3rd ed., 2008.