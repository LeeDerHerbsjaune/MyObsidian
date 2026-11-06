---
type: technical-term
title: "Multiple Independent Variables"
aliases:
  - Variational Problems with Multiple Independent Variables
  - Field Variational Problems
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus of Variations
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - partial-differential-equations
sources: []
related: []
projects: []
---

> [!abstract] Definition
> **Variational problems with multiple independent variables** involve functionals defined over fields whose values depend on two or more independent coordinates.
>
> They generalize classical one-dimensional variational problems from curves and functions of one variable to fields defined over multidimensional domains.

## 2. Mathematical Formulation

> [!important] Scalar Field
> Let $\Omega\subseteq\mathbb{R}^n$ be a domain and let:
>
> $$u:\Omega\rightarrow\mathbb{R}$$
>
> be a scalar field.
>
> A common variational functional is:
>
> $$J[u]=
> \int_\Omega
> L(\mathbf{x},u,\nabla u)\,d\mathbf{x}$$
>
> where:
> - $\mathbf{x}=(x_1,\ldots,x_n)$ represents the independent variables.
> - $u$ is the unknown field.
> - $\nabla u$ is its gradient.
> - $L$ is the Lagrangian density.

## 3. First Variation

> [!note] Field Variation
> Perturb the field using:
>
> $$u_\varepsilon(\mathbf{x})
> =
> u(\mathbf{x})+\varepsilon\eta(\mathbf{x})$$
>
> For fixed boundary values, the variation satisfies:
>
> $$\eta|_{\partial\Omega}=0$$
>
> The first variation is:
>
> $$\delta J[u;\eta]
> =
> \int_\Omega
> \left(
> \frac{\partial L}{\partial u}\eta
> +
> \frac{\partial L}{\partial(\nabla u)}
> \cdot\nabla\eta
> \right)d\mathbf{x}$$

## 4. Generalized Euler–Lagrange Equation

> [!important] Field Euler–Lagrange Equation
> Applying the multidimensional integration-by-parts identity and imposing stationarity yields:
>
> $$\boxed{
> \frac{\partial L}{\partial u}
> -
> \nabla\cdot
> \left(
> \frac{\partial L}{\partial(\nabla u)}
> \right)=0
> }$$
>
> This is a partial differential equation for the stationary field $u$.

## 5. Multiple Field Components

> [!note] Vector-Valued Fields
> If the unknown is a collection of fields:
>
> $$\mathbf{u}=(u_1,\ldots,u_m)$$
>
> and:
>
> $$J[\mathbf{u}]
> =
> \int_\Omega
> L(\mathbf{x},\mathbf{u},\nabla\mathbf{u})\,d\mathbf{x}$$
>
> then each component satisfies:
>
> $$\frac{\partial L}{\partial u_i}
> -
> \nabla\cdot
> \left(
> \frac{\partial L}{\partial(\nabla u_i)}
> \right)=0$$
>
> for $i=1,\ldots,m$.

## 6. Interpretation and Scope

> [!note] From Curves to Fields
> In one independent variable, the unknown is a function such as $y(x)$.
>
> With multiple independent variables, the unknown becomes a field such as $u(x_1,x_2)$ or $u(x_1,x_2,x_3)$.
>
> The resulting Euler–Lagrange equations are generally PDEs rather than ordinary differential equations.

> [!warning] Important Distinction
> Multiple independent variables do not necessarily imply multiple dependent variables.
>
> A problem may involve:
> - One scalar field over a multidimensional domain.
> - Several scalar fields over the same domain.
>
> These are separate dimensions of generalization.

## 7. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Multivariable Calculus:** Provides partial derivatives, gradients, and multidimensional integration.
> - **Vector Calculus:** Provides divergence and multidimensional integration identities.
> - **Functionals:** Define optimization over fields.
> - **Variations:** Define admissible perturbations of fields.
>
> [!note] Downstream Knowledge
> - **Partial Differential Equations:** Field Euler–Lagrange equations are PDEs.
> - **Field Theory:** Uses variational principles to formulate field equations.
> - **Geometric Calculus of Variations:** Studies variational problems on geometric domains and manifolds.
> - **Functional Analysis:** Provides rigorous spaces and methods for field-based variational problems.

## 8. References

> [!note] References
> - Gelfand, I. M., and Fomin, S. V. (1963). *Calculus of Variations*. Prentice-Hall.
> - Giaquinta, M., and Hildebrandt, S. (1996). *Calculus of Variations I: The Lagrangian Formalism*. Springer.