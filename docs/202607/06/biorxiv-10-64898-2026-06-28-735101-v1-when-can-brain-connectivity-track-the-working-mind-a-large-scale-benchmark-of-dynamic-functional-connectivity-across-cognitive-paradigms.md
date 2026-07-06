---
title: When Can Brain Connectivity Track the Working Mind? A Large-Scale Benchmark of Dynamic Functional Connectivity Across Cognitive Paradigms
title_zh: 动态功能连接何时能追踪工作思维？跨认知范式的大规模基准测试
authors: "Torabi, M., Poline, J.-B., Mitsis, G. D."
date: 2026-06-29
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.28.735101v1.full.pdf"
tags: ["query:neuro-mental"]
score: 7.0
evidence: 动态功能连接方法的大规模基准测试
tldr: 动态功能连接能否可靠追踪认知状态？该研究对7种常用dFC方法进行了大规模基准测试，涵盖16个fMRI数据集、1500多名参与者和28种实验设置。结果发现，多数方法-实验组合的预测表现接近随机，无法可靠追踪认知参与。解码性能受实验设计、数据质量与dFC方法三因素交互影响：使用较长、规律的任务块且减少任务-休息转换的设计可显著提升可解码性。研究揭示了dFC作为认知状态标记的适用条件，为未来应用提供了可操作原则。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究动态功能连接能否可靠追踪认知参与状态，并明确导致失败的关键因素。
method: 在16个fMRI数据集和模拟数据上，基准测试7种dFC方法对任务存在性的预测能力。
result: 多数方法-实验组合表现接近随机；解码性能受实验设计、数据质量与dFC方法三者交互影响。
conclusion: 较长且规律的任务块设计可提升dFC可靠性，为认知状态标记的使用提供指导原则。
---

## 摘要
动态功能连接（dFC）——脑网络交互随时间变化的重构——已成为研究神经动态如何反映持续认知的广泛采用方法。然而，一个基本问题仍未解决：dFC能否可靠地追踪一个人何时处于认知参与状态，如果不能，为何失败？在此，我们通过一个大规模基准测试来解决这个问题，该测试涉及七种广泛使用的dFC方法，评估它们在16个fMRI数据集（涵盖超过1500名参与者、28种不同实验设置）中预测任务存在性的能力，并辅以真实模拟数据。

在实验数据中，基于dFC的认知参与追踪在许多情况下并不可靠：大多数方法-实验组合的表现接近随机水平，没有单一方法在所有情境中成功。然而，这种失败并非一致。实验和模拟数据均显示，解码性能随着三个相互作用的因素——实验设计、数据质量和dFC方法的选择——而系统性地变化，而不仅仅取决于dFC特征本身。

关键的是，我们识别出与更可靠追踪相关的特定实验设计条件：具有更长、更规则任务块和更少任务-休息转换的范式的可解码性显著更高，而数据质量独立地影响不同方法的性能。这些发现为何时可以期望（以及不能期望）dFC作为潜在认知状态的可靠标记提供了可操作的原则。

## Abstract
Dynamic functional connectivity (dFC) -- the time-varying re-configuration of brain network interactions -- has become a widely adopted method for studying how neural dynamics reflect ongoing cognition. Yet a fundamental question remains unresolved: can dFC reliably track when a person is cognitively engaged, and if not, why does it fail? Here, we address this question through a large-scale benchmark of seven widely used dFC methods, evaluating how well each predicts task presence across 16 fMRI datasets encompassing over 1,500 participants and 28 distinct experimental settings, complemented by realistic simulated data.

Across experimental data, dFC-based tracking of cognitive engagement was unreliable in many cases: most method-experiment combinations performed near chance, and no single method succeeded across all contexts. This failure, however, was not uniform. Both experimental and simulated data showed that decoding performance varied systematically with three interacting factors -- experimental design, data quality, and the choice of dFC method -- rather than depending on dFC features alone.

Critically, we identify specific experimental design conditions associated with more reliable tracking: paradigms with longer, more regular task blocks and fewer task-rest transitions were substantially more decodable, while data quality independently influenced performance across methods. These findings offer actionable principles for when dFC can -- and cannot -- be expected to serve as a reliable marker of underlying cognitive states.