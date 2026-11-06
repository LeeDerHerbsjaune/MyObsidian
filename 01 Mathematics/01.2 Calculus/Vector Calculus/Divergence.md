---
type: technical-term
title: "Divergence"
aliases: []
abbreviation: ""
field:
  - Mathematics
subfield:
  - Vector Calculus
  - Differential Operators
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - vector-calculus
  - differential-operators
sources: []
related: []
projects: []
---

> [!abstract] Definition
> **Divergence** is a scalar differential operator that measures the local net outward flux density of a vector field.
>
> It describes whether a vector field behaves locally like a source, a sink, or neither.

## 1. Mathematical Formulation

> [!definition] Divergence in Cartesian Coordinates
> For a differentiable vector field:
>
> $$\mathbf{F}(x,y,z)=
> \begin{bmatrix}
> P(x,y,z)\\
> Q(x,y,z)\\
> R(x,y,z)
> \end{bmatrix}$$
>
> Its divergence is:
>
> $$\nabla\cdot\mathbf{F}
> =
> \frac{\partial P}{\partial x}
> +
> \frac{\partial Q}{\partial y}
> +
> \frac{\partial R}{\partial z}$$
>
> The result is a scalar field.

## 2. Geometric Interpretation

> [!important] Local Flux Density
> Divergence describes the limiting outward flux per unit volume around a point.
>
> Informally:
> - Positive divergence indicates local source-like behavior.
> - Negative divergence indicates local sink-like behavior.
> - Zero divergence indicates locally balanced flux.

> [!note] Important Distinction
> Zero divergence does not imply that a vector field is zero.
>
> A field can have nonzero vectors while its local net outward flux density is zero.

## 3. Mathematical Properties

> [!important] Linearity
> For differentiable vector fields $\mathbf{F}$ and $\mathbf{G}$ and scalars $a,b$:
>
> $$\nabla\cdot(a\mathbf{F}+b\mathbf{G})
> =
> a\nabla\cdot\mathbf{F}
> +b\nabla\cdot\mathbf{G}$$

> [!important] Product Rule
> For a scalar field $f$ and vector field $\mathbf{F}$:
>
> $$\nabla\cdot(f\mathbf{F})
> =
> \nabla f\cdot\mathbf{F}
> +f(\nabla\cdot\mathbf{F})$$

> [!important] Divergence of a Curl
> For sufficiently smooth vector fields:
>
> $$\nabla\cdot(\nabla\times\mathbf{F})=0$$
>
> Thus, the curl of a sufficiently smooth vector field is always divergence-free.

## 4. Solenoidal Vector Fields

> [!definition] Divergence-Free Field
> A vector field is called **solenoidal** if:
>
> $$\nabla\cdot\mathbf{F}=0$$
>
> Such a field has zero local net outward flux density throughout its domain.
>
> Under appropriate regularity and topological conditions, solenoidal fields can be represented locally or globally as curls of vector potentials.

## 5. Divergence Theorem

> [!important] Integral Relationship
> The Divergence Theorem relates the divergence inside a volume to the outward flux through its closed boundary:
>
> $$\iint_{\partial V}\mathbf{F}\cdot\mathbf{n}\,dS
> =
> \iiint_V(\nabla\cdot\mathbf{F})\,dV$$
>
> This theorem converts a surface flux integral into a volume integral.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Vector Fields:** Divergence operates on vector fields.
- **Partial Derivatives:** Provides the derivatives used in its formulation.
- **Multiple Integrals:** Supports the volume integral appearing in the Divergence Theorem.

### Downstream Knowledge
- **Divergence Theorem:** Connects divergence with outward surface flux.
- **Solenoidal Vector Fields:** Studies fields with zero divergence.
- **Differential Equations:** Uses divergence in conservation equations and field equations.

## 7. References

> [!bibliography] Recommended References
> - Marsden, J. E., and Tromba, A. J. *Vector Calculus*. 6th edition, 2012.
> - Schey, H. M. *Div, Grad, Curl, and All That: An Informal Text on Vector Calculus*. 4th edition, 2005.