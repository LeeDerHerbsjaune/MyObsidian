---
type: technical-term
title: "Nonhomogeneous Linear Second-Order ODEs"
aliases:
  - Nonhomogeneous Linear Second-Order Differential Equations
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
  - technical-term
  - differential-equations
sources: []
related: []
projects: []
---

# Nonhomogeneous Linear Second-Order ODEs

> [!abstract] Definition
> A nonhomogeneous linear second-order ODE has the form:
>
> $$a_2(x)y''+a_1(x)y'+a_0(x)y=g(x)$$
>
> where $g(x)$ is not identically zero.

## 1. Associated Homogeneous Equation

> [!definition]
> The associated homogeneous equation is obtained by setting the forcing function to zero:
>
> $$a_2(x)y''+a_1(x)y'+a_0(x)y=0$$

## 2. General Solution

> [!important] General Solution Theorem
> The general solution is:
>
> $$y=y_h+y_p$$
>
> where:
> - $y_h$ is the general solution of the associated homogeneous equation.
> - $y_p$ is any particular solution of the nonhomogeneous equation.

## 3. Methods of Solution

> [!method]
> - Method of Undetermined Coefficients
> - Variation of Parameters
> - Green's Function Method
>
> The Method of Undetermined Coefficients is especially useful for certain forcing functions, such as polynomials, exponentials, and trigonometric functions, when the coefficients are constant.

## 4. Foundation Knowledge

### Essential
- Homogeneous Linear Second-Order ODEs
- Linear Second-Order Ordinary Differential Equations

### Relevant
- Integration Techniques
- Linear Algebra
- Fundamental Set of Solutions

## 5. Downstream Knowledge

### Relevant
- Variation of Parameters
- Green's Functions
- Boundary-Value Problems

### Advanced
- Sturm–Liouville Theory
- Forced Oscillations

## 6. References

- Boyce, W. E., DiPrima, R. C., and Meade, D. B. *Elementary Differential Equations and Boundary Value Problems*. 11th ed., Wiley, 2017.