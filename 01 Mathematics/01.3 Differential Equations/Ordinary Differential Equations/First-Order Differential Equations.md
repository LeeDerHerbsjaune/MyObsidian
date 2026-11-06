---
type: technical-term
title: "First-Order Ordinary Differential Equations"
aliases:
  - First-Order ODEs
  - First-Order Ordinary Differential Equations
abbreviation: First-Order ODE
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
> A First-Order Ordinary Differential Equation (First-Order ODE) is an ordinary differential equation in which the highest-order derivative of the unknown function is the first derivative.
>
> It describes a relationship between an unknown function of one independent variable and its first derivative.

## 1. Mathematical Representation

> [!abstract] General Implicit Form
> A first-order ODE can be represented as:
>
> $$F(x,y,y')=0$$
>
> where:
> - $x$ is the independent variable.
> - $y=y(x)$ is the unknown dependent function.
> - $y'=\frac{dy}{dx}$ is the first derivative.
> - $F$ defines the relationship between the independent variable, unknown function, and its derivative.

> [!abstract] Explicit Form
> When the equation can be solved for the first derivative, it takes the form:
>
> $$\frac{dy}{dx}=f(x,y)$$
>
> This is the standard explicit representation of a first-order ODE.

## 2. Classification

> [!abstract] Linear First-Order ODEs
> A first-order linear ODE has the standard form:
>
> $$\frac{dy}{dx}+P(x)y=Q(x)$$
>
> where $P(x)$ and $Q(x)$ are known functions.
>
> - Homogeneous Linear First-Order ODEs
> - Nonhomogeneous Linear First-Order ODEs

> [!abstract] Nonlinear First-Order ODEs
> First-order ODEs that cannot be expressed in linear form.
>
> Important classes include:
> - Separable Differential Equations
> - Exact Differential Equations
> - Bernoulli Differential Equations
> - Homogeneous Differential Equations
> - Riccati Differential Equations
> - Autonomous Differential Equations

> [!note] Classification Clarification
> The term homogeneous has different meanings in different classifications:
> - Homogeneous linear ODE: $y'+P(x)y=0$.
> - Homogeneous first-order ODE: commonly expressed as $y'=F(y/x)$.
>
> These are distinct mathematical concepts.

## 3. Solution Methods

> [!abstract] Fundamental Analytical Methods
> - Separation of Variables
> - Integrating Factor Method
> - Substitution Methods
> - Exact Equation Method
> - Bernoulli Equation Method
> - Homogeneous Equation Method
> - Riccati Equation Method

> [!note] Integrating Factor
> For a linear first-order ODE:
>
> $$y'+P(x)y=Q(x)$$
>
> The integrating factor is:
>
> $$\mu(x)=e^{\int P(x)\,dx}$$
>
> Multiplying the equation by $\mu(x)$ gives:
>
> $$\frac{d}{dx}[\mu(x)y]=\mu(x)Q(x)$$

## 4. Initial Value Problems

> [!abstract] Initial Value Problem (IVP)
> A first-order ODE accompanied by an initial condition is called an initial value problem.
>
> $$\frac{dy}{dx}=f(x,y)$$
>
> $$y(x_0)=y_0$$
>
> where $(x_0,y_0)$ specifies the initial condition.
>
> The objective is to determine a solution satisfying both the differential equation and the initial condition.

## 5. Fundamental Theoretical Properties

> [!important] Existence and Uniqueness
> For an initial value problem:
>
> $$y'=f(x,y), \qquad y(x_0)=y_0$$
>
> If $f$ is continuous in a neighborhood of $(x_0,y_0)$, a local solution exists.
>
> If $f$ additionally satisfies a local Lipschitz condition with respect to $y$, the local solution is unique.

> [!note] Other Important Properties
> - Local Existence of Solutions
> - Uniqueness of Solutions
> - Maximal Interval of Existence
> - Continuous Dependence on Initial Conditions
> - Equilibrium Solutions
> - Implicit and Explicit Solutions

## 6. Special Concepts

> [!abstract] Equilibrium Solutions
> An equilibrium solution is a constant solution $y(x)=y^*$ satisfying:
>
> $$f(x,y^*)=0$$
>
> For autonomous equations $y'=f(y)$, equilibrium values satisfy:
>
> $$f(y^*)=0$$

> [!note] General and Particular Solutions
> - General Solution: A family of solutions containing an arbitrary constant, where applicable.
> - Particular Solution: A solution obtained by specifying an additional condition, such as an initial condition.
> - Singular Solution: A solution that cannot be obtained from the general solution family in certain classical formulations.

## 7. Knowledge Relationships

### Foundation Knowledge

- **Differential Equations:** Establishes the general mathematical framework.
- **Calculus:** Provides differentiation and integration.
- **Integration Techniques:** Supports analytical solution methods.
- **Real Analysis:** Provides rigorous foundations for existence, uniqueness, and convergence.

### Downstream Knowledge

- **Higher-Order Ordinary Differential Equations:** Extends differential equations to higher derivative orders.
- **Systems of Ordinary Differential Equations:** Extends scalar ODEs to coupled systems of unknown functions.
- **Qualitative Theory of Differential Equations:** Studies solution behavior, equilibrium points, and stability.
- **Numerical Methods for ODEs:** Develops numerical approximations for first-order initial value problems.

## 8. References

- Boyce, W. E., DiPrima, R. C., and Meade, D. B. *Elementary Differential Equations and Boundary Value Problems*. Wiley.
- Coddington, E. A. *An Introduction to Ordinary Differential Equations*. Dover Publications, 1989.
- Tenenbaum, M., and Pollard, H. *Ordinary Differential Equations*. Dover Publications, 1985.