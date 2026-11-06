---
type: technical-term
title: "Separable Differential Equations"
aliases:
  - Separable ODEs
  - Separable Equations
abbreviation: ""
field:
  - Mathematics
subfield:
  - Differential Equations
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - mathematics
  - differential-equations
  - ordinary-differential-equations
sources: []
related: []
projects: []
---
> [!abstract] Definition
> A Separable Differential Equation is a first-order ordinary differential equation in which the dependent and independent variables can be separated into functions of their respective variables.
>
> It can be solved by rearranging the equation so that each variable appears on a different side before integration.

## 1. Mathematical Representation

> [!abstract] Standard Form
>
> $$\frac{dy}{dx}=g(x)h(y)$$
>
> When $h(y)\neq 0$, the equation can be rearranged as:
>
> $$\frac{1}{h(y)}dy=g(x)dx$$

## 2. Identification Conditions

> [!important] Recognition
> A first-order ODE is separable if its derivative can be expressed as a product of a function of $x$ and a function of $y$:
>
> $$y'=g(x)h(y)$$
>
> Equivalently, it can be written in separated form:
>
> $$M(y)dy=N(x)dx$$

## 3. Solution Method

> [!note] Separation of Variables
> Integrating both sides gives:
>
> $$\int\frac{1}{h(y)}dy=\int g(x)dx+C$$
>
> The resulting relationship may define the solution implicitly or explicitly.

## 4. Properties

- The equation is solved using direct integration after variable separation.
- Solutions may be expressed implicitly.
- Constant solutions may be lost when dividing by $h(y)$.
- The equation may admit multiple solution branches.
- An initial condition can determine the integration constant when the solution is well-defined.

## 5. Examples

> [!example] Example
>
> $$\frac{dy}{dx}=xy$$
>
> Separating variables:
>
> $$\frac{1}{y}dy=x\,dx$$
>
> Integrating:
>
> $$\ln|y|=\frac{x^2}{2}+C$$
>
> Therefore:
>
> $$y=Ce^{x^2/2}$$
>
> where $C$ is an arbitrary constant.

## 6. Knowledge Relationships

### Foundation Knowledge

- First-Order Ordinary Differential Equations — provides the general equation framework.
- Integral Calculus — provides integration techniques.
- Function Algebra — supports variable separation and rearrangement.

### Downstream Knowledge

- Autonomous Differential Equations — many autonomous scalar equations are separable.
- Initial Value Problems — applies initial conditions to determine particular solutions.
- Numerical Methods for ODEs — provides approximations when direct integration is unavailable.

## 7. References

- Boyce, W. E., DiPrima, R. C., and Meade, D. B. *Elementary Differential Equations and Boundary Value Problems*. Wiley.
- Zill, D. G. *A First Course in Differential Equations with Modeling Applications*. Cengage.