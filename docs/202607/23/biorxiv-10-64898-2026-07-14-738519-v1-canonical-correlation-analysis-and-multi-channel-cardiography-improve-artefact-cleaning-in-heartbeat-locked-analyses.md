---
title: Canonical Correlation Analysis and Multi-Channel Cardiography Improve Artefact Cleaning in Heartbeat-Locked Analyses
title_zh: 典型相关分析与多通道心电图改善心跳锁定分析中的伪迹清理
authors: "Vidaurre, C., Azanova, M., Germanova, K., Greschke, E., Steinfath, T. P., Laufs, U., Uhe, T., Villringer, A., Nikulin, V."
date: 2026-07-20
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.14.738519v1.full.pdf"
tags: ["query:neuro-mental"]
score: 7.0
evidence: 脑电伪迹清理方法
tldr: 心跳锁定的神经生理分析常受心脏伪影干扰，传统单通道心电图去除不充分。本文提出基于典型相关分析的多通道心电图联合去伪影方法，在14名受试者中与独立成分分析比较。结果表明，该方法在减少R峰伪影和保留alpha功率方面系统性更优，仅需4-5个优化通道（如心前和锁骨上电极）即可达到15通道性能。研究为多通道心脏伪影去除提供了可靠框架和通道选择标准，提升了脑电分析的清洁质量。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738519-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 834, \"height\": 570, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738519-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1670, \"height\": 897, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738519-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1642, \"height\": 1154, \"label\": \"Figure\"}]"
motivation: 传统单通道心电图无法充分捕捉心脏电场的多维扩散，且缺乏整合多通道信号的成熟方法。
method: 基于典型相关分析，利用15通道心电图同时记录，对脑电信号进行多通道心脏伪影去除。
result: 典型相关分析在降低R峰伪影和保留alpha功率上系统性优于独立成分分析，4-5个优化通道性能接近15通道。
conclusion: 典型相关分析是多通道心脏伪影去除的可靠方法，并提供了通道配置的决策标准。
---

## 摘要
心脏伪迹对神经生理学分析构成问题，特别是在心跳锁定的大脑反应中，神经活动和伪迹在时间上同时发生。传统使用单通道心电图去除伪迹的方法无法完全捕捉心电场的多维分布。此外，即使记录了多个通道，也没有成熟的方法将其整合以去除伪迹。本文提出了一种基于典型相关的多变量方法用于心脏伪迹去除，并在14名参与者中同时记录定制15通道心电图和脑电图，报告其有效性。我们通过残余R波伪迹量化清理质量，通过alpha功率衡量神经信号保留。典型相关在减少R波伪迹和保留alpha功率方面系统性地优于传统的独立成分分析。通过分析所有可能的通道组合，我们发现当只有少量通道可用时，颈部或锁骨上电极可改善清理效果。使用四或五个通道时，心前区电极结合肢体或锁骨上位置可提供与15通道设置相当的性能。虽然这些发现需要在其他数据集中验证，但我们概述了清理效率的清晰决策标准，并表明典型相关是多通道心脏伪迹去除的可靠方法。

## Abstract
Cardiac artefacts are problematic for neurophysiological analyses, especially for heartbeat-locked brain responses where neural activity and artefacts co-occur in time. Traditional approaches using single-channel electrocardiography for artefact removal do not fully capture the multidimensional spread of cardiac fields. Moreover, even if several channels are recorded, no established methods exist for integrating them for artefact removal. Here, we propose a multivariate approach based on Canonical Correlation for cardiac artefact removal and report its effectiveness in electroencephalography recorded simultaneously with a custom 15-channel electrocardiography in 14 participants. We quantify cleaning quality via residual R-peak artefact and neural signal preservation via alpha power. Canonical Correlation systematically outperforms the traditional Independent Component Analysis in both reducing R-peak artefacts and preserving alpha power. By analysing all possible channel combinations, we found that neck or supraclavicular electrodes improve cleaning when only a few channels are available. With four or five channels, precordial electrodes in combination with limb or supraclavicular locations provide a performance comparable to the 15-channel setup. While these findings require validation in other datasets, we outline clear decision criteria for cleaning efficiency and show that canonical correlation is a reliable approach for multi-channel cardiac artefact removal.