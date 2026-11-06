---
type: technical-term
title: "Exact Forms"
aliases:
  - Exact Differential Forms
field:
  - Mathematics
subfield:
  - Differential Geometry
  - Differential Topology
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - differential-forms
sources:
  - "Bott & Tu (1982), Differential Forms in Algebraic Topology"
  - "Lee (2012), Introduction to Smooth Manifolds"
related: []
projects: []
---

> [!abstract] Definition
> A differential $k$-form $\omega$ is **exact** if there exists a $(k-1)$-form $\eta$ such that
>
> $$\omega=d\eta$$
>
> The space of exact $k$-forms is
>
> $$B^k(M)=\operatorname{im}(d:\Omega^{k-1}(M)\rightarrow\Omega^k(M))$$

> [!important] Exact Forms Are Closed
> Since $d^2=0$:
>
> $$d\omega=d(d\eta)=0$$
>
> Therefore:
>
> $$B^k(M)\subseteq Z^k(M)$$
>
> Every exact form is closed, but not every closed form is necessarily exact.

> [!example] Exact 1-Form
> If $f$ is a smooth scalar function, then
>
> $$\omega=df$$
>
> is an exact 1-form.
>
> Its coordinate representation is
>
> $$\omega=\frac{\partial f}{\partial x^i}dx^i$$

> [!note] Potential Forms
> If $\omega=d\eta$, then $\eta$ is called a potential or primitive of $\omega$.
>
> A form can have multiple potentials because adding a closed form to a potential does not change its exterior derivative.

> [!important] Global Versus Local Exactness
> The Poincaré lemma guarantees local exactness of closed forms of positive degree.
>
> Global exactness depends on the topology of the manifold.
>
> For example, on the punctured plane $\mathbb{R}^2\setminus\{0\}$, the form
>
> $$\omega=\frac{-y\,dx+x\,dy}{x^2+y^2}$$
>
> is closed but not globally exact.

> [!warning] Exactness Is Stronger Than Closedness
> The condition $d\omega=0$ is a differential condition.
>
> The condition $\omega=d\eta$ additionally requires a globally defined potential $\eta$.
>
> This distinction cannot generally be determined from local differential calculations alone.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Exterior Derivative — defines exactness.
> - Closed Forms — provides the larger space containing exact forms.
>
> **Downstream Knowledge**
> - De Rham Cohomology — classifies closed forms modulo exact forms.
> - Poincaré Lemma — explains local exactness.
> - Potential Theory — studies the existence of potentials in relevant settings.