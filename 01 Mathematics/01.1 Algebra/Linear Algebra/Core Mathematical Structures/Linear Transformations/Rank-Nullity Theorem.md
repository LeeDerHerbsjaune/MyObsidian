---
type: technical-term
title: "Rank-Nullity Theorem"
aliases:
  - Rank-Nullity
  - Dimension Theorem
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
  - rank-nullity-theorem
sources:
  - "Axler, Linear Algebra Done Right, 3rd Edition, 2015"
  - "Strang, Introduction to Linear Algebra, 5th Edition, 2016"
related: []
projects: []
---
> [!abstract] Definition
> The Rank-Nullity Theorem states that the dimension of the domain of a linear transformation equals the sum of the dimensions of its kernel and image.
>
> It establishes a fundamental relationship between the input directions mapped to zero and the independent output directions produced by the transformation.

## 1. Mathematical Statement

> [!theorem] Rank-Nullity Theorem
> Let:
>
> $$
> T:V\rightarrow W
> $$
>
> be a linear transformation where $V$ is finite-dimensional.
>
> Then:
>
> $$
> \boxed{
> \dim(V)=\dim(\ker T)+\dim(\operatorname{im}T)
> }
> $$
>
> Equivalently:
>
> $$
> \boxed{
> \dim(V)=\operatorname{nullity}(T)+\operatorname{rank}(T)
> }
> $$

## 2. Matrix Form

For a matrix:

$$
A\in\mathbb{F}^{m\times n}
$$

the theorem becomes:

$$
\boxed{
n=\operatorname{rank}(A)+\operatorname{nullity}(A)
}
$$

Where:
- $n$: Number of columns of $A$.
- $\operatorname{rank}(A)$: Dimension of the column space.
- $\operatorname{nullity}(A)$: Dimension of the null space.

## 3. Example

Consider:

$$
A=
\begin{bmatrix}
1&2&3\\
2&4&6
\end{bmatrix}
$$

The second row is twice the first row, so:

$$
\operatorname{rank}(A)=1
$$

Since $A$ has three columns:

$$
\operatorname{nullity}(A)=3-1=2
$$

Therefore:

$$
3=1+2
$$

## 4. Conceptual Interpretation

> [!important] Input Space Decomposition
> The theorem expresses the dimension of the domain as the sum of:
>
> - Directions that are mapped to zero by the transformation.
> - Independent directions represented in the image.
>
> The kernel describes the loss of distinguishable input information, while the image describes the output space actually reached.

## 5. Important Consequences

> [!important] Injectivity Criterion
> For finite-dimensional $V$:
>
> $$
> T\text{ is injective}
> \iff
> \operatorname{nullity}(T)=0
> $$

> [!important] Surjectivity Criterion
> $$
> T\text{ is surjective}
> \iff
> \dim(\operatorname{im}T)=\dim(W)
> $$

> [!important] Equal Dimensions
> If $V$ and $W$ are finite-dimensional and:
>
> $$
> \dim(V)=\dim(W)
> $$
>
> then injectivity and surjectivity of $T$ are equivalent.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Linear Transformations** — establishes the mapping.
- **Kernel and Image** — defines the two subspaces in the theorem.
- **Dimension** — provides the concept of subspace dimension.
- **Null Space and Column Space** — provides the matrix interpretation.

### Downstream Knowledge
- **Matrix Rank** — develops rank as the dimension of the image.
- **Linear Systems** — uses nullity to determine the number of free variables in a homogeneous system.
- **Invertible Linear Transformations** — uses zero nullity and full image to characterize invertibility.
- **Dimension Theory** — develops further relationships between vector spaces and their subspaces.

## 7. References

- Axler, Sheldon. *Linear Algebra Done Right*, 3rd Edition, 2015.
- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.
- Hoffman, Kenneth, and Ray Kunze. *Linear Algebra*, 2nd Edition, 1971.