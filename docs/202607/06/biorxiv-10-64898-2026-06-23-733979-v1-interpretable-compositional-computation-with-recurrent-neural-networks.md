---
title: Interpretable compositional computation with recurrent neural networks
title_zh: 循环神经网络的解释性组合计算
authors: "Pezon, L., Van Meegen, A."
date: 2026-06-29
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.23.733979v1.full.pdf"
tags: ["query:neuro-mental"]
score: 6.0
evidence: 循环神经网络的可解释组合计算与神经科学中的动态结构
tldr: 循环神经网络在多任务训练中展现组合计算能力，但共享动态组件的本质不明。本文在低秩网络低维潜空间提出可解释组合计算理论，发现共享组件隐藏于神经活动，与任务依赖活动兼容，并在连接与表征中留下可测试标志。理论刻画了任务依赖的不同介入位点，揭示了组合计算的多种机制。
source: biorxiv
selection_source: fresh_fetch
motivation: 多任务训练的网络展现出跨任务共享的动态结构，但共享组件的性质及任务依赖使用方式尚不清楚。
method: 在低秩循环神经网络的低维潜空间中，基于共享动态结构构建可解释组合计算理论，并分析连接统计与表征。
result: 共享潜组件不直接出现在神经活动中，与任务依赖活动兼容；识别出连接与表征中的标志，可预测扰动响应并揭示任务依赖的多种介入位点。
conclusion: 提供了组合计算通过低秩网络共享组件的机制理解和可测试标志，促进对灵活认知的洞见。
---

## 摘要
灵活认知利用可重复使用的组件，使行为能够快速适应不同的情境或任务。对多个任务训练的人工神经网络分析表明，这种组合性由跨任务共享和重用的动力学结构支持。然而，这些共享组件的本质以及它们如何以任务依赖的方式被使用，仍不清楚。在此，我们发展了一个基于低秩循环神经网络低维潜在空间中共享动力学结构的可解释组合计算理论。我们表明，这些共享的潜在组件在神经活动中并不直接可见，因此与任务依赖的活动兼容。我们在连接统计和神经表征中识别了共享潜在组件的标志。这些标志为网络对特定扰动实验的响应提供了可检验的预测。最后，我们识别了任务依赖性可以进入计算的不同位置，使我们能够刻画组合任务的定性不同解决方案。总之，我们的理论通过低秩网络中的共享组件提供了组合计算的机理性理解和可检验的标志。

## Abstract
Flexible cognition utilizes reusable components to enable rapid adaptation of behavior to different contexts or tasks. Analysis of artificial neural networks trained on multiple tasks suggested that this compositionality is supported by dynamical structures which are shared and re-used across tasks. However, the nature of these shared components, and how they can be used in a task-dependent manner, remained unclear. Here, we develop a theory of interpretable compositional computation based on shared dynamical structures in the low-dimensional latent space of low-rank recurrent neural networks. We show that these shared latent components are not immediately visible in the neural activity, and are thus compatible with task-dependent activity. We identify hallmarks of shared latent components both in the connectivity statistics and the neural representations. These hallmarks yield testable predictions for the networks response to specific perturbation experiments. Finally, we identify distinct loci where task-dependence can enter the computation, allowing us to characterize qualitatively different solutions to compositional tasks. In summary, our theory provides a mechanistic understanding and testable hallmarks of compositional computation via shared components in low-rank networks.