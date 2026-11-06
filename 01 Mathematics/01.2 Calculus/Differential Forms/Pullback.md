---
type: technical-term
title: "Pullback"
aliases:
  - Pullback of Differential Forms
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
  - "Lee (2012), Introduction to Smooth Manifolds"
  - "Spivak (1965), Calculus on Manifolds"
related: []
projects: []
---

> [!abstract] Definition
> The **pullback** is an operation that transfers differential forms from the target manifold of a smooth map to its domain.
>
> For a smooth map
>
> $$F:M\rightarrow N$$
>
> it defines
>
> $$F^*:\Omega^k(N)\rightarrow\Omega^k(M)$$

> [!important] Pointwise Definition
> If $\omega$ is a $k$-form on $N$, then at $p\in M$:
>
> $$(F^*\omega)_p(v_1,\ldots,v_k)
> =
> \omega_{F(p)}
> (dF_p(v_1),\ldots,dF_p(v_k))$$
>
> where $dF_p$ is the differential (pushforward) of the map.

> [!note] Coordinate Formula
> For a 1-form
>
> $$\omega=\omega_i(y)\,dy^i$$
>
> and a coordinate representation $y^i=F^i(x)$:
>
> $$F^*\omega
> =
> \omega_i(F(x))
> \frac{\partial F^i}{\partial x^j}dx^j$$
>
> The pullback combines function composition with the Jacobian of the map.

> [!important] Algebraic Properties
> Pullback preserves wedge products:
>
> $$F^*(\alpha\wedge\beta)
> =
> F^*\alpha\wedge F^*\beta$$
>
> It also commutes with exterior differentiation:
>
> $$F^*(d\omega)=d(F^*\omega)$$

> [!note] Composition
> For smooth maps
>
> $$M\xrightarrow{F}N\xrightarrow{G}P$$
>
> the pullback satisfies
>
> $$(G\circ F)^*=F^*\circ G^*$$

> [!warning] Pullback Versus Pushforward
> Pullback acts on covariant objects such as differential forms and transfers them in the direction opposite to the map.
>
> Pushforward acts on tangent vectors through the differential of the map.
>
> They are related but are not interchangeable operations.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Smooth Maps — provides the map between manifolds.
> - Differential Forms — provides the objects being pulled back.
> - Tangent Maps — provides the differential $dF$.
>
> **Downstream Knowledge**
> - Integration of Differential Forms — uses pullbacks to define integration through parametrizations.
> - Differential Topology — uses pullbacks to study smooth maps.
> - De Rham Cohomology — pullbacks induce maps between cohomology groups.