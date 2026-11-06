---
type: technical-term
title: "Homogeneous Linear Second-Order ODEs"
aliases:
  - Homogeneous Linear Second-Order Differential Equations
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

# Homogeneous Linear Second-Order ODEs

> [!abstract] Definition
> A homogeneous linear second-order ODE is an equation of the form:
>
> $$a_2(x)y''+a_1(x)y'+a_0(x)y=0$$
>
> where $a_2(x)\neq0$ on the interval of interest.

## 1. Standard Form

> Dividing by the leading coefficient:
>
> $$y''+P(x)y'+Q(x)y=0$$

## 2. Superposition Principle

> [!important] Linear Superposition
> If $y_1$ and $y_2$ are solutions, then:
>
> $$y=c_1y_1+c_2y_2$$
>
> is also a solution.
>
> This property follows from the linearity of the differential operator.

## 3. Fundamental Set of Solutions

> [!definition]
> Two solutions $y_1,y_2$ form a fundamental set on an interval if they are linearly independent and span the solution space.
>
> Under regularity conditions, the general solution is:
>
> $$y=c_1y_1+c_2y_2$$

## 4. Solution Methods

> - Characteristic Equation for constant coefficients.
> - Reduction of Order.
> - Power Series Method.
> - Frobenius Method.
> - Cauchy–Euler Method for equations of Euler type.

## 5. Foundation Knowledge

### Essential
- Linear Second-Order Ordinary Differential Equations
- Linear Algebra
- Differential Calculus

### Relevant
- Linear Independence
- Vector Spaces

## 6. Downstream Knowledge

### Relevant
- Fundamental Set of Solutions
- Wronskian
- Abel's Identity

### Advanced
- Sturm–Liouville Theory
- Eigenvalue Problems
- Green's Functions

## 7. References

- Coddington, E. A. *An Introduction to Ordinary Differential Equations*. Dover Publications, 1989.