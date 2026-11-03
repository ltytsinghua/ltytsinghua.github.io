---
title: "Efficient optimization of variational tensor-network approach to three-dimensional statistical systems"
collection: publications
category: manuscripts
permalink: /publication/2025-10-02-variational-tn-3d-statistical
excerpt: 'Variational tensor-network optimization for 3D statistical models requires repeatedly contracting a three-layer network made of a projected entangled-pair operator and projected entangled-pair states, which is computationally expensive. We proposed a split corner-transfer-matrix renormalization group (split CTMRG) contraction scheme for this network, reducing the cost from <i>O</i>(<i>D</i><sup>10</sup>) to <i>O</i>(<i>D</i><sup>9</sup>) without loss of accuracy. Results for the 3D classical Ising model match the precision of state-of-the-art Monte Carlo simulations, with a significant speed-up over previous variational tensor-network methods.'
journal_ref: '<i>Phys. Rev. B</i> <b>112</b>, 134403 (2025)'
excerpt_zh: '三维统计模型的变分张量网络优化需要反复收缩由投影纠缠对算符与投影纠缠对态构成的三层张量网络，计算代价高昂。本工作针对该三层网络提出分裂角转移矩阵重整化群（split CTMRG）收缩方案，在保持精度的同时将复杂度从 <i>O</i>(<i>D</i><sup>10</sup>) 降至 <i>O</i>(<i>D</i><sup>9</sup>)。在三维经典 Ising 模型上的结果与最新蒙特卡洛模拟精度相当，相比以往变分张量网络方法显著加速。'
date: 2025-10-02
venue: 'Physical Review B'
authors: 'Xia-Ze Xu<sup>*</sup>, <b>Tong-Yu Lin</b><sup>*</sup>, and Guang-Ming Zhang'
role: 'Co-first author'
paperurl: 'https://doi.org/10.1103/7dbj-w7cn'
---

We employ a split corner-transfer renormalization group scheme tailored for contracting
the triple-layer tensor network that arises in variational optimization of
three-dimensional classical statistical systems, substantially reducing the
computational complexity while keeping high accuracy. Benchmarks on the 3D classical
Ising model show results comparable to the most recent Monte Carlo simulations,
making the method well-suited for efficient gradient-based optimization in 3D
tensor-network simulations.
