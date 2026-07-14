---
title: Diffusion Latent Representations for Neural Decoding
title_zh: 用于神经解码的扩散潜在表示
authors: "Wong, B., Laschowski, B."
date: 2026-07-13
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.08.737343v1.full.pdf"
tags: ["query:neuro-mental"]
score: 8.0
evidence: 扩散潜表示用于神经语音解码
tldr: "神经解码可视为将神经活动映射到中间表示再重建的过程，中间表示的选择显著影响性能与学习难度。本文提出通用框架系统研究中间表示选择的影响，并以扩散潜表示为实例，在神经语音解码任务中比较不同扩散时间步的表征效果。实验表明，教师强制词错误率从44.7%降至3.5%，揭示了扩散潜表示的有效性高度依赖于特定时间步。该框架为优化中间表示提供了系统性基础。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-08-737343-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1864, \"height\": 1043, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-08-737343-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1837, \"height\": 1094, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-08-737343-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 931, \"height\": 193, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-08-737343-v1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 929, \"height\": 159, \"label\": \"Table\"}]"
motivation: 现有神经解码方法未系统探究中间表示对下游重建的影响，本文旨在建立框架以明确这一关键因素。
method: 采用不同扩散时间步的潜表示作为中间表征，在神经语音解码任务上逐组件评估重建性能。
result: "教师强制词错误率随扩散时间步变化显著，最优模型达3.5%，最差为44.7%。"
conclusion: 扩散潜表示适用于神经解码，但效果高度依赖时间步选择，所提框架可推广至其他领域。
---

## 摘要
神经解码可被视为一个表示学习问题，其中神经活动在下游重建之前被映射到中间表示。中间表示的选择影响性能和学习的难度。本文开发了一个新框架，用于研究中间表示选择如何影响下游学习和重建。作为概念验证，我们使用从不同扩散时间步提取的扩散潜在表示进行神经语音解码，实例化该框架。逐分量评估显示，不同扩散时间步的重建性能存在显著差异，不同潜在模型的教师强制词错误率分别为44.7%、7.5%和3.5%。这些结果表明，扩散潜在表示可以作为从神经活动中学习的有效中间表示，但其有效性强烈依赖于所选的扩散时间步。更广泛地，我们的框架为系统研究中间表示选择如何影响下游学习和重建提供了基础。

## Abstract
Neural decoding can be viewed as a representation learning problem in which neural activity is mapped into an intermediate representation before downstream reconstruction. The choice of intermediate representation influences both performance and learning difficulty. Here we developed a novel framework for studying how intermediate representation choice influences downstream learning and reconstruction. As a proof-of-concept, we instantiated our framework using diffusion latent representations extracted from different diffusion timesteps for neural speech decoding. Component-wise evaluation showed that reconstruction performance differed substantially across diffusion timesteps, with teacher-forced Word Error Rates of 44.7%, 7.5%, and 3.5% for different latent models. These results demonstrate that diffusion latent representations can serve as effective intermediate representations for learning from neural activity, but that their effectiveness depends strongly on the selected diffusion timestep. More broadly, our framework provides a basis for systematically studying how intermediate representation choice influences downstream learning and reconstruction.