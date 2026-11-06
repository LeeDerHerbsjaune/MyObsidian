---
type: technical-term
title: "Fractional Integral Equations"
aliases:
  - Fractional-Order Integral Equations
field:
  - Mathematics
subfield:
  - Fractional Calculus
  - Integral Equations
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - fractional-calculus
  - integral-equations
sources:
  - "Kilbas, Srivastava, and Trujillo (2006), Theory and Applications of Fractional Differential Equations"
  - "Samko, Kilbas, and Marichev (1993), Fractional Integrals and Derivatives"
related: []
projects: []
---

> [!abstract] Definition
> **Fractional integral equations** are integral equations involving fractional integral operators or kernels associated with fractional calculus.
>
> They generalize classical integral equations by incorporating non-integer-order integration and its characteristic power-law kernels.

> [!important] General Form
> A fractional integral equation may be represented as
>
> $$
> y(x)=g(x)+\lambda I_{a+}^{\alpha}y(x)
> $$
>
> where:
> - $y(x)$ is the unknown function.
> - $g(x)$ is a prescribed function.
> - $\lambda$ is a parameter.
> - $I_{a+}^{\alpha}$ is a fractional integral operator.
> - $\alpha>0$ is the fractional order.
>
> More general formulations can involve nonlinear functions of the unknown solution.

> [!note] Volterra-Type Fractional Integral Equation
> A common linear Volterra-type equation is
>
> $$
> y(x)=g(x)+
> \frac{\lambda}{\Gamma(\alpha)}
> \int_a^x
> (x-t)^{\alpha-1}y(t)\,dt
> $$
>
> The kernel
>
> $$
> K_\alpha(x,t)
> =
> \frac{(x-t)^{\alpha-1}}{\Gamma(\alpha)}
> $$
>
> is associated with the Riemann–Liouville fractional integral.
>
> The integration range depends on the evaluation point $x$, giving the equation its Volterra structure.

> [!note] Fredholm-Type Formulations
> A fractional integral equation can also have a fixed integration interval:
>
> $$
> y(x)=g(x)+
> \lambda\int_a^b K_\alpha(x,t)y(t)\,dt
> $$
>
> Here, the fractional character is encoded in the kernel $K_\alpha$ or in a fractional integral operator defined over the domain.
>
> Not every equation with a singular kernel is automatically a fractional integral equation; the operator structure must be specified.

> [!important] Relation to Fractional Differential Equations
> Many fractional differential equations can be transformed into fractional integral equations.
>
> For example, for a Caputo initial-value problem
>
> $$
> {}^C D_{a+}^{\alpha}y(x)=f(x,y(x)),
> \qquad 0<\alpha<1
> $$
>
> with $y(a)=y_a$, an equivalent integral formulation under suitable assumptions is
>
> $$
> y(x)=y_a+
> \frac{1}{\Gamma(\alpha)}
> \int_a^x
> (x-t)^{\alpha-1}f(t,y(t))\,dt
> $$
>
> This equivalence connects differential and integral formulations of fractional-order problems.

> [!important] Analytical Methods
> Common methods include:
> - Successive approximations.
> - Fixed-point theorems.
> - Resolvent-kernel methods.
> - Laplace transform methods.
> - Series solutions.
> - Fractional integral operator techniques.
>
> Existence and uniqueness results depend on the kernel, function space, and assumptions on the nonlinear terms.

> [!note] Numerical Methods
> Numerical approaches include:
> - Product integration methods.
> - Quadrature methods for weakly singular kernels.
> - Collocation methods.
> - Spectral methods.
> - Discretization of the associated fractional differential equation.
>
> The weak singularity of many fractional kernels must be considered when designing numerical integration schemes.

> [!warning] Limitations
> - The kernel may be weakly singular near the integration boundary.
> - Existence and uniqueness require suitable assumptions.
> - The equivalence with a fractional differential equation depends on the derivative definition and initial conditions.
> - Numerical methods must account for kernel behavior and possible solution singularities.

> [!link] Knowledge Relationships
> **Foundation Knowledge**
> - Fractional Integrals — supplies the operators used in fractional integral equations.
> - Integral Equations — provides the general theory of integral equations.
> - Real Analysis — supports convergence and integrability arguments.
> - Functional Analysis — provides operator-theoretic existence and uniqueness methods.
>
> **Downstream Knowledge**
> - Fractional Differential Equations — can be reformulated as fractional integral equations.
> - Numerical Methods for Fractional Integral Equations — develops computational solution methods.
> - Nonlinear Fractional Integral Equations — studies nonlinear operator formulations.
> - Fractional PDEs — related multidimensional problems can also admit integral formulations.

> [!quote] References
> - Kilbas, A. A., Srivastava, H. M., and Trujillo, J. J. (2006). *Theory and Applications of Fractional Differential Equations*.
> - Samko, S. G., Kilbas, A. A., and Marichev, O. I. (1993). *Fractional Integrals and Derivatives: Theory and Applications*.