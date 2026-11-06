---
type: technical-term
title: "Exact Differential Equations"
aliases:
  - Exact ODEs
  - Exact First-Order Differential Equations
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

# Exact Differential Equations

> [!abstract] Definition
> An Exact Differential Equation is a first-order differential equation that can be expressed as the total differential of a scalar potential function.
>
> Its solution is obtained by finding a potential function whose total differential reproduces the original equation.

## 1. Mathematical Representation

> [!abstract] Standard Form
>
> $$M(x,y)dx+N(x,y)dy=0$$
>
> The equation is exact if there exists a scalar function $\Psi(x,y)$ such that:
>
> $$d\Psi=\Psi_xdx+\Psi_ydy$$
>
> Consequently:
>
> $$\Psi_x=M,\qquad \Psi_y=N$$

## 2. Exactness Condition

> [!important] Exactness Criterion
> Assuming the relevant first partial derivatives are continuous on a suitable simply connected domain, the equation is exact if and only if:
>
> $$\frac{\partial M}{\partial y}
> =
> \frac{\partial N}{\partial x}$$
>
> This condition ensures that $Mdx+Ndy$ is an exact differential form.

## 3. Solution Method

> [!note] Potential Function Method
> 1. Identify $M(x,y)$ and $N(x,y)$.
> 2. Verify the exactness condition.
> 3. Integrate $M$ with respect to $x$:
>
> $$\Psi(x,y)=\int M(x,y)dx+g(y)$$
>
> 4. Differentiate $\Psi$ with respect to $y$.
> 5. Compare with $N(x,y)$ to determine $g(y)$.
> 6. Express the general solution as:
>
> $$\Psi(x,y)=C$$

## 4. Integrating Factors

> [!note] Integrating Factor
> If an equation is not exact, it may become exact after multiplication by a suitable nonzero integrating factor $\mu(x,y)$:
>
> $$\mu Mdx+\mu Ndy=0$$
>
> The resulting equation must satisfy:
>
> $$\frac{\partial(\mu M)}{\partial y}
> =
> \frac{\partial(\mu N)}{\partial x}$$
>
> Special cases allow integrating factors depending only on $x$ or only on $y$.

## 5. Properties

- Exact equations admit a potential function on the appropriate domain.
- Their solutions are represented by level curves of the potential function.
- Exactness is a local differential condition; global potential existence also depends on the domain.
- The solution is generally obtained implicitly.
- Integrating factors can transform certain non-exact equations into exact equations.

## 6. Examples

> [!example] Example
>
> $$2xy\,dx+x^2\,dy=0$$
>
> Identify:
>
> $$M=2xy,\qquad N=x^2$$
>
> Verify:
>
> $$\frac{\partial M}{\partial y}=2x$$
>
> $$\frac{\partial N}{\partial x}=2x$$
>
> Therefore, the equation is exact.
>
> Integrating $M$ with respect to $x$:
>
> $$\Psi(x,y)=x^2y+g(y)$$
>
> Comparing its partial derivative with $N$ gives $g'(y)=0$.
>
> The solution is:
>
> $$x^2y=C$$

## 7. Knowledge Relationships

### Foundation Knowledge

- First-Order Ordinary Differential Equations — provides the general equation framework.
- Multivariable Calculus — provides partial derivatives and total differentials.
- Differential Forms — provides the mathematical framework for exact differential expressions.

### Downstream Knowledge

- Integrating Factors — extends the solution of non-exact differential equations.
- Potential Functions — develops the concept of scalar potentials.
- Differential Forms — provides a broader geometric treatment of exactness.

## 8. References

- Boyce, W. E., DiPrima, R. C., and Meade, D. B. *Elementary Differential Equations and Boundary Value Problems*. Wiley.
- Zill, D. G. *A First Course in Differential Equations with Modeling Applications*. Cengage.