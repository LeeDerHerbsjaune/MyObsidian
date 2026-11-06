---
type: technical-term
title: "Divergence Theorem"
aliases:
  - Gauss's Theorem
abbreviation: ""
field:
  - Mathematics
subfield:
  - Vector Calculus
  - Integral Theorems
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - vector-calculus
  - integral-theorems
sources: []
related: []
projects: []
---

> [!abstract] Definition
> The **Divergence Theorem** relates the outward flux of a vector field through a closed surface to the volume integral of the divergence of that field over the enclosed region.
>
> It connects local source and sink behavior with global outward flux.

## 1. Mathematical Formulation

> [!definition] Divergence Theorem
> Let $V$ be a bounded solid region with a sufficiently regular, closed, piecewise-smooth boundary surface $\partial V$.
>
> If $\mathbf{F}$ has continuous first-order partial derivatives on an open region containing $V$, then:
>
> $$\iint_{\partial V}
> \mathbf{F}\cdot\mathbf{n}\,dS
> =
> \iiint_V
> (\nabla\cdot\mathbf{F})\,dV$$
>
> Here:
> - $\partial V$ is the closed boundary surface.
> - $\mathbf{n}$ is the outward unit normal.
> - $\nabla\cdot\mathbf{F}$ is the divergence of the field.
> - $V$ is the enclosed volume.

## 2. Geometric Interpretation

> [!important] Local and Global Flux
> The surface integral measures the net outward flux through the entire closed boundary.
>
> The volume integral accumulates the local divergence throughout the enclosed region.
>
> The theorem states that the total outward flux equals the total divergence inside the volume.

## 3. Orientation

> [!important] Outward Normal
> The boundary surface must use the outward orientation.
>
> Choosing the inward normal reverses the sign of the flux integral:
>
> $$\iint_{\partial V}
> \mathbf{F}\cdot(-\mathbf{n})\,dS
> =
> -\iiint_V(\nabla\cdot\mathbf{F})\,dV$$

## 4. Important Consequences

> [!important] Divergence-Free Fields
> If:
>
> $$\nabla\cdot\mathbf{F}=0$$
>
> throughout $V$, then:
>
> $$\iint_{\partial V}\mathbf{F}\cdot\mathbf{n}\,dS=0$$
>
> The net outward flux through the closed boundary is zero.

> [!important] Conservation Interpretation
> Divergence describes local net production or removal of a field quantity.
>
> Integrating divergence over a volume gives the net outward flux across its boundary.
>
> This relationship is fundamental to mathematical formulations of conservation laws.

## 5. Relationship with Other Integral Theorems

> [!important] Connection to Green's Theorem
> The flux form of Green's Theorem is the two-dimensional analogue of the Divergence Theorem.

> [!important] Connection to Stokes' Theorem
> Both theorems relate local differential operators to global boundary integrals.
>
> - Stokes' Theorem relates curl to circulation.
> - The Divergence Theorem relates divergence to outward flux.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Divergence:** Provides the local differential quantity.
- **Surface Integrals:** Provides the boundary flux integral.
- **Volume Integrals:** Provides integration over the enclosed region.
- **Vector Fields:** Provides the field to which the theorem is applied.

### Downstream Knowledge
- **Conservation Laws:** Uses the relationship between local divergence and boundary flux.
- **Continuity Equations:** Expresses conservation of quantities in differential form.
- **Differential Equations:** Uses divergence operators in field equations.
- **Differential Forms:** Provides a general framework for the theorem.

## 7. References

> [!bibliography] Recommended References
> - Marsden, J. E., and Tromba, A. J. *Vector Calculus*. 6th edition, 2012.
> - Hubbard, J. H., and Hubbard, B. B. *Vector Calculus, Linear Algebra, and Differential Forms: A Unified Approach*. 5th edition, 2015.