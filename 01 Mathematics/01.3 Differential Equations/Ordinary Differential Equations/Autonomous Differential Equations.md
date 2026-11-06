---
type: technical-term
title: "Autonomous Differential Equations"
aliases:
  - Autonomous ODEs
  - Autonomous Equations
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

# Autonomous Differential Equations

> [!abstract] Definition
> An Autonomous Differential Equation is a differential equation in which the independent variable does not appear explicitly in the governing equation.
>
> Its rate of change depends only on the dependent variable or state variables, rather than explicitly on time or another independent variable.

## 1. Mathematical Representation

> [!abstract] Scalar First-Order Form
>
> $$\frac{dy}{dt}=f(y)$$
>
> where:
> - $t$ is the independent variable.
> - $y=y(t)$ is the dependent function.
> - $f(y)$ determines the rate of change.
>
> The corresponding nonautonomous form is:
>
> $$\frac{dy}{dt}=f(t,y)$$

> [!note] Autonomous Systems
> For a system of first-order ODEs:
>
> $$\frac{d\mathbf{x}}{dt}=\mathbf{f}(\mathbf{x})$$
>
> where $\mathbf{x}$ represents the state vector.
>
> The system is autonomous when the independent variable does not appear explicitly in $\mathbf{f}$.

## 2. Identification Conditions

> [!important] Recognition
> A scalar first-order ODE is autonomous if it can be written as:
>
> $$y'=f(y)$$
>
> The independent variable does not explicitly occur in the right-hand side.
>
> An equation is nonautonomous if it requires explicit dependence on the independent variable:
>
> $$y'=f(t,y)$$

## 3. Equilibrium Solutions

> [!abstract] Equilibrium Definition
> An equilibrium solution is a constant solution $y(t)=y^*$ satisfying:
>
> $$f(y^*)=0$$
>
> At equilibrium, the rate of change is zero:
>
> $$\frac{dy}{dt}=0$$

## 4. Solution Methods

> [!note] Separation of Variables
> When $f(y)\neq 0$, an autonomous scalar equation can be separated:
>
> $$\frac{dy}{f(y)}=dt$$
>
> Integrating:
>
> $$\int\frac{1}{f(y)}dy=t+C$$
>
> Constant equilibrium solutions must be checked separately.

> [!note] Phase-Line Analysis
> The sign of $f(y)$ determines the direction of solution evolution:
>
> - $f(y)>0$: Solutions increase.
> - $f(y)<0$: Solutions decrease.
> - $f(y)=0$: Equilibrium solutions.
>
> This provides a qualitative description of solution behavior without requiring an explicit solution.

## 5. Fundamental Properties

- The equation is invariant under translations of the independent variable, wherever the solution is defined.
- Equilibrium solutions correspond to roots of $f(y)$.
- The sign of $f(y)$ determines the direction of scalar solution trajectories.
- Solutions cannot cross an equilibrium under standard uniqueness assumptions.
- Autonomous systems can be studied through their phase-space structure.
- Time translation does not change the governing equation.

## 6. Stability of Equilibrium Solutions

> [!important] Local Stability Criterion
> Consider:
>
> $$y'=f(y)$$
>
> with an equilibrium $y^*$ satisfying $f(y^*)=0$.
>
> If $f$ is differentiable near $y^*$:
>
> - $f'(y^*)<0$: The equilibrium is locally asymptotically stable.
> - $f'(y^*)>0$: The equilibrium is unstable.
> - $f'(y^*)=0$: The linearization test is inconclusive.

## 7. Knowledge Relationships

### Foundation Knowledge

- First-Order Ordinary Differential Equations — provides the general equation framework.
- Calculus — provides differentiation and integration.
- Linear Algebra — supports the study of multidimensional autonomous systems.

### Downstream Knowledge

- Dynamical Systems — develops the mathematical study of autonomous system evolution.
- Qualitative Theory of Differential Equations — studies solution trajectories and equilibrium behavior.
- Stability Theory — analyzes the stability of equilibrium solutions.
- Phase-Line Analysis — provides qualitative analysis of scalar autonomous equations.
- Phase-Space Analysis — extends qualitative analysis to multidimensional systems.

## 8. References

- Hirsch, M. W., Smale, S., and Devaney, R. L. *Differential Equations, Dynamical Systems, and an Introduction to Chaos*. 3rd ed., Academic Press, 2012.
- Perko, L. *Differential Equations and Dynamical Systems*. 3rd ed., Springer, 2001.