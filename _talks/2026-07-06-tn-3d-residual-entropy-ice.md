---
title: "Tensor-Network Methods for Three-Dimensional Classical Statistical Models and Their Application to the Residual Entropy of Ice"
collection: talks
type: "Invited talk"
permalink: /talks/2026-07-06-tn-3d-residual-entropy-ice/
venue: "Quantum Science Center of Guangdong-Hong Kong-Macao Greater Bay Area"
date: 2026-07-06
location: "Shenzhen, China"
---

Tensor-network methods are by now well developed for two-dimensional classical statistical models, but extending them to three dimensions remains challenging: evaluating the free-energy density and its gradient requires contracting a triple-layer tensor network built from a projected entangled-pair operator (PEPO) and projected entangled-pair states (PEPS), which is computationally demanding.

In this talk I will describe two recent works along this direction. First, we introduce a split corner-transfer-matrix renormalization group (split CTMRG) scheme for triple-layer contraction that reduces the computational complexity while retaining accuracy, making gradient-based variational optimization feasible in 3D; benchmarked on the three-dimensional Ising model, our results agree with recent Monte Carlo simulations. Second, we apply this approach to a long-standing question—whether the residual entropies of hexagonal and cubic ice are equal. We propose a perspective based on analyzing the normality of the transfer operator and examine it numerically with variational tensor-network methods. This analysis also allows a direct computation of both residual entropies using the split CTMRG algorithm, providing numerical evidence supporting the equality between $$S_h$$ and $$S_c$$.
