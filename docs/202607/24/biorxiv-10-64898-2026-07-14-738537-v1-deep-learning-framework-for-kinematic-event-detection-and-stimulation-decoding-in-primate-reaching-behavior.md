---
title: Deep learning framework for kinematic event detection and stimulation decoding in primate reaching behavior
title_zh: 灵长类类动物触达行为中运动学事件检测和刺激解码的深度学习框架
authors: "Markus, A., Sinha, N., Prut, Y., Goldberger, J."
date: 2026-07-20
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.14.738537v1.full.pdf"
tags: ["query:neuro-mental"]
score: 7.0
evidence: 深度学习用于神经科学中的运动事件检测
tldr: "研究基于双向LSTM的深度学习框架，分析非人灵长类单次三维抓取运动，自动检测起始时刻与矫正转折点，并区分小脑阻断扰动与对照试验。相比速度阈值法，检测误差显著减小至10毫秒内，但跨动物应用需正交Procrustes对齐才能恢复精度。解码扰动试验的准确率达71%和62%，但跨动物泛化失败，说明运动事件结构可迁移，而扰动补偿策略具有动物特异性。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738537-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1637, \"height\": 666, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738537-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1588, \"height\": 911, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738537-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1136, \"height\": 609, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738537-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1516, \"height\": 668, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738537-v1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1638, \"height\": 592, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738537-v1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1638, \"height\": 595, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738537-v1/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1589, \"height\": 565, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-14-738537-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1648, \"height\": 570, \"label\": \"Table\"}]"
motivation: 现有运动事件检测依赖速度阈值，误差大且跨个体泛化差；需可靠区分神经干扰引起的运动变化，以理解运动控制的神经机制。
method: 基于双向LSTM的框架处理三维抓取轨迹，检测运动起始与转折点；使用正交Procrustes对齐跨动物坐标，并采用分类模型解码扰动与对照试验。
result: "运动起始检测误差约9ms，显著优于速度阈值法；扰动解码准确率71%/61.9%，跨动物泛化仅随机水平，几何对齐无法改善。"
conclusion: 几何对齐可迁移共享运动事件结构，但扰动诱发的运动变化反映动物特异性补偿策略，不支持跨动物通用模型。
---

## 摘要
对运动行为的准确分析需要可靠地检测正在进行的运动学事件，并详细描述因神经损伤而发生的运动输出变化。本文介绍了一种基于双向长短期记忆（BiLSTM）网络的深度学习框架，该框架用于分析从两只非人类灵长类动物记录的单试验三维触达轨迹。该框架用于检测运动起始和校正转折点，并将控制试验与抑制小脑输出的扰动试验区分开来。将此方法与手动注释数据进行了比较。在检测运动起始时间方面，仅观察到较小的动物内误差（两只猴子分别为8.92 ± 2.03毫秒和9.56 ± 3.64毫秒）。这些误差显著小于（p < 0.001）使用传统速度阈值方法获得的误差。将相同的检测算法从一只动物转移到另一只动物会导致较大误差，因为重建的工作空间以不同的坐标框架表示。正交Procrustes对齐显著减少了动物间的事件检测误差，并使性能更接近动物内范围。对扰动试验与控制试验的解码达到了每只动物高于偶然水平的准确性（准确率分别为71.0%和61.9%）。然而，动物间的泛化能力较差（接近偶然水平），并且几何对齐并未改善这一状况。这些发现表明，几何对齐可以支持动物之间共享运动学事件结构的转移，但与扰动相关的运动变化反映了动物特定的补偿策略，这些策略无法泛化。

## Abstract
Accurate analysis of motor behavior requires the reliable detection of ongoing kinematic events and a granular characterization of the changes in motor output that occur in response to neural impairments. This article describes a deep learning framework based on bidirectional long short-term memory (BiLSTM) networks developed to analyze single-trial three-dimensional reaching trajectories recorded from two non-human primates. The framework was used to detect movement onset and corrective turning points, and to differentiate control from the perturbed trials during which cerebellar output was blocked. This approach was compared to manually annotated data. Only small within-animal errors in detecting movement onset times were observed (8.92 +/- 2.03 ms and 9.56 +/- 3.64 ms for the two monkeys). These errors were significantly smaller (p < 0.001) than those obtained using conventional velocity-threshold methods. Transferring the same detection algorithm from one animal to the other resulted in large errors because the reconstructed workspaces were represented in different coordinate frames. Orthogonal Procrustes alignment substantially reduced the between-animal event-detection errors, and brought performance closer to the within-animal range. Decoding of the perturbed vs. the control trials achieved above-chance levels of accuracy for each animal (accuracies of 71.0% and 61.9% respectively). However, the between-animal generalization was poor (near chance level) and was not improved by geometric alignment. These findings suggest that geometric alignment can support the transfer of shared kinematic event structure between animals, but that perturbation-related changes in movements reflect animal-specific compensatory strategies which cannot be generalized.