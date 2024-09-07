---
layout: post
author: Rashid Alawadhi
title:  "Electromagnetism in a medium and the analogy with gravity"
date:   2024-09-07 22:20:00 +0400
categories: physics, gravity, general relativity, electromagnetism, maxwell's equations
---
Today I was thinking about the relativistic simple harmonic oscillator and what the correct action is for it. However, as I was checking a textbook by Maurizio Gasperini titled *Theory of Gravitational Interactions*, an interesting observation by the author had caught my eyes. He was discussing electromagnetism in curved spacetimes where the metric tensor $g_{\mu\nu}$ cannot be transformed into the Minkowski metric at all points in the manifold.

The author starts by reminding us that in the context of Minkowski spacetime, using the gauge field $A_\mu$, Maxwell equations can by succinctly expressed in the form

$$\partial_\nu F^{\mu\nu} = J^\mu, \quad F^{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu,$$

where $J_\mu$ is the current and the field strength tensor is $F_{\mu\nu}$ is related to the electric and magnetic fields by $F_{0i} = E_i$ and $F_{ij} = -\epsilon_{ijk}B^k$ respectively. However, given that the post is dealing with electromagnetism in a *medium*, there is another tensor $G_{\mu\nu}$ related to the field strength tensor by
\begin{align}
G^{\mu\nu} = \chi^{\mu\nu\alpha\beta}F_{\alpha\beta}.
\label{GF}
\end{align}

$G_{\mu\nu}$ describes the electric and magnetic field in a medium both denoted by $G^{0i} = D^i$ and $G^{ij} = -\epsilon^{ijk}H_k$ respectively. The previous equation is called the constitutive equation and $\chi^{\mu\nu\alpha\beta}$ is called the constitutive tensor which has the following properties

$$\chi^{\mu\nu\alpha\beta} = \chi^{[\mu\nu][\alpha\beta]} = \chi^{\alpha\beta\mu\nu}, \quad \chi^{[\mu\nu\alpha\beta]} = 0$$

$G_{\mu\nu}$ also satisfies the Maxwell equations in the respective medium

\begin{align}
\partial_\nu G^{\mu\nu} = J^\mu,\label{Gmax}
\end{align}

where the current is not necessarily the same as the one in the Maxwell equations for $F_{\mu\nu}$. The author gives a simple example by choosing a medium that is isotropic and non-conductive and choosing

$$\chi^{0i0j} = -\epsilon\delta^{ij}, \quad \chi^{ijkl} = \frac{1}{2\mu}(\delta^{ik}\delta^{jl} - \delta^{il}\delta^{jk}).$$

Then equation $\eqref{GF}$ gives $E=\epsilon D$ and $B = \mu H$ where $\epsilon$ and $\mu$ are constants controlling the strength of the electromagnetic field in the medium.

Let us now move on to the curved spacetime case modelled by a Riemannian manifold with a Levi-Civita connection $(M,g, \nabla)$. The Maxwell equation can be written as

\begin{align}
\partial_{\mu}(\sqrt{-g}F^{\mu\nu}) = J^{\nu}.\label{curvedMax}
\end{align}

Now we need a similar relationship to $\eqref{GF}$ between the field strength and a `gravitational' version of $G_{\mu\nu}$ by finding an effective constitutive tensor $\chi^{\mu\nu\alpha\beta}$ for the Riemannian manifold. First let us reintroduce the metric on the left hand side of $\eqref{curvedMax}$

$$\partial_{\mu}(\sqrt{-g}g^{\mu\alpha}g^{\nu\beta}F_{\alpha\beta}) = J^{\nu},$$

then using the symmetries of $F_{\alpha\beta}$ we can rewrite the LHS as

$$\partial_{\mu}(\sqrt{-g}\frac{1}{2}(g^{\mu\alpha}g^{\nu\beta}- g^{\mu\beta}g^{\nu\alpha})F_{\alpha\beta}) = J^{\nu}.$$

Now if we compare it to $\eqref{Gmax}$ and $\eqref{GF}$ we find the gravitational analogue of $G_{\mu\nu}$ and $\chi^{\mu\nu\alpha\beta}$ to be

$$\tilde{G}^{\mu\nu} = \tilde{\chi}^{\mu\nu\alpha\beta}F_{\alpha\beta}, \quad \tilde{\chi}^{\mu\nu\alpha\beta} = \frac{\sqrt{-g}}{2}(g^{\mu\alpha}g^{\nu\beta}- g^{\mu\beta}g^{\nu\alpha})$$

From this we can see that spacetime behaves like a medium in which electromagnetic waves travel through. The medium's properties are controlled by the gravitational analogue of the constitutive tensor $\tilde{\chi}^{\mu\nu\alpha\beta}$. One can think of the flat Minkowski spacetime as the vacuum case where electromagnetic waves do not bend, and is controlled by $\tilde{\chi}^{\mu\nu\alpha\beta} = \frac{1}{2}(\eta^{\mu\alpha}\eta^{\nu\beta}- \eta^{\mu\beta}\eta^{\nu\alpha})$. Therefore one finds that for the flat spacetime case $G_{\mu\nu} = F_{\mu\nu}$. On the other hand, when the metric is not flat, the constitutive tensor will cause a non-trivial situation where $\tilde{G}_ {\mu\nu} \neq F_{\mu\nu}$. This is not very surprising as just like in the usual case of electromagnetism where light's path can get altered by moving through different media, curved spacetime famously cases light to be bent around massive objects plus other phenomena such as rotating its polarisation, lensing, etc.