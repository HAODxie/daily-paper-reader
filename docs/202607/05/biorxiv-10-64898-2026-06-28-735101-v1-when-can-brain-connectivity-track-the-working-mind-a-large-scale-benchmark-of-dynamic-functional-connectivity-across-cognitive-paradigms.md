---
title: When Can Brain Connectivity Track the Working Mind? A Large-Scale Benchmark of Dynamic Functional Connectivity Across Cognitive Paradigms
title_zh: 大脑连接何时能够追踪工作思维？跨认知范式的动态功能连接大规模基准测试
authors: "Torabi, M., Poline, J.-B., Mitsis, G. D."
date: 2026-06-29
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.28.735101v1.full.pdf"
tags: ["query:neuro-mental"]
score: 7.0
evidence: fMRI动态功能连接基准测试用于认知状态追踪
tldr: 动态功能连接（dFC）能否可靠追踪认知状态？本研究对7种dFC方法在16个fMRI数据集（1500+被试，28种实验设置）上进行了大规模基准测试。结果发现，大多数方法预测认知参与的表现接近随机，且无一种方法在所有情境下成功。解码性能受实验设计（更长、更规则的任务块和更少的任务-休息转换）、数据质量和方法选择的交互影响。研究提供了何时可预期dFC作为认知状态可靠标记的行动指南。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究动态功能连接能否可靠地追踪认知参与状态，并明确其失败原因。
method: 基于7种dFC方法，在16个fMRI数据集（含1500+被试和28种实验设置）及模拟数据上进行任务存在预测的基准测试。
result: 多数方法预测表现近随机；实验设计（长规则任务块、少转换）和数据质量是影响解码性能的关键因素。
conclusion: dFC追踪认知状态不可靠但受条件制约，为实验设计提供了可操作的优化原则。
---

## 摘要
动态功能连接（dFC）——即脑网络相互作用的时变重构——已成为研究神经动态如何反映持续认知的广泛采用方法。然而，一个基本问题仍未解决：dFC能否可靠地追踪一个人何时处于认知参与状态，如果不能，其失败的原因是什么？在此，我们通过一项包含七种广泛使用的dFC方法的大规模基准测试来探讨这一问题，评估每种方法在16个fMRI数据集（涵盖超过1500名参与者、28种不同实验设置）以及补充的现实模拟数据中预测任务存在性的能力。

在实验数据中，基于dFC的认知参与追踪在许多情况下并不可靠：大多数方法-实验组合的表现接近随机水平，且没有一种方法能在所有情境中成功。然而，这种失败并非均匀分布。实验和模拟数据均显示，解码性能系统地随三个相互作用因素——实验设计、数据质量和dFC方法的选择——而变化，而非仅依赖于dFC特征本身。

关键的是，我们识别出与更可靠追踪相关的特定实验设计条件：具有更长、更规则任务区块以及更少任务-静息转换的范式显著更易解码，而数据质量则独立地影响各方法的性能。这些发现为dFC何时可以（以及何时不能）被期望作为潜在认知状态的可靠标记提供了可操作的指导原则。

## Abstract
Dynamic functional connectivity (dFC) -- the time-varying re-configuration of brain network interactions -- has become a widely adopted method for studying how neural dynamics reflect ongoing cognition. Yet a fundamental question remains unresolved: can dFC reliably track when a person is cognitively engaged, and if not, why does it fail? Here, we address this question through a large-scale benchmark of seven widely used dFC methods, evaluating how well each predicts task presence across 16 fMRI datasets encompassing over 1,500 participants and 28 distinct experimental settings, complemented by realistic simulated data.

Across experimental data, dFC-based tracking of cognitive engagement was unreliable in many cases: most method-experiment combinations performed near chance, and no single method succeeded across all contexts. This failure, however, was not uniform. Both experimental and simulated data showed that decoding performance varied systematically with three interacting factors -- experimental design, data quality, and the choice of dFC method -- rather than depending on dFC features alone.

Critically, we identify specific experimental design conditions associated with more reliable tracking: paradigms with longer, more regular task blocks and fewer task-rest transitions were substantially more decodable, while data quality independently influenced performance across methods. These findings offer actionable principles for when dFC can -- and cannot -- be expected to serve as a reliable marker of underlying cognitive states.