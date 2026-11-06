---
type: technical-term
title: Differential Equations
aliases:
  - Differential Equation Theory
abbreviation: DE
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
sources: []
related:
projects: []
---
> [!abstract] Definition
> A differential equation is a mathematical equation involving an unknown function and one or more of its derivatives.
>
> Differential equations describe relationships between an unknown function, its independent variables, and the rates at which the function changes.

## 1. Core Concepts

> [!note] Fundamental Terminology
> - **Unknown Function:** The function to be determined.
> - **Independent Variable:** The variable with respect to which differentiation is performed.
> - **Dependent Variable:** The unknown function whose value depends on the independent variables.
> - **Derivative:** Represents the rate of change of the unknown function.
> - **Solution:** A function that satisfies the differential equation over a specified domain.

## 2. Mathematical Representation

> [!important] General Form
> A general differential equation can be represented as:
>
> $$F(x,y,y',y'',\ldots,y^{(n)})=0$$
>
> where:
> - $x$ is the independent variable.
> - $y$ is the unknown function.
> - $y^{(k)}$ denotes the $k$-th derivative of $y$.
> - $F$ defines the relationship among the function and its derivatives.

> [!note] Partial Differential Equation Representation
> For functions of multiple independent variables, a differential equation may involve partial derivatives:
>
> $$F(x_1,\ldots,x_m,u,\partial u,\partial^2u,\ldots)=0$$

## 3. Classification

> [!abstract] Classification by Independent Variables
> - [[Ordinary Differential Equations (ODEs)]]
> - [[Partial Differential Equations (PDEs)]]

> [!abstract] Classification by Order
>>[!hint] [[First-Order Differential Equations]]
>> - [[Separable Differential Equations]] 
>> - [[Exact Differential Equations]]
>> - [[Bernoulli Differential Equations]]
>> - [[Homogeneous First-Order Differential Equations]]
>> - [[Riccati Differential Equations]]
>> - [[Autonomous Differential Equations]]
>
>>[!hint] [[Second-Order Differential Equations]]
>>- [[Homogeneous Linear Second-Order ODEs]]
>>- [[Nonhomogeneous Linear Second-Order ODEs]]
> - Higher-Order Differential Equations

> [!abstract] Classification by Linearity
> - Linear Differential Equations
> - Nonlinear Differential Equations

> [!abstract] Other Classifications
> - Homogeneous Differential Equations
> - Nonhomogeneous Differential Equations
> - Autonomous Differential Equations
> - Nonautonomous Differential Equations

## 4. Solutions

> [!note] Types of Solutions
> - **General Solution:** A family of solutions containing arbitrary constants or functions, as appropriate.
> - **Particular Solution:** A solution obtained by specifying additional conditions.
> - **Explicit Solution:** Expresses the unknown function directly in terms of independent variables.
> - **Implicit Solution:** Represents the solution through an implicit relationship.
> - **Singular Solution:** A solution that cannot be obtained as a member of the general solution family in certain classical formulations.

## 5. Conditions and Problems

> [!important] Initial and Boundary Conditions
> Differential equations are frequently accompanied by additional conditions that specify or constrain their solutions.
>
> - Initial Value Problems (IVPs)
> - Boundary Value Problems (BVPs)
> - Initial-Boundary Value Problems (IBVPs)

## 6. Fundamental Theoretical Questions

> [!question] Existence and Uniqueness
> - Under what conditions does a solution exist?
> - When is the solution unique?
> - How do initial or boundary conditions determine the solution?

> [!question] Solution Behavior
> - How do solutions behave over their domains?
> - Can solutions become unbounded?
> - Do solutions converge to equilibrium states?
> - How sensitive are solutions to initial conditions and parameters?

## 7. Knowledge Relationships

### Foundation Knowledge

- **Calculus:** Provides differentiation and integration.
- **Linear Algebra:** Provides the mathematical framework for systems of differential equations.
- **Real Analysis:** Establishes rigorous foundations for convergence, continuity, and existence theorems.

### Downstream Knowledge

- **Ordinary Differential Equations:** Develops the theory of differential equations involving one independent variable.
- **Partial Differential Equations:** Develops the theory of differential equations involving multiple independent variables.
- **Qualitative Theory of Differential Equations:** Studies solution behavior without necessarily obtaining explicit solutions.
- **Numerical Methods for Differential Equations:** Develops numerical approximations to differential equation solutions.

## 8. Further Development

- Ordinary Differential Equations
- Partial Differential Equations
- Qualitative Theory of Differential Equations
- Numerical Methods for Differential Equations
- Advanced Differential Equation Theory

## 9. References

- Boyce, W. E., DiPrima, R. C., and Meade, D. B. *Elementary Differential Equations and Boundary Value Problems*. Wiley.
- Coddington, E. A. *An Introduction to Ordinary Differential Equations*. Dover Publications, 1989.
- Evans, L. C. *Partial Differential Equations*. American Mathematical Society, 2010.