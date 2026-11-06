---
type: technical-term
title: "Volume Integrals"
aliases:
  - Triple Integrals
abbreviation: ""
field:
  - Mathematics
subfield:
  - Vector Calculus
  - Integral Calculus
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - vector-calculus
  - integration
sources: []
related: []
projects: []
---

> [!abstract] Definition
> A **Volume Integral** is an integral that accumulates a scalar quantity throughout a three-dimensional region.
>
> In Cartesian coordinates, it is commonly represented as a triple integral.

## 1. Mathematical Formulation

> [!definition] Triple Integral
> For a scalar field $f(x,y,z)$ defined over a volume $V$:
>
> $$\iiint_V f(x,y,z)\,dV$$
>
> In Cartesian coordinates:
>
> $$dV=dx\,dy\,dz$$
>
> The integral accumulates the values of $f$ throughout the region.

## 2. Geometric Interpretation

> [!important] Accumulation over Volume
> A volume integral generalizes double integration from planar regions to three-dimensional regions.
>
> If $f=1$, the integral gives the volume:
>
> $$\operatorname{Vol}(V)=\iiint_V1\,dV$$
>
> If $f$ represents volume density, the integral gives the total quantity distributed throughout the region.

## 3. Coordinate Representations

> [!note] Cartesian Coordinates
> $$dV=dx\,dy\,dz$$

> [!note] Cylindrical Coordinates
> $$x=r\cos\theta,\qquad y=r\sin\theta,\qquad z=z$$
>
> $$dV=r\,dr\,d\theta\,dz$$

> [!note] Spherical Coordinates
> Using $\rho$ for radial distance, $\theta$ for azimuth, and $\phi$ for the angle measured from the positive $z$-axis:
>
> $$x=\rho\sin\phi\cos\theta$$
>
> $$y=\rho\sin\phi\sin\theta$$
>
> $$z=\rho\cos\phi$$
>
> $$dV=\rho^2\sin\phi\,d\rho\,d\phi\,d\theta$$

## 4. Properties

> [!important] Linearity
> $$\iiint_V(af+bg)\,dV
> =
> a\iiint_Vf\,dV+b\iiint_Vg\,dV$$

> [!important] Additivity
> If $V=V_1\cup V_2$ and the interiors are disjoint:
>
> $$\iiint_Vf\,dV
> =
> \iiint_{V_1}f\,dV
> +
> \iiint_{V_2}f\,dV$$

> [!important] Fubini's Theorem
> Under appropriate integrability conditions, a triple integral can be evaluated as an iterated integral.
>
> The order of integration can be changed when the relevant conditions are satisfied.

## 5. Relationship with Divergence

> [!important] Divergence Theorem
> The Divergence Theorem uses a volume integral of divergence:
>
> $$\iiint_V(\nabla\cdot\mathbf{F})\,dV$$
>
> This quantity equals the outward flux through the closed boundary surface of $V$, under the theorem's regularity assumptions.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Multiple Integrals:** Provides the general mathematical theory of integration over multidimensional regions.
- **Scalar Fields:** Provides the functions integrated over volumes.
- **Coordinate Systems:** Supports the representation of regions and volume elements.

### Downstream Knowledge
- **Divergence Theorem:** Relates volume integrals of divergence to closed-surface flux.
- **Mass and Density Integrals:** Uses volume integration to calculate total mass and other distributed quantities.
- **Integral Equations:** Uses accumulated field quantities over spatial domains.

## 7. References

> [!bibliography] Recommended References
> - Stewart, J. *Calculus: Early Transcendentals*. 8th edition, 2015.
> - Marsden, J. E., and Tromba, A. J. *Vector Calculus*. 6th edition, 2012.