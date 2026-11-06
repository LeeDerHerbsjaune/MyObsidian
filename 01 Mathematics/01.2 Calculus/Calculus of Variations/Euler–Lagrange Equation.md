---
type: technical-term
title: "Euler–Lagrange Equation"
aliases:
  - Euler-Lagrange Differential Equation
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
  - differential-equations
sources: []
related: []
projects: []
---

> [!abstract] Definition
> The **Euler–Lagrange equation** is the fundamental differential equation satisfied by sufficiently regular stationary functions of a classical integral variational problem.
>
> It is obtained by setting the first variation of the functional equal to zero for every admissible variation.

## 2. Classical Formulation

> [!important] Euler–Lagrange Equation
> Consider the functional:
>
> $$J[y]=\int_a^b L(x,y,y')\,dx$$
>
> A stationary function satisfies:
>
> $$\boxed{
> \frac{\partial L}{\partial y}
> -
> \frac{d}{dx}
> \left(
> \frac{\partial L}{\partial y'}
> \right)=0
> }$$
>
> where $L(x,y,y')$ is the Lagrangian.

## 3. Derivation

> [!note] Derivation from the First Variation
> The first variation is:
>
> $$\delta J=
> \int_a^b
> \left(
> L_y\eta+L_{y'}\eta'
> \right)dx$$
>
> Integration by parts gives:
>
> $$\delta J=
> [L_{y'}\eta]_a^b+
> \int_a^b
> \left(L_y-\frac{d}{dx}L_{y'}\right)\eta\,dx$$
>
> For fixed endpoints, $\eta(a)=\eta(b)=0$. Thus:
>
> $$\delta J=
> \int_a^b
> \left(L_y-\frac{d}{dx}L_{y'}\right)\eta\,dx$$
>
> Since this expression must vanish for all admissible $\eta$, the fundamental lemma of the calculus of variations yields the Euler–Lagrange equation.

## 4. Example

> [!example] Shortest Curve Between Two Fixed Points
> Consider:
>
> $$J[y]=\int_a^b\sqrt{1+(y')^2}\,dx$$
>
> The Lagrangian is:
>
> $$L=\sqrt{1+(y')^2}$$
>
> Since $L_y=0$ and:
>
> $$L_{y'}=\frac{y'}{\sqrt{1+(y')^2}}$$
>
> the Euler–Lagrange equation becomes:
>
> $$\frac{d}{dx}
> \left(
> \frac{y'}{\sqrt{1+(y')^2}}
> \right)=0$$
>
> Therefore $y'$ is constant, and the stationary curves are straight lines.

## 5. Generalizations

> [!note] Higher-Order Derivatives
> If the Lagrangian depends on derivatives up to order $n$:
>
> $$L=L(x,y,y',\ldots,y^{(n)})$$
>
> then:
>
> $$\boxed{
> \sum_{k=0}^{n}
> (-1)^k
> \frac{d^k}{dx^k}
> \left(
> \frac{\partial L}{\partial y^{(k)}}
> \right)=0
> }$$

> [!note] Multiple Dependent Variables
> For $y_1,\ldots,y_m$:
>
> $$\frac{\partial L}{\partial y_i}
> -
> \frac{d}{dx}
> \left(
> \frac{\partial L}{\partial y_i'}
> \right)=0,
> \quad i=1,\ldots,m$$

> [!note] Multiple Independent Variables
> For a field $u(\mathbf{x})$:
>
> $$\frac{\partial L}{\partial u}
> -
> \nabla\cdot
> \left(
> \frac{\partial L}{\partial(\nabla u)}
> \right)=0$$

## 6. Limitations

> [!warning] Necessary, Not Sufficient
> - Satisfying the Euler–Lagrange equation establishes a stationary candidate under appropriate assumptions.
> - It does not guarantee a local or global minimum.
> - The existence of a solution is a separate mathematical question.
> - Boundary conditions and admissibility requirements are essential parts of the problem.

## 7. Knowledge Relationships

> [!note] Foundation Knowledge
> - **First Variation:** Provides the stationarity condition.
> - **Variations:** Define admissible perturbations.
> - **Integration by Parts:** Enables the derivation.
> - **Fundamental Lemma of the Calculus of Variations:** Converts the integral condition into a pointwise differential equation.
>
> [!note] Downstream Knowledge
> - **Boundary Conditions:** Complete the variational boundary-value problem.
> - **Second Variation:** Provides second-order information about stationary solutions.
> - **Partial Differential Equations:** Generalized Euler–Lagrange equations produce PDEs.
> - **Optimal Control Theory:** Uses related variational principles.

## 8. References

> [!note] References
> - Gelfand, I. M., and Fomin, S. V. (1963). *Calculus of Variations*. Prentice-Hall.
> - Liberzon, D. (2012). *Calculus of Variations and Optimal Control Theory*. Princeton University Press.