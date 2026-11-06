---
type: technical-term
title: "Kernel and Image"
aliases:
  - Kernel
  - Image
  - Null Kernel
  - Range of a Linear Transformation
field:
  - Mathematics
subfield:
  - Linear Algebra
status: learning
confidence: 1
created: 2026-11-04
updated: 2026-11-04
tags:
  - mathematics
  - linear-algebra
  - kernel
  - image
sources:
  - "Axler, Linear Algebra Done Right, 3rd Edition, 2015"
related: []
projects: []
---
> [!abstract] Definition
> The kernel and image are two fundamental subspaces associated with a linear transformation.
>
> - The **kernel** contains all vectors mapped to the zero vector.
> - The **image** contains all possible outputs of the transformation.

## 1. Kernel

> [!definition] Kernel
> Let $T:V\rightarrow W$ be a linear transformation.
>
> The kernel of $T$ is:
>
> $$
> \ker(T)=
> \{\mathbf{v}\in V\mid T(\mathbf{v})=\mathbf{0}_W\}
> $$
>
> It is a subspace of the domain $V$.

## 2. Image

> [!definition] Image
> The image of $T$ is:
>
> $$
> \operatorname{im}(T)=
> \{T(\mathbf{v})\mid\mathbf{v}\in V\}
> $$
>
> It is a subspace of the codomain $W$.

## 3. Example

Consider:

$$
T:\mathbb{R}^2\rightarrow\mathbb{R}^2
$$

defined by:

$$
T(x,y)=(x+y,0)
$$

> [!example] Kernel
> To find the kernel, solve:
>
> $$
> T(x,y)=(0,0)
> $$
>
> Therefore:
>
> $$
> x+y=0
> $$
>
> Hence:
>
> $$
> \ker(T)=
> \left\{
> \begin{bmatrix}t\\-t\end{bmatrix}
> \mid t\in\mathbb{R}
> \right\}
> $$

> [!example] Image
> Every output has the form:
>
> $$
> T(x,y)=
> \begin{bmatrix}x+y\\0\end{bmatrix}
> $$
>
> Therefore:
>
> $$
> \operatorname{im}(T)=
> \left\{
> \begin{bmatrix}t\\0\end{bmatrix}
> \mid t\in\mathbb{R}
> \right\}
> $$

## 4. Important Properties

> [!important] Injectivity
> A linear transformation is injective if and only if:
>
> $$
> \ker(T)=\{\mathbf{0}_V\}
> $$

> [!important] Surjectivity
> A linear transformation $T:V\rightarrow W$ is surjective if and only if:
>
> $$
> \operatorname{im}(T)=W
> $$

> [!important] Subspace Properties
> $$
> \ker(T)\leq V
> $$
>
> $$
> \operatorname{im}(T)\leq W
> $$

## 5. Knowledge Relationships

### Foundation Knowledge
- **Linear Transformations** — defines the mapping whose kernel and image are studied.
- **Vector Spaces** — establishes the domain and codomain structures.
- **Subspaces** — provides the mathematical framework for kernel and image.

### Downstream Knowledge
- **Null Space and Column Space** — provides matrix-based descriptions of kernel and image.
- **Rank-Nullity Theorem** — relates the dimensions of the kernel and image.
- **Isomorphisms** — uses injectivity and surjectivity to characterize invertible linear maps.

## 6. References

- Axler, Sheldon. *Linear Algebra Done Right*, 3rd Edition, 2015.
- Hoffman, Kenneth, and Ray Kunze. *Linear Algebra*, 2nd Edition, 1971.