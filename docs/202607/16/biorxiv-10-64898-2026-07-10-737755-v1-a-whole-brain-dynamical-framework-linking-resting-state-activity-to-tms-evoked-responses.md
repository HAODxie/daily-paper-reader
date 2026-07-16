---
title: A Whole-Brain Dynamical Framework Linking Resting-State Activity to TMS-Evoked Responses
title_zh: 全脑动力学框架：连接静息态活动与TMS诱发电位
authors: "Veronese, A., Momi, D., Sarasso, S., Corbetta, M., Allegra, M., Suweis, S."
date: 2026-07-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.10.737755v1.full.pdf"
tags: ["query:neuro-mental"]
score: 6.0
evidence: 连接静息态与TMS诱发反应的全局脑电框架
tldr: 理解外部扰动如何与脑活动交互是系统神经科学的挑战。本文提出一个分析上可处理的生成式全脑模型，连接静息态EEG与TMS诱发响应。模型仅需少量TMS-EEG trials即可估计有效连接，并准确预测未见过试次的TEP时空结构。该框架为个体化TMS-EEG建模和基于模型的神经调控奠定了基础。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737755-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1209, \"height\": 769, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737755-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1205, \"height\": 1062, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737755-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1319, \"height\": 671, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737755-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1221, \"height\": 1108, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737755-v1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1339, \"height\": 890, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737755-v1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1346, \"height\": 683, \"label\": \"Figure\"}]"
motivation: 现有方法难以从全脑EEG水平估计状态依赖的有效连接，限制了对TMS诱发活动传播机制的理解。
method: 推导闭式表达拟合静息态EEG谱以推断局部参数，再基于少量TMS-EEG trials估计刺激位点特异性有效连接，构建生成式全脑模型。
result: 模型准确预测未见过TMS-EEG试次的诱发电位时空结构，且组级有效连接模板可复现个体早期响应模式。
conclusion: 建立了可解释的个体化全脑建模框架，为基于模型的神经调控提供了分析工具。
---

## 摘要
系统神经科学的一个主要挑战是理解外部扰动如何与持续的大脑活动相互作用。经颅磁刺激（TMS）在基础与临床神经科学中应用日益广泛，常与脑电图（EEG）联合使用，为探究这种相互作用提供了独特机会。然而，内在动力学如何约束TMS诱发电活动的传播仍知之甚少。特别是，有效连接（EC）——捕捉脑区间有向的、状态依赖的相互作用——被认为对扰动传播起关键塑造作用，但在全脑EEG层面仍难以估计。本文引入了一个解析可处理、生成式的全脑模型，将自发EEG活动与扰动下的皮层响应联系起来。通过推导模型交叉谱密度的闭式表达式，我们直接拟合经验静息态EEG谱，并无需时域模拟即可推断出具有生物物理可解释性的局部动力学参数。随后，我们仅利用少量TMS-EEG试验数据估计出刺激位点特异性的有效连接。所得模型能准确预测未见试验中TMS诱发电位（TEP）的时空结构。此外，即使不进行个体特异性重新拟合，群体水平的有效连接模板也能捕捉单被试早期TMS响应中典型的位点特异性传播模式。综上，我们的结果为TMS-EEG的个体化全脑建模建立了一个分析框架，并具有应用于基于模型的神经调控的潜力。

## Abstract
A major challenge in systems neuroscience is understanding how external perturbations interact with ongoing brain activity. Transcranial magnetic stimulation (TMS), increasingly used in both basic and clinical neuroscience and often combined with electroencephalography (EEG), provides a unique opportunity to probe this interaction. However, how intrinsic dynamics constrain the propagation of TMS-evoked activity remains poorly understood. In particular, effective connectivity (EC)--capturing directed, state-dependent interactions between brain regions--is thought to critically shape perturbational spread, yet remains difficult to estimate at the whole-brain EEG level. Here we introduce an analytically tractable, generative whole-brain model that links spontaneous EEG activity to cortical responses under perturbation. By deriving a closed-form expression for the model's cross-spectral density, we directly fit empirical resting-state EEG spectra and infer biophysically interpretable local dynamical parameters without time-domain simulations. We then estimate stimulation-site-specific EC using only a small fraction of the TMS-EEG trials. The resulting model accurately predicts the spatiotemporal structure of TMS-evoked potentials (TEPs) in unseen trials. Moreover, even without subject-specific refitting, group-level EC templates capture canonical site-specific propagation motifs underlying single-subject early TMS responses. Together, our results establish an analytical framework for individualized whole-brain modeling of TMS-EEG with potential applicability to model-based neuromodulation.