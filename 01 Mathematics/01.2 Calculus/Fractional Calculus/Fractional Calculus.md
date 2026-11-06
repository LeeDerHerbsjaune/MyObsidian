---
type: technical-term
title: Fractional Calculus
aliases:
  - Calculus of Fractional Order
abbreviation: ""
field:
  - Mathematics
subfield:
  - Fractional Calculus
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - calculus
  - fractional-calculus
sources: []
related:
  - "[[Fractional Integrals]]"
  - "[[Fractional Derivatives]]"
  - "[[Riemann–Liouville Derivative]]"
  - "[[Caputo Derivative]]"
  - "[[Grünwald–Letnikov Derivative]]"
  - "[[Riesz Fractional Derivative]]"
  - "[[Properties of Fractional Operators]]"
  - "[[Fractional Integrals and Derivatives of Several Variables]]"
  - "[[Fractional Differential Equations]]"
  - "[[Fractional PDEs]]"
  - "[[Fractional Integral Equations]]"
projects: []
---

> [!abstract] Definition
> **Fractional Calculus** is the mathematical theory of differentiation and integration of arbitrary real or complex order.
>
> It generalizes classical integer-order calculus by defining integral and differential operators whose orders are not restricted to positive integers.
>
> Fractional operators are commonly nonlocal: evaluating an operator at a point may require information about the function over an interval or a larger domain.

## 2. Scope and Mathematical Foundations

> [!important] Central Concept
> Classical calculus studies integer-order derivatives and integrals:
>
> $$\frac{d^n f}{dx^n},
> \qquad
> \int f(x)\,dx$$
>
> Fractional calculus extends this framework to operators of order $\alpha$, where $\alpha$ may be fractional:
>
> $$D^\alpha f(x)$$
>
> $$I^\alpha f(x)$$
>
> Here:
> - $D^\alpha$ denotes a fractional differentiation operator.
> - $I^\alpha$ denotes a fractional integration operator.
> - $\alpha$ denotes the operator order.
>
> Different definitions of fractional operators produce different mathematical properties and are appropriate for different classes of problems.

## 3. Fractional Integrals

> [!important] Riemann–Liouville Fractional Integral
> One of the fundamental definitions is the left-sided Riemann–Liouville fractional integral:
>
> $$\boxed{
> (I_{a+}^{\alpha}f)(x)
> =
> \frac{1}{\Gamma(\alpha)}
> \int_a^x
> (x-t)^{\alpha-1}f(t)\,dt
> }$$
>
> where:
> - $\alpha>0$ is the fractional order.
> - $\Gamma(\alpha)$ is the Gamma function.
> - $a$ is the lower terminal of integration.
>
> For $\alpha=1$, this reduces to ordinary integration:
>
> $$I_{a+}^{1}f(x)=\int_a^x f(t)\,dt$$

> [!note] Interpretation
> Fractional integration generalizes repeated integration through an integral kernel involving a power-law weighting function.
>
> The value at $x$ depends on the function over the interval $[a,x]$.

## 4. Fractional Derivatives

> [!important] General Concept
> A fractional derivative generalizes differentiation to non-integer orders.
>
> Unlike ordinary differentiation, there is no single universally accepted definition. Different definitions encode different treatments of initial conditions, boundary conditions, and nonlocal dependence.

> [!note] Riemann–Liouville Derivative
> For $\alpha>0$, let $n=\lceil\alpha\rceil$. The left-sided Riemann–Liouville derivative is:
>
> $$\boxed{
> (D_{a+}^{\alpha}f)(x)
> =
> \frac{d^n}{dx^n}
> \left[
> \frac{1}{\Gamma(n-\alpha)}
> \int_a^x
> (x-t)^{n-\alpha-1}f(t)\,dt
> \right]
> }$$
>
> for non-integer $\alpha$ under suitable integrability and regularity assumptions.
>
> It is defined by applying an integer-order derivative to a fractional integral.

> [!note] Caputo Derivative
> The Caputo derivative is defined by applying fractional integration to an integer-order derivative:
>
> $$\boxed{
> ({}^{C}D_{a+}^{\alpha}f)(x)
> =
> \frac{1}{\Gamma(n-\alpha)}
> \int_a^x
> (x-t)^{n-\alpha-1}f^{(n)}(t)\,dt
> }$$
>
> where $n=\lceil\alpha\rceil$ and $n-1<\alpha<n$.
>
> A significant distinction is that Caputo derivatives annihilate constants for positive non-integer orders under the usual assumptions.

> [!note] Grünwald–Letnikov Derivative
> The Grünwald–Letnikov derivative is defined through a limiting fractional finite-difference expression:
>
> $$\boxed{
> D_{a+}^{\alpha}f(x)
> =
> \lim_{h\to0^+}
> \frac{1}{h^\alpha}
> \sum_{k=0}^{\lfloor(x-a)/h\rfloor}
> (-1)^k
> \binom{\alpha}{k}
> f(x-kh)
> }$$
>
> when the limit exists.
>
> This definition provides a connection between fractional differentiation and generalized finite differences.

## 5. Fundamental Mathematical Properties

> [!important] Nonlocality
> Fractional operators generally depend on function values over an interval or domain.
>
> For example, a left-sided fractional derivative with lower terminal $a$ can depend on the function throughout $[a,x]$.
>
> This differs from the local behavior of classical derivatives.

> [!important] Semigroup Property
> Fractional integrals satisfy a semigroup property under suitable conditions:
>
> $$I_{a+}^{\alpha}I_{a+}^{\beta}f
> =
> I_{a+}^{\alpha+\beta}f$$
>
> However, fractional derivatives do not generally satisfy the analogous composition rule without additional assumptions and correction terms.

> [!note] Integer-Order Consistency
> Appropriate fractional operators recover classical calculus at integer orders.
>
> For example:
>
> $$I_{a+}^{1}f(x)=\int_a^x f(t)\,dt$$
>
> The exact limiting and integer-order conventions depend on the operator definition.

> [!note] Gamma Function
> The Gamma function generalizes the factorial:
>
> $$\Gamma(n+1)=n!$$
>
> For positive real $z$:
>
> $$\Gamma(z)=\int_0^\infty t^{z-1}e^{-t}\,dt$$
>
> It appears naturally in fractional integral and derivative definitions.

## 6. Fractional Differential Equations

> [!important] Definition
> A **fractional differential equation** is a differential equation involving one or more fractional-order derivatives.
>
> A general form is:
>
> $$F(x,y,D^\alpha y,D^\beta y,\ldots)=0$$
>
> Such equations extend ordinary and partial differential equations by incorporating fractional-order operators.
>
> Their solutions and initial conditions depend on the chosen derivative definition.

> [!note] Initial Conditions
> Initial conditions for fractional differential equations are not always identical to those used in integer-order differential equations.
>
> For example, Caputo formulations commonly use ordinary integer-order initial values, whereas Riemann–Liouville formulations can involve fractional integral or derivative initial data.

## 7. Generalizations

> [!note] Fractional Operators in Several Variables
> Fractional calculus can be extended to functions of multiple independent variables.
>
> Examples include:
> - Partial fractional derivatives.
> - Multidimensional fractional integrals.
> - Fractional Laplacian operators.
>
> The precise definitions depend on the geometry of the domain, boundary conditions, and the selected operator.

> [!note] Fractional Laplacian
> A widely used multidimensional fractional operator is the fractional Laplacian:
>
> $$(-\Delta)^s u$$
>
> where $0<s<1$.
>
> On $\mathbb{R}^n$, it can be defined through the Fourier transform by:
>
> $$\mathcal{F}[(-\Delta)^s u](\boldsymbol{\xi})
> =
> |\boldsymbol{\xi}|^{2s}
> \widehat{u}(\boldsymbol{\xi})$$
>
> This operator is generally nonlocal and has important mathematical connections to fractional-order differential equations.

## 8. Limitations and Mathematical Considerations

> [!warning] Important Distinctions
> - There is no unique definition of fractional differentiation.
> - Different definitions can produce different initial-value formulations and mathematical properties.
> - Fractional operators are generally nonlocal.
> - Semigroup and composition properties require careful assumptions.
> - Existence, uniqueness, and regularity of solutions depend on the operator and function space.
> - The choice of lower terminal, boundary conditions, and operator definition is part of the mathematical model.

## 9. Knowledge Relationships

> [!note] Foundation Knowledge
> **Essential**
> - Differential Calculus — provides the integer-order differentiation framework.
> - Integral Calculus — provides the integration framework generalized by fractional operators.
>
> **Relevant**
> - Real Analysis — supports rigorous definitions of integrals, derivatives, and convergence.
> - Infinite Sequences and Series — supports representations involving power series and special functions.
> - Complex Analysis — relevant to complex-order operators and analytic methods.
> - Special Functions — the Gamma and Mittag-Leffler functions play important roles in fractional calculus.

> [!note] Downstream Knowledge
> **Relevant**
> - Fractional Differential Equations — develops equations involving fractional derivatives.
> - Integral Transforms — provides methods for analyzing fractional operators and equations.
> - Fractional Integral Equations — studies equations involving fractional integral operators.
>
> **Advanced**
> - Fractional PDEs — extends fractional differential equations to multidimensional domains.
> - Fractional Optimal Control — incorporates fractional dynamics into variational and control problems.
> - Fractional Sobolev Spaces — develops function spaces associated with fractional-order regularity.
> - Nonlocal Analysis — provides a broader mathematical framework for nonlocal operators.

## 10. Further Development

> [!todo] Recommended Independent Notes
> - Fractional-Order Operators
> - Fractional Integrals
> - Fractional Derivatives
> - Riemann–Liouville Fractional Integral
> - Riemann–Liouville Derivative
> - Caputo Derivative
> - Grünwald–Letnikov Derivative
> - Riesz Fractional Derivative
> - Properties of Fractional Operators
> - Fractional Differential Equations
> - Fractional Calculus in Several Variables
>
> These are proposed note boundaries. Some closely related definitions may later be grouped if their individual scope proves too narrow.

## 11. References

> [!note] Foundational References
> - Oldham, K. B., and Spanier, J. (1974). *The Fractional Calculus: Theory and Applications of Differentiation and Integration to Arbitrary Order*. Academic Press.
> - Samko, S. G., Kilbas, A. A., and Marichev, O. I. (1993). *Fractional Integrals and Derivatives: Theory and Applications*. Gordon and Breach Science Publishers.
> - Podlubny, I. (1999). *Fractional Differential Equations*. Academic Press.
> - Kilbas, A. A., Srivastava, H. M., and Trujillo, J. J. (2006). *Theory and Applications of Fractional Differential Equations*. Elsevier.