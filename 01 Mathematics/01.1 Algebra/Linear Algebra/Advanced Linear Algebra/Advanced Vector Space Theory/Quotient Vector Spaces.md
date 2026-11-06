---
type: technical-term
title: "Quotient Vector Spaces"
aliases:
  - Factor Spaces
abbreviation: ""
field:
  - Mathematics
subfield:
  - Linear Algebra
  - Abstract Algebra
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - linear-algebra
  - vector-spaces
sources:
  - "Hoffman, Kenneth, and Ray Kunze. Linear Algebra, 2nd ed., 1971."
  - "Roman, Steven. Advanced Linear Algebra, 3rd ed., 2008."
related: []
projects: []
---

> [!abstract] Definition
> Let $V$ be a vector space over $\mathbb{F}$ and let $U$ be a subspace of $V$.
>
> The **quotient vector space** of $V$ by $U$, denoted by $V/U$, is the set of equivalence classes of vectors under the relation:
>
> $$v\sim w \iff v-w\in U$$
>
> Each equivalence class is called a coset:
>
> $$v+U=\{v+u\mid u\in U\}$$

> [!info] Core Concept
> A quotient space treats vectors as equivalent when their difference belongs to a selected subspace.
>
> Instead of distinguishing every vector in $V$, the quotient construction identifies vectors that differ only by an element of $U$.

> [!note] Vector Space Operations
> The operations are defined by:
>
> $$(v+U)+(w+U)=(v+w)+U$$
>
> $$a(v+U)=av+U$$
>
> These operations are well-defined because $U$ is a subspace.

> [!example] Example
> Let $V=\mathbb{R}^2$ and:
>
> $$U=\{(x,0)\mid x\in\mathbb{R}\}$$
>
> Then:
>
> $$V/U$$
>
> identifies all vectors that differ only in their first coordinate.
>
> Every coset is determined by the second coordinate. Therefore:
>
> $$\dim(V/U)=1$$

> [!important] Quotient Map
> The canonical quotient map is:
>
> $$\pi:V\rightarrow V/U$$
>
> defined by:
>
> $$\pi(v)=v+U$$
>
> It is linear and surjective, with:
>
> $$\ker(\pi)=U$$
>
> Thus, the quotient map sends each vector to its equivalence class.

> [!important] Dimension Theorem
> If $V$ is finite-dimensional:
>
> $$\dim(V/U)=\dim(V)-\dim(U)$$
>
> This follows from the relationship between a subspace, its quotient, and a basis extension.

> [!important] Quotient Spaces and Linear Maps
> Let $T:V\rightarrow W$ be linear and let $U\subseteq V$.
>
> A map:
>
> $$\widetilde{T}:V/U\rightarrow W$$
>
> defined by:
>
> $$\widetilde{T}(v+U)=T(v)$$
>
> is well-defined precisely when:
>
> $$U\subseteq\ker(T)$$
>
> In particular, if $U=\ker(T)$, the induced map:
>
> $$\widetilde{T}:V/\ker(T)\rightarrow\operatorname{im}(T)$$
>
> is an isomorphism.
>
> This is the First Isomorphism Theorem for vector spaces.

> [!important] Conceptual Interpretation
> Quotient spaces provide a way to remove a subspace from consideration by identifying all vectors that differ by elements of that subspace.
>
> This is an algebraic construction, not a geometric operation of physically subtracting one set of vectors from another.

> [!warning] Common Misconception
> $V/U$ is not generally the set-theoretic difference $V\setminus U$.
>
> Its elements are cosets, not individual vectors.

> [!success] Foundation Knowledge
> - **Vector Spaces:** Provides the underlying structure.
> - **Subspaces:** Defines the equivalence relation used to construct the quotient.
> - **Equivalence Relations:** Explains the partition of $V$ into cosets.
> - **Linear Transformations and Kernels:** Establishes the relationship between quotient spaces and induced maps.

> [!success] Downstream Knowledge
> - **Relevant — Isomorphism Theorems:** Formalizes the relationship between kernels, images, and quotient spaces.
> - **Relevant — Dual Spaces and Annihilators:** Connects quotient spaces to subspaces of the dual space.
> - **Advanced — Quotient Modules:** Generalizes quotient vector spaces to modules over rings.
> - **Advanced — Quotient Topological Vector Spaces:** Adds topological structure to quotient constructions.

> [!quote] References
> - Hoffman, Kenneth, and Ray Kunze. *Linear Algebra*, 2nd ed., 1971.
> - Roman, Steven. *Advanced Linear Algebra*, 3rd ed., 2008.