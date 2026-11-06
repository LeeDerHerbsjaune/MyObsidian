---
type: technical-term
title: "Derivatives"
aliases:
  - Derivative
  - Đạo hàm
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
  - differential-calculus
sources: []
related: []
projects: []
---

# Derivatives

> [!abstract] Definition
> A derivative is a mathematical quantity that measures the instantaneous rate of change of a function with respect to an independent variable.
>
> Geometrically, it represents the slope of the tangent line to the graph of a function at a given point.
>
> The derivative is the central mathematical object of Differential Calculus.

## 1. Difference Quotient

> [!definition] Definition
> The difference quotient measures the average rate of change of a function over an interval. 
$$
\frac{f(x+h)-f(x)}{h}
$$

> [!info] Interpretation
> - Numerator: Change in function value.
> - Denominator: Change in independent variable.
> - Ratio: Average rate of change.

## 2. Derivative Definition

> [!important] Limit Definition
> The derivative is defined as the limit of the difference quotient as the interval approaches zero.
$$
f'(x)=
\lim_{h\to 0}
\frac{f(x+h)-f(x)}{h}
$$

> [!note] Existence
> A derivative exists at a point when this limit exists and is finite.

## 3. Derivative Notations

> [!info] Common Notations
> For a function $y=f(x)$:
>
> - Lagrange notation: $f'(x)$
> - Leibniz notation: $\frac{dy}{dx}$
> - Operator notation: $Df(x)$
> - Newton notation: $\dot{x}$, commonly for time derivatives.

## 4. Geometric Interpretation

> [!definition] Tangent Slope
> The derivative at a point determines the slope of the tangent line to the function's graph.

$$
m_{\text{tangent}}=f'(a)
$$

The tangent line is:

$$
y-f(a)=f'(a)(x-a)
$$

## 5. One-Sided Derivatives

> [!definition] Left Derivative

$$
f'_-(a)=
\lim_{h\to0^-}
\frac{f(a+h)-f(a)}{h}
$$

> [!definition] Right Derivative

$$
f'_+(a)=
\lim_{h\to0^+}
\frac{f(a+h)-f(a)}{h}
$$

A two-sided derivative exists when both one-sided derivatives exist and are equal.

## 6. Fundamental Properties

> [!important] Properties
> - A derivative describes instantaneous rather than average change.
> - Differentiability implies continuity.
> - The derivative can be positive, negative, or zero.
> - A derivative can exist even when the function is not smooth in the everyday geometric sense.
> - A function may have different derivatives at different points.

## 7. Knowledge Relationships

### Foundation Knowledge
- **Functions:** Derivatives operate on functions.
- **Limits:** The derivative is defined using a limiting process.
- **Continuity:** Provides an important relationship with differentiability.
- **Difference Quotient:** Provides the expression from which the derivative is constructed.

### Downstream Knowledge
- **Differentiability:** Studies the existence of derivatives.
- **Differentiation Rules:** Develops systematic derivative computation.
- **Higher-Order Derivatives:** Extends differentiation through repeated operations.
- **Applications of Derivatives:** Uses derivatives for function analysis and optimization.

## 8. References

- Apostol, Tom M. (1967). *Calculus, Volume 1*. Wiley.
- Spivak, Michael (2008). *Calculus*. 4th Edition.