---
type: technical-term
title: "Related Rates"
aliases:
  - Related Rates Problems
  - Tốc độ biến thiên liên quan
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus
  - Differential Calculus
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - mathematics
  - calculus
  - differentiation
sources: []
related: []
projects: []
---

# Related Rates

> [!abstract] Definition
> Related Rates is an application of differential calculus that studies the relationships between the rates of change of multiple interdependent quantities.
>
> It determines how one quantity changes with respect to time when its relationship with other time-dependent quantities is known.

## 1. Time-Dependent Variables

> [!definition] Definition
> Related rates problems involve variables that depend on time.

$$
x=x(t),\qquad y=y(t)
$$

Their rates of change are:

$$
\frac{dx}{dt},\qquad \frac{dy}{dt}
$$

## 2. Differentiating Relationships

> [!important] Key Principle
> If two variables satisfy a relationship, differentiate that relationship with respect to time to establish a relationship between their rates.

For:

$$
F(x,y)=0
$$

Differentiating with respect to $t$:

$$
F_x\frac{dx}{dt}
+
F_y\frac{dy}{dt}=0
$$

## 3. Chain Rule

> [!info] Application
> The chain rule connects the rate of change of a dependent variable with respect to another variable to its rate of change with respect to time.

$$
\frac{dy}{dt}
=
\frac{dy}{dx}\frac{dx}{dt}
$$

## 4. General Problem-Solving Method

> [!important] Procedure
> 1. Identify the quantities that change with time.
> 2. Define the relevant variables.
> 3. Establish the mathematical relationship between them.
> 4. Differentiate the relationship with respect to time.
> 5. Substitute known values and rates.
> 6. Solve for the unknown rate.
> 7. Verify signs and physical units.

## 5. Geometric Relationships

> [!example] Circle

For a circle:

$$
A=\pi r^2
$$

Differentiating with respect to time:

$$
\frac{dA}{dt}
=
2\pi r\frac{dr}{dt}
$$

For a sphere:

$$
V=\frac{4}{3}\pi r^3
$$

Therefore:

$$
\frac{dV}{dt}
=
4\pi r^2\frac{dr}{dt}
$$

## 6. Sign Interpretation

> [!note] Increasing and Decreasing Quantities
> - Positive rate: Quantity increases with time.
> - Negative rate: Quantity decreases with time.
> - Zero rate: Quantity has zero instantaneous rate of change.

## 7. Knowledge Relationships

### Foundation Knowledge
- **Derivatives:** Provides the mathematical concept of instantaneous rates of change.
- **Differentiation Rules:** Provides the computational procedures.
- **Chain Rule:** Establishes the relationship between different rates of change.
- **Implicit Differentiation:** Provides techniques for differentiating interdependent variables.

### Downstream Knowledge
- **Multivariable Calculus:** Generalizes rate relationships to multiple independent variables.
- **Ordinary Differential Equations:** Develops mathematical models involving time-dependent rates.
- **Mathematical Modeling:** Applies related rates to changing physical and geometric systems.

## 8. References

- Stewart, James (2015). *Calculus: Early Transcendentals*. 8th Edition.
- Apostol, Tom M. (1967). *Calculus, Volume 1*. Wiley.