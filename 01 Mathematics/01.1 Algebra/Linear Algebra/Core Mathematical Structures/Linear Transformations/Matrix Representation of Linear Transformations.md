---
type: technical-term
title: "Matrix Representation of Linear Transformations"
aliases:
  - Matrix Representation
  - Standard Matrix of a Linear Transformation
  - Transformation Matrix
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
  - matrix-representation
sources:
  - "Axler, Linear Algebra Done Right, 3rd Edition, 2015"
  - "Strang, Introduction to Linear Algebra, 5th Edition, 2016"
related: []
projects: []
---
> [!abstract] Definition
> A matrix representation of a linear transformation is a matrix that encodes the transformation relative to chosen bases of its domain and codomain.
>
> It converts an abstract linear mapping into a coordinate-based matrix operation.

## 1. Mathematical Framework

Let:

$$
T:V\rightarrow W
$$

where $V$ and $W$ are finite-dimensional vector spaces.

Choose ordered bases:

$$
B=(\mathbf{v}_1,\ldots,\mathbf{v}_n)
$$

$$
C=(\mathbf{w}_1,\ldots,\mathbf{w}_m)
$$

The matrix representation of $T$ relative to $B$ and $C$ is denoted by:

$$
[T]_{C\leftarrow B}
\in\mathbb{F}^{m\times n}
$$

## 2. Construction

> [!method] Constructing the Representation Matrix
> For each basis vector $\mathbf{v}_j$ in the domain basis, compute:
>
> $$
> T(\mathbf{v}_j)
> $$
>
> Express the result in the codomain basis:
>
> $$
> T(\mathbf{v}_j)
> =
> a_{1j}\mathbf{w}_1+\cdots+
> a_{mj}\mathbf{w}_m
> $$
>
> The coordinate vector becomes the $j$-th column:
>
> $$
> [T]_{C\leftarrow B}
> =
> \begin{bmatrix}
> |&|&&|\\
> [T(\mathbf{v}_1)]_C&
> [T(\mathbf{v}_2)]_C&
> \cdots&
> [T(\mathbf{v}_n)]_C\\
> |&|&&|
> \end{bmatrix}
> $$

## 3. Coordinate Transformation Equation

> [!important] Matrix Representation
> For every $\mathbf{v}\in V$:
>
> $$
> [T(\mathbf{v})]_C
> =
> [T]_{C\leftarrow B}[\mathbf{v}]_B
> $$
>
> The matrix acts on the coordinate vector of the input and produces the coordinate vector of the output.

## 4. Standard Matrix Representation

For the standard bases of $\mathbb{R}^n$ and $\mathbb{R}^m$, the matrix columns are:

$$
A=
\begin{bmatrix}
|&|&&|\\
T(\mathbf{e}_1)&T(\mathbf{e}_2)&\cdots&T(\mathbf{e}_n)\\
|&|&&|
\end{bmatrix}
$$

## 5. Composition

> [!important] Composition and Matrix Multiplication
> Suppose:
>
> $$
> T:U\rightarrow V,\qquad S:V\rightarrow W
> $$
>
> Using compatible bases:
>
> $$
> [S\circ T]=[S][T]
> $$
>
> The order of multiplication follows the order of function application: $T$ acts first, then $S$.

## 6. Important Properties

- The matrix dimensions are determined by the dimensions of the domain and codomain.
- A fixed linear transformation has different matrix representations under different choices of bases.
- Once the bases are fixed, its matrix representation is unique.
- Matrix multiplication represents composition of linear transformations.
- The rank of the representation matrix equals the dimension of the image.

## 7. Knowledge Relationships

### Foundation Knowledge
- **Linear Transformations** — defines the abstract mapping.
- **Vector Spaces** — establishes the domain and codomain.
- **Basis** — provides the coordinate systems.
- **Matrices** — provides the representation structure.

### Downstream Knowledge
- **Change of Basis** — studies how representation matrices change when bases change.
- **Similarity Transformations** — relates matrices of an endomorphism under different bases.
- **Matrix Factorization** — develops structured representations of matrices.
- **Eigenvalues and Eigenvectors** — studies properties of square transformation matrices.

## 8. References

- Axler, Sheldon. *Linear Algebra Done Right*, 3rd Edition, 2015.
- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.