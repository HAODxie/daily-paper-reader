---
title: Time space signatures of hybrid search resolution using EEG and eye movements concurrent recordings
title_zh: 基于EEG和眼动同步记录的混合搜索解析的时空特征
authors: "Care, D., Gonzalez, J. E., Ison, M. J., Kamienkowski, J. E."
date: 2026-06-28
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.22.733836v1.full.pdf"
tags: ["query:neuro-mental"]
score: 7.0
evidence: 利用EEG和眼动追踪分析混合视觉搜索
tldr: 自然环境中视觉搜索需要注意与记忆协同，但传统事件相关方法无法分离重叠神经信号。本研究采用去卷积方法分析同步EEG和眼动数据，从假设驱动到数据驱动建模，成功提取了目标检测的P300成分，并发现漏检也引发较弱响应。模型随复杂度增加保持稳定，为揭示自由观看中注意与记忆的动态交互提供了有效工具。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统事件相关方法无法分离自然场景中重叠的神经信号，阻碍对生态效度下注意与记忆协同过程的研究。
method: 对同步记录的EEG和眼动数据采用去卷积方法，从假设驱动模型扩展到数据驱动模型，并利用方差膨胀因子控制模型复杂度。
result: 成功提取目标检测的P300成分，漏检引发类似但较弱的响应；模型性能随特征空间扩大保持稳定，交互效应被有效探索。
conclusion: 去卷积方法结合模型评估指标能有效分离自由观看中注意与记忆的时空动态，为自然场景认知研究提供新范式。
---

## 摘要
理解大脑如何在自然环境中支持视觉搜索——其中注意和记忆必须协同工作以在干扰物中找到目标——需要分析神经信号，这些信号中响应在时间上重叠且多个环境变量同时交互。传统的事件相关方法无法分离这些重叠信号，从而在生态有效场景下研究认知时造成了根本性瓶颈。在此，我们试图在自然场景下的混合视觉和记忆搜索任务中分离激活模式。我们证明，基于反卷积的方法应用于共配准的EEG和眼动追踪数据解决了这一问题，捕捉到了主效应及其交互作用的时间响应函数（TRF）中的精细激活模式。从假设驱动模型出发，我们在自由眼动的混合搜索任务中复制了视觉处理和目标检测的已知成分。此外，将我们的方法扩展到层次更大的数据驱动模型，使我们能够探索先前被分别研究的效应之间的交互作用。我们发现，随着模型复杂度的增加，TRF估计保持稳定，这得益于模型性能（皮尔逊相关系数）的提升，并由方差膨胀因子（VIF）控制。我们识别出一个与目标检测的P300成分一致的晚期激活，并揭示了漏检引发了相似但较弱的响应，表明其作用比简单检测更为微妙。这些发现展示了反卷积方法，辅以支持其在特征空间扩展的稳健模型性能度量，如何揭示自由观看行为背后的注意和记忆过程的动态相互作用。

## Abstract
Understanding how the brain supports visual search in naturalistic environments--where attention and memory must work together to find targets among distractors--requires analysing neural signals where responses overlap in time and multiple environmental variables simultaneously interact. Conventional event-related methods cannot disentangle these overlapping signals, creating a fundamental bottleneck for studying cognition in ecologically valid settings. Here, we seek to isolate activation patterns during a hybrid visual and memory search task in naturalistic scenarios. We show that our deconvolution-based approach applied to coregistered EEG and eye-tracking data resolves this problem, capturing fine-grained activation patterns in the temporal response functions (TRFs) for main effects and their interactions. Starting from hypothesis-driven models, we replicated established components for visual processing and target detection in a Hybrid Search task with unrestricted eye movements. Moreover, extending our approach to hierarchically larger data-driven models enabled us to explore interactions between the effects that have otherwise been studied separately. We showed that the TRF estimates remained stable with increasing model complexity, supported by improved model performance (Pearsons correlation coefficient) and controlled by the variance inflation factor (VIF). We identified a late activation consistent with the P300 component for target detection, and revealed that missed detections elicited similar but weaker responses, suggesting a more nuanced role than simple detection. These findings demonstrate how deconvolution methods, complemented with robust measures of model performance that support its expansion in features space, can uncover the dynamic interplay of attention and memory processes underlying free-viewing behavior.