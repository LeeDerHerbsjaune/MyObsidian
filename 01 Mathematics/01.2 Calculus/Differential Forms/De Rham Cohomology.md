---
type: technical-term
title: "De Rham Cohomology"
aliases:
  - de Rham Cohomology Groups
field:
  - Mathematics
subfield:
  - Differential Geometry
  - Algebraic Topology
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - differential-forms
  - algebraic-topology
sources:
  - "Bott & Tu (1982), Differential Forms in Algebraic Topology"
  - "Lee (2012), Introduction to Smooth Manifolds"
related: []
projects: []
---

> [!abstract] Definition
> **De Rham cohomology** is a mathematical theory that uses differential forms to study the global topology of smooth manifolds.
>
> It classifies closed differential forms modulo exact differential forms.

> [!important] Cohomology Groups
> Let
>
> $$Z^k(M)=\ker(d:\Omega^k(M)\rightarrow\Omega^{k+1}(M))$$
>
> be the space of closed $k$-forms, and
>
> $$B^k(M)=\operatorname{im}(d:\Omega^{k-1}(M)\rightarrow\Omega^k(M))$$
>
> be the space of exact $k$-forms.
>
> Since $d^2=0$:
>
> $$B^k(M)\subseteq Z^k(M)$$
>
> The $k$th de Rham cohomology group is
>
> $$\boxed{H^k_{\mathrm{dR}}(M)=
> \frac{Z^k(M)}{B^k(M)}}$$

> [!note] Cohomology Classes
> Two closed forms $\alpha$ and $\beta$ represent the same cohomology class if their difference is exact:
>
> $$\alpha-\beta=d\eta$$
>
> Their equivalence class is denoted
>
> $$[\alpha]\in H^k_{\mathrm{dR}}(M)$$
>
> Thus, cohomology ignores differences between closed forms that arise from adding an exact form.

> [!important] Topological Meaning
> De Rham cohomology detects global obstructions to finding potentials.
>
> The Poincaré lemma guarantees local exactness of closed forms of positive degree, but global exactness can fail because of the topology of the manifold.

> [!example] Punctured Plane
> On $\mathbb{R}^2\setminus\{0\}$, the 1-form
>
> $$\omega=\frac{-y\,dx+x\,dy}{x^2+y^2}$$
>
> is closed but not exact.
>
> Its integral around a positively oriented unit circle is
>
> $$\int_{S^1}\omega=2\pi$$
>
> This nonzero integral demonstrates that it cannot be globally exact.

> [!note] de Rham Theorem
> The de Rham theorem states that de Rham cohomology is naturally isomorphic to singular cohomology with real coefficients:
>
> $$H^k_{\mathrm{dR}}(M)\cong H^k(M;\mathbb{R})$$
>
> for smooth manifolds.
>
> This establishes a deep connection between differential calculus and algebraic topology.

> [!note] Betti Numbers
> For a compact smooth manifold, the dimension of the de Rham cohomology group is the $k$th Betti number:
>
> $$b_k=\dim H^k_{\mathrm{dR}}(M)$$
>
> These numbers encode topological information about the manifold.

> [!warning] Cohomology Versus Differential Calculus
> De Rham cohomology is not merely a method for solving differential equations.
>
> It is a global topological invariant constructed from the differential-form complex.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Differential Forms — provides the cochain spaces.
> - Exterior Derivative — defines the differential operator.
> - Closed Forms — provides the kernel of the exterior derivative.
> - Exact Forms — provides its image.
> - Algebraic Topology — supplies the cohomological framework.
>
> **Downstream Knowledge**
> - Hodge Theory — gives geometric representatives of de Rham cohomology classes under suitable compactness and metric assumptions.
> - Differential Topology — uses cohomology to study smooth manifolds.
> - Characteristic Classes — develops further topological invariants.