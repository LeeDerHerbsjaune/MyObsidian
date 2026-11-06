---
type: technical-term
title: "Change of Basis"
aliases:
  - Basis Transformation
  - Change-of-Basis Matrix
  - Coordinate Transformation
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
  - change-of-basis
sources:
  - "Axler, Linear Algebra Done Right, 3rd Edition, 2015"
  - "Strang, Introduction to Linear Algebra, 5th Edition, 2016"
related: []
projects: []
---
> [!abstract] Definition
> Change of basis is the process of converting the coordinate representation of a vector or linear transformation from one basis to another basis of the same vector space.
>
> The underlying vector or linear transformation remains unchanged; only its coordinate representation changes.

## 1. Coordinate Representation

Let $V$ be an $n$-dimensional vector space with two ordered bases:

$$
B=(\mathbf{b}_1,\ldots,\mathbf{b}_n)
$$

$$
C=(\mathbf{c}_1,\ldots,\mathbf{c}_n)
$$

For the same vector $\mathbf{v}\in V$:

$$
[\mathbf{v}]_B\neq[\mathbf{v}]_C
$$

in general.

The coordinate vectors differ because they express the same vector using different basis vectors.

## 2. Change-of-Basis Matrix

> [!definition] Change-of-Basis Matrix
> Let $P_{C\leftarrow B}$ denote the matrix that converts coordinates from basis $B$ to basis $C$.
>
> $$
> [\mathbf{v}]_C
> =
> P_{C\leftarrow B}[\mathbf{v}]_B
> $$
>
> Its columns are the coordinates of the vectors in $B$, expressed relative to $C$:
>
> $$
> P_{C\leftarrow B}
> =
> \begin{bmatrix}
> |&|&&|\\
> [\mathbf{b}_1]_C&
> [\mathbf{b}_2]_C&
> \cdots&
> [\mathbf{b}_n]_C\\
> |&|&&|
> \end{bmatrix}
> $$

<LearningViz type_id="CHANGE_OF_BASIS" />

## 3. Inverse Relationship

> [!important] Reverse Conversion
> The reverse change-of-basis matrix is:
>
> $$
> P_{B\leftarrow C}
> =
> (P_{C\leftarrow B})^{-1}
> $$
>
> Therefore:
>
> $$
> [\mathbf{v}]_B
> =
> (P_{C\leftarrow B})^{-1}
> [\mathbf{v}]_C
> $$

## 4. Change of Basis for Linear Transformations

Suppose $T:V\rightarrow V$ is a linear operator.

Let $A_B$ and $A_C$ be its matrix representations under bases $B$ and $C$, respectively.

Then:

$$
A_C
=
P_{C\leftarrow B}
A_B
P_{C\leftarrow B}^{-1}
$$

> [!important] Similarity
> Matrices representing the same linear operator under different bases are similar.
>
> Similar matrices represent the same underlying linear operator in different coordinate systems.

## 5. Fundamental Properties

- A change-of-basis matrix is invertible.
- The vector itself does not change.
- Only its coordinate representation changes.
- The matrix representation of a linear operator changes with the basis.
- Similar matrices have the same characteristic polynomial, determinant, and eigenvalues.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Vector Spaces** — defines the space in which basis changes occur.
- **Basis** — provides the coordinate systems.
- **Matrix Representation of Linear Transformations** — defines coordinate-based representations.

### Downstream Knowledge
- **Similarity Transformations** — formalizes relationships between matrix representations.
- **Diagonalization** — searches for a basis yielding a diagonal representation.
- **Eigenvalues and Eigenvectors** — provides the structural information used in diagonalization.
- **Coordinate Systems** — applies basis changes to coordinate descriptions.

## 7. References

- Axler, Sheldon. *Linear Algebra Done Right*, 3rd Edition, 2015.
- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.