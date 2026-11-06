---
type: technical-term
title: "Closed Forms"
aliases:
  - Closed Differential Forms
field:
  - Mathematics
subfield:
  - Differential Geometry
  - Differential Topology
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - differential-forms
sources:
  - "Bott & Tu (1982), Differential Forms in Algebraic Topology"
  - "Lee (2012), Introduction to Smooth Manifolds"
related: []
projects: []
---

> [!abstract] Definition
> A differential form $\omega$ is **closed** if its exterior derivative vanishes:
>
> $$d\omega=0$$
>
> The space of closed $k$-forms is commonly denoted
>
> $$Z^k(M)=\ker(d:\Omega^k(M)\rightarrow\Omega^{k+1}(M))$$

> [!important] Fundamental Property
> Because the exterior derivative is nilpotent,
>
> $$d^2=0$$
>
> every exact form is closed.
>
> Therefore,
>
> $$B^k(M)\subseteq Z^k(M)$$
>
> where $B^k(M)$ denotes the space of exact $k$-forms.

> [!note] Coordinate Example
> In $\mathbb{R}^3$, consider
>
> $$\omega=P\,dx+Q\,dy+R\,dz$$
>
> It is closed when
>
> $$d\omega=0$$
>
> which requires
>
> $$\frac{\partial Q}{\partial x}
> =\frac{\partial P}{\partial y}$$
>
> $$\frac{\partial R}{\partial x}
> =\frac{\partial P}{\partial z}$$
>
> $$\frac{\partial R}{\partial y}
> =\frac{\partial Q}{\partial z}$$

> [!note] Local Exactness
> The Poincaré lemma states that every closed differential form of positive degree is locally exact.
>
> Thus, around every point, a closed form can be expressed as the exterior derivative of another form.

> [!warning] Closed Does Not Always Mean Exact
> A closed form need not be globally exact.
>
> Global exactness depends on the topology of the manifold.
>
> This distinction is one of the foundations of de Rham cohomology.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Exterior Derivative — defines closedness.
> - Differential Forms — supplies the underlying spaces.
>
> **Downstream Knowledge**
> - Exact Forms — form a subspace of closed forms.
> - Poincaré Lemma — establishes local exactness.
> - De Rham Cohomology — measures the failure of closed forms to be globally exact.