---
title: Generating whole-brain neural activity and behavior through unified latent dynamics
title_zh: 通过统一潜在动力学生成全脑神经活动和行为
authors: "Nuzzi, D., Mattia, M., Pezzulo, G."
date: 2026-07-14
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.05.730482v2.full.pdf"
tags: ["query:neuro-mental"]
score: 7.0
evidence: 使用深度生成模型建模线虫神经动态
tldr: 理解高维神经活动与行为如何从共享潜在动力学涌现是神经科学的核心挑战。本文提出NEBULA生成框架，利用秀丽隐杆线虫全脑记录学习统一潜在动力学，实现长时程神经和行为轨迹生成、逼真行为仿真及靶向虚拟干预。扰动揭示行为相关转换点，操纵可控制状态。该工作建立了连接脑动力与行为的框架，为虚拟实验提供基础。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-06-05-730482-v2/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1599, \"height\": 1654, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-06-05-730482-v2/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1598, \"height\": 1461, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-06-05-730482-v2/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1568, \"height\": 1573, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-06-05-730482-v2/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1693, \"height\": 1163, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-06-05-730482-v2/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1648, \"height\": 1465, \"label\": \"Figure\"}]"
motivation: 现有模型难以统一建模全脑神经活动与行为的长时程动态，阻碍数字孪生构建。
method: 提出NEBULA，基于变分自编码器学习共享潜在状态空间，联合生成神经活动与行为序列。
result: 在C. elegans全脑数据上，模型生成长时程动态，扰动发现行为转换点，干预实现状态控制。
conclusion: NEBULA为理解脑-行为涌现提供了生成框架，支持无训练干预和可扩展虚拟实验。
---

## 摘要
理解高维神经活动和行为如何从共享的底层动力学中涌现，仍然是神经科学中的一项基本挑战。解决这一问题对于实现能够忠实再现和预测生命系统多尺度脑-行为动力学的数字孪生至关重要。在这里，我们提出NEBULA（通过统一潜在动力学进行神经与行为建模），这是一个联合建模全脑神经活动和行为的生成框架。利用线虫的全脑记录，该模型学习了一个统一的潜在动力学结构，支持神经和行为轨迹的长时程生成、行为逼真模拟以及定向虚拟干预。对所学动力学的扰动揭示了行为相关的转变点，而引导干预则无需重新训练即可实现对神经和行为状态的可控操纵。这些结果建立了一个将活体生物的大脑动力学与行为联系起来的框架，并为神经科学中的可扩展虚拟实验提供了基础。

## Abstract
Understanding how high-dimensional neural activity and behavior emerge from shared underlying dynamics remains a fundamental challenge in neuroscience. Addressing this problem is key to enabling digital twins that can faithfully reproduce and predict the multiscale brain-behavior dynamics of living systems. Here we present NEBULA (NEural and Behavioral modeling through Unified LAtent dynamics), a generative framework that jointly models whole-brain neural activity and behavior. Using brain-wide recordings from C. elegans, the model learns a unified latent dynamical structure that supports long-horizon generation of neural and behavioral trajectories, realistic simulations of behavior, and targeted virtual interventions. Perturbations of the learned dynamics reveal behaviorally relevant transition points, whereas steering interventions enable controlled manipulation of neural and behavioral states without retraining. These results establish a framework for linking brain dynamics to behavior in a living organism and provide a foundation for scalable virtual experimentation in neuroscience.