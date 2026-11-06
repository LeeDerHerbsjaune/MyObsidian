---
type: technical-term
title: "Fractional Differential Equations"
aliases:
  - Fractional-Order Differential Equations
abbreviation: FDEs
field:
  - Mathematics
subfield:
  - Fractional Calculus
  - Differential Equations
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - fractional-calculus
  - differential-equations
sources:
  - "Podlubny (1999), Fractional Differential Equations"
  - "Diethelm (2010), The Analysis of Fractional Differential Equations"
related: []
projects: []
---

> [!abstract] Definition
> **Fractional differential equations (FDEs)** are differential equations involving derivatives of non-integer order.
>
> They extend ordinary and partial differential equations by replacing or supplementing integer-order derivatives with fractional-order operators.

> [!important] General Form
> A general fractional differential equation can be represented abstractly as
>
> $$
> F\left(t,y(t),D^{\alpha_1}y(t),\ldots,
> D^{\alpha_m}y(t)\right)=0
> $$
>
> where:
> - $y(t)$ is the unknown function.
> - $D^{\alpha_i}$ denotes a fractional derivative of order $\alpha_i$.
> - $F$ specifies the relationship between the unknown function and its fractional derivatives.
>
> The exact equation depends on the selected derivative definition.

> [!note] Linear Fractional Differential Equation
> A linear fractional differential equation may take the form
>
> $$
> \sum_{k=0}^{m}a_k(t)D^{\alpha_k}y(t)=g(t)
> $$
>
> where $a_k(t)$ are coefficient functions and $g(t)$ is a prescribed forcing function.

> [!important] Initial-Value Problems
> For a Caputo derivative of order $n-1<\alpha\leq n$, a typical initial-value problem specifies
>
> $$
> y(0),y'(0),\ldots,y^{(n-1)}(0)
> $$
>
> The required number and type of initial conditions depend on the derivative order and formulation.
>
> For Riemann–Liouville derivatives, the natural initial data generally involve fractional integral or derivative quantities instead.

> [!important] Integral Formulation
> Fractional differential equations can often be converted into fractional integral equations.
>
> For example, consider
>
> $$
> {}^C D_{0+}^{\alpha}y(t)=f(t,y(t)),
> \qquad 0<\alpha<1
> $$
>
> Under suitable assumptions, this is equivalent to
>
> $$
> y(t)=y(0)+
> \frac{1}{\Gamma(\alpha)}
> \int_0^t
> (t-\tau)^{\alpha-1}
> f(\tau,y(\tau))\,d\tau
> $$
>
> This integral representation is important in existence theory and numerical analysis.

> [!note] Analytical Methods
> Common analytical approaches include:
> - Laplace transform methods.
> - Integral-equation formulations.
> - Series solutions.
> - Mittag-Leffler function representations.
> - Fixed-point methods.
> - Existence and uniqueness theorems.
>
> The suitability of each method depends on the equation, derivative definition, and initial conditions.

> [!note] Numerical Methods
> Common numerical approaches include:
> - Grünwald–Letnikov discretization.
> - L1 and related finite-difference schemes.
> - Predictor–corrector methods.
> - Convolution quadrature.
> - Spectral and finite-element methods for suitable problems.
>
> Because fractional derivatives are generally nonlocal, numerical methods often require information from many previous time steps.

> [!warning] Important Considerations
> - The derivative definition must be stated explicitly.
> - Initial conditions must be compatible with that definition.
> - Existence and uniqueness require appropriate assumptions.
> - Numerical schemes must account for nonlocal history dependence.
> - Fractional-order models do not automatically provide a better description than integer-order models; their suitability must be justified by the problem.

> [!link] Knowledge Relationships
> **Foundation Knowledge**
> - Fractional Derivatives — supplies the operators defining FDEs.
> - Fractional Integrals — supports their integral formulations.
> - Ordinary Differential Equations — provides the classical equation framework.
> - Real Analysis — supports existence, convergence, and regularity arguments.
> - Integral Equations — provides the theory behind equivalent integral formulations.
>
> **Downstream Knowledge**
> - Fractional PDEs — extends fractional differential equations to multiple independent variables.
> - Numerical Methods for Fractional Differential Equations — develops computational solution methods.
> - Fractional Optimal Control — studies optimization problems governed by fractional dynamics.
> - Stability Theory for Fractional Systems — studies the stability of fractional-order dynamical systems.

> [!quote] References
> - Podlubny, I. (1999). *Fractional Differential Equations*.
> - Diethelm, K. (2010). *The Analysis of Fractional Differential Equations*.
> - Kilbas, A. A., Srivastava, H. M., and Trujillo, J. J. (2006). *Theory and Applications of Fractional Differential Equations*.