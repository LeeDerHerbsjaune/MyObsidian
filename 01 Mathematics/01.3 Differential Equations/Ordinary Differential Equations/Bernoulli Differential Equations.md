---
type: technical-term
title: "Bernoulli Differential Equations"
aliases:
  - Bernoulli Equations
  - Bernoulli ODEs
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
> A Bernoulli Differential Equation is a first-order nonlinear ordinary differential equation that can be transformed into a linear first-order differential equation through a suitable substitution.
>
> It is named after Jacob Bernoulli and represents an important class of nonlinear ODEs with a systematic analytical solution method.

## 1. Mathematical Representation

> [!abstract] Standard Form
>
> $$\frac{dy}{dx}+P(x)y=Q(x)y^n$$
>
> where:
> - $P(x)$ and $Q(x)$ are known functions.
> - $y=y(x)$ is the unknown function.
> - $n$ is a real constant.
> - $n\neq 0,1$ for the genuinely nonlinear Bernoulli case.

## 2. Identification Conditions

> [!important] Recognition
> An equation is a Bernoulli equation if it can be rearranged into:
>
> $$y'+P(x)y=Q(x)y^n$$
>
> Its defining characteristic is the nonlinear power term $y^n$ combined with a linear term in $y$.

## 3. Solution Method

> [!note] Bernoulli Substitution
> Divide the equation by $y^n$:
>
> $$y^{-n}y'+P(x)y^{1-n}=Q(x)$$
>
> Introduce the substitution:
>
> $$v=y^{1-n}$$
>
> Therefore:
>
> $$v'=(1-n)y^{-n}y'$$
>
> Multiplying the original transformed equation by $1-n$ produces:
>
> $$v'+(1-n)P(x)v=(1-n)Q(x)$$
>
> This is a linear first-order ODE in $v$.
>
> After solving for $v$, recover the original function:
>
> $$y=v^{\frac{1}{1-n}}$$

## 4. Properties

- Bernoulli equations are generally nonlinear when $n\neq 0,1$.
- A power substitution transforms them into linear first-order ODEs.
- The transformed equation can be solved using an integrating factor.
- The transformation requires care at points where $y=0$.
- Solutions excluded by division or substitution must be checked separately.

## 5. Examples

> [!example] Example
>
> $$y'+y=xy^2$$
>
> Identify:
>
> $$P(x)=1,\qquad Q(x)=x,\qquad n=2$$
>
> Apply:
>
> $$v=y^{1-2}=\frac{1}{y}$$
>
> The transformed equation becomes:
>
> $$v'-v=-x$$
>
> Its integrating factor is:
>
> $$\mu(x)=e^{-x}$$
>
> Therefore:
>
> $$v=1+Ce^x$$
>
> Recovering $y$:
>
> $$y=\frac{1}{1+Ce^x}$$
>
> The solution $y=0$ must also be considered separately.

## 6. Knowledge Relationships

### Foundation Knowledge

- First-Order Ordinary Differential Equations — provides the general equation framework.
- Linear First-Order ODEs — provides the solution method for the transformed equation.
- Differential Calculus — supports differentiation and substitutions.
- Integral Calculus — supports integration factor techniques.

### Downstream Knowledge

- Nonlinear Differential Equations — develops broader nonlinear equation theory.
- Integrating Factor Method — provides the principal solution technique after transformation.
- Riccati Differential Equations — provides a related but structurally different class of nonlinear first-order equations.

## 7. References

- Boyce, W. E., DiPrima, R. C., and Meade, D. B. *Elementary Differential Equations and Boundary Value Problems*. Wiley.
- Zill, D. G. *A First Course in Differential Equations with Modeling Applications*. Cengage.