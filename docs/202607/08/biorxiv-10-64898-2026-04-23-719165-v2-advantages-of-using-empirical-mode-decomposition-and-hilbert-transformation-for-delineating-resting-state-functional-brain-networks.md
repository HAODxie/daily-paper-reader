---
title: Advantages of using Empirical Mode Decomposition and Hilbert Transformation for Delineating Resting State Functional Brain Networks
title_zh: 使用经验模态分解和希尔伯特变换描绘静息态功能脑网络的优势
authors: "Kaur, T., Yadav, S., Jain, N."
date: 2026-07-05
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.23.719165v2.full.pdf"
tags: ["query:neuro-mental"]
score: 8.0
evidence: 利用经验模态分解和希尔伯特变换进行静息态功能磁共振脑网络分析
tldr: 静息态功能连接研究旨在揭示大脑内在网络活动，但传统基于皮尔逊相关的BOLD信号分析难以与已知结构连接匹配。本研究采用经验模态分解（EMD）对fMRI时间序列进行分解，再通过希尔伯特变换（HT）提取瞬时相位，以计算功能连接。以体感运动网络为例，该方法显著提高了功能连接与结构连接的一致性，尤其适用于低时间分辨率（低TR）数据。EMD-HT方法为功能连接分析提供了更可靠的替代方案。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统基于皮尔逊相关系数的静息态功能连接与已知结构连接相关性差，需要改进方法。
method: 使用经验模态分解对BOLD时间序列进行分解，再经希尔伯特变换计算瞬时相位，从而确定功能连接。
result: 以体感运动网络为例，EMD-HT方法相比传统方法显著提升了功能连接与结构连接的相关性，对低TR数据尤为明显。
conclusion: EMD-HT方法能更准确地反映静息态功能脑网络，优于常用分析方法。
---

## 摘要
静息态功能连接研究的目标是确定身体在休息时脑网络的内在动态。当大脑参与各种任务（如处理感觉输入、启动运动活动或各种认知任务）时，这些网络会差异化激活。静息态功能连接网络通常通过确定受试者未主动执行任何任务时，使用功能磁共振成像（fMRI）从不同脑区收集的血氧水平依赖（BOLD）信号的皮尔逊相关系数来揭示。然而，这样确定的功能连接与不同脑区之间已知的结构连接相关性不佳。在此，我们使用经验模态分解（EMD）后接希尔伯特变换（HT）来确定人脑的静息态功能连接。我们以躯体运动网络为例展示了使用这种EMD-HT方法的优势。我们表明，与常用方法相比，该方法分解的时间序列数据改善了所推导的功能连接与已知结构连接的相关性（尤其是对于低TR的fMRI数据）。

## Abstract
The goal of the resting-state functional connectivity studies is to determine the inherent dynamics of the brain networks while the body is at rest. These networks get differentially activated when the brain is involved in various tasks such as processing of sensory inputs, initiating motor activities, or various cognitive tasks. Resting state functional connectivity networks are commonly revealed by determining Pearson Correlation Coefficients of the Blood Oxygenation Level Dependent (BOLD) signals collected from different brain regions using functional Magnetic Resonance Imaging (fMRI) while the subject is not actively performing any task. However, the functional connectivity thus determined does not correlate well with the known structural connectivity between different brain regions. Here, we used Empirical Mode decomposition (EMD), followed by Hilbert Transformation (HT), to determine the resting state functional connectivity in the human brains. We show the advantage of using this EMD-HT method using somatomotor network as an example. We show that the time series data decomposed by this method improves correlation of the derived functional connectivity with the known structural connectivity (especially for low -TR fMRI data) as compared to the methods commonly used.