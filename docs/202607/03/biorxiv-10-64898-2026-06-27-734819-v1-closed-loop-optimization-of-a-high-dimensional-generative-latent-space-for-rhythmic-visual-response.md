---
title: Closed-loop optimization of a high-dimensional generative latent space for rhythmic visual response
title_zh: 基于闭环优化的高维生成潜在空间实现节律性视觉响应
authors: "Livezey, J. A., Su, Y., Wolfer, S., Ingster, A., Klein, D. J., Hanina, A."
date: 2026-07-02
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.27.734819v1.full.pdf"
tags: ["query:neuro-mental"]
score: 6.0
evidence: 基于EEG的闭环脑机接口视觉调制
tldr: 神经振荡的闭环调制以往依赖侵入记录且聚焦发放率最大化。本文利用非侵入EEG测量SSVEP，在生成潜空间中优化图像刺激参数，实现alpha和theta频段节律性调制。在10-40维潜空间均优化成功，优化刺激可泛化至新参与者。低频空间功率反向驱动theta和alpha，证实闭环刺激优化是非侵入节律调制的可行方法。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有闭环调制视觉响应依赖侵入记录且仅优化发放率，缺乏非侵入节律性调制方法。
method: 通过非侵入EEG测量SSVEP，闭环优化生成潜空间图像刺激的闪烁频率以调制alpha/theta频段相对功率。
result: 在10-40维潜空间成功优化刺激，开环泛化至新参与者，低频空间功率反向调节theta和alpha。
conclusion: 闭环刺激优化是非侵入神经成像实现节律性神经调制的有效途径。
---

## 摘要
神经振荡伴随着广泛的认知状态和行为，包括感知、记忆和运动，调节神经振荡对于基础神经科学和临床研究日益重要。先前对视觉神经反应进行闭环调节的演示主要依赖于侵入性记录，并侧重于发放率最大化而非节律性调节。在此，我们展示了通过易于获取的非侵入性脑电图测量的稳态视觉诱发电位（SSVEP）的相对功率，可以在单次会话中对单个参与者根据图像刺激参数进行闭环调节。使用α和θ波段的闪烁频率在10、20和40维潜在空间中成功实现了刺激优化。我们还展示了优化后的刺激在开环呈现时能够泛化到新参与者。最后，我们表征了调节相对SSVEP功率的视觉特征，并发现图像中的低频空间功率以相反方向驱动θ和α波。总之，我们的结果表明，闭环刺激优化是一种利用非侵入性神经成像方法进行节律性神经调节的可行方法。

## Abstract
Neural oscillations accompany a wide range of cognitive states and behaviors including perception, memory, and movement, and modulating them is of growing interest for both basic neuroscience and clinical research. Previous demonstrations of closed-loop modulation of visual neural responses mainly relied on invasive recordings and focused on firing-rate maximization rather than rhythmic modulation. Here, we show that the relative power of steady-state visual evoked response (SSVEP), measured with readily-available, non-invasive electroencephalography, can be modulated in closed-loop as a function of image stimulus parameters for single participants within a single session. Stimulus optimization with flicker frequencies in the alpha and theta bands was successful in 10, 20, and 40 dimensional latent spaces. We also show that optimized stimuli generalize to new participants when shown in open-loop. Finally, we characterize the visual features that modulate relative SSVEP power and find that low-frequency spatial power in the image drives theta and alpha in opposite directions. Together, our results show that closed-loop stimulus optimization is a viable method for rhythmic neural modulation using noninvasive neuroimaging methods.