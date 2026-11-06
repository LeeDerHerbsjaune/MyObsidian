---
type: technical-term
title: "Functions of Several Variables"
aliases:
  - Multivariable Functions
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus
  - Mathematical Analysis
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - multivariable-calculus
sources: []
related: []
projects: []
---

> [!abstract] Definition
> A **function of several variables** is a mathematical mapping whose output depends on two or more independent input variables.
>
> A scalar-valued function of $n$ variables is represented as:
>
> $$f:\mathbb{R}^n\rightarrow\mathbb{R}$$
>
> Its general form is:
>
> $$z=f(x_1,x_2,\ldots,x_n)$$

## 1. Domain and Range

> [!definition] Domain
> The domain of a multivariable function is the set of all valid input tuples for which the function is defined.
>
> $$D_f\subseteq\mathbb{R}^n$$

> [!definition] Range
> The range is the set of all attainable output values:
>
> $$R_f=\{f(\mathbf{x}):\mathbf{x}\in D_f\}$$

## 2. Types of Multivariable Functions

> [!note] Scalar-Valued Functions
> A scalar-valued function maps a multidimensional input to a single scalar:
>
> $$f:\mathbb{R}^n\rightarrow\mathbb{R}$$
>
> Example:
>
> $$f(x,y)=x^2+y^2$$

> [!note] Vector-Valued Functions
> A vector-valued function maps an input vector to an output vector:
>
> $$\mathbf{F}:\mathbb{R}^n\rightarrow\mathbb{R}^m$$
>
> Example:
>
> $$\mathbf{F}(x,y)=
> \begin{bmatrix}
> x+y\\
> xy
> \end{bmatrix}$$

## 3. Geometric Representations

> [!note] Graph
> For a scalar function of two variables:
>
> $$z=f(x,y)$$
>
> its graph is a surface in three-dimensional space.

> [!note] Level Sets
> A level set is the set of inputs that produce the same function value:
>
> $$f(x_1,\ldots,x_n)=c$$
>
> For two input variables, level sets are generally curves. For three input variables, they are generally surfaces.

> [!note] Contour Maps
> A contour map represents level curves in the input plane. Each curve corresponds to a constant function value.

## 4. Important Properties

> [!note] Boundedness
> A function is bounded on its domain if there exists $M>0$ such that:
>
> $$|f(\mathbf{x})|\leq M$$

> [!note] Symmetry
> Multivariable functions may exhibit symmetry under transformations of their input variables.
>
> For example, $f(x,y)=x^2+y^2$ is invariant under rotations around the origin.

> [!note] Composite Functions
> Multivariable functions can be composed with other functions or coordinate mappings, forming the basis of the multivariable chain rule.

## 5. Knowledge Relationships

### Foundation Knowledge
- **Functions:** Establishes the general concept of mathematical mappings.
- **Sets and Cartesian Products:** Define multidimensional input domains.
- **Coordinate Systems:** Provide representations of multidimensional inputs.

### Downstream Knowledge
- **Limits and Continuity of Multivariable Functions:** Studies local behavior.
- **Partial Derivatives:** Measures changes with respect to individual inputs.
- **Multiple Integrals:** Integrates functions over multidimensional domains.
- **Vector-Valued Functions:** Develops mappings with vector outputs.