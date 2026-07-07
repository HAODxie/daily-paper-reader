---
title: Network and hierarchical organization of intrinsic timescales in the human brain
title_zh: 人脑内在时间尺度的网络与层级组织
authors: "Krause, B. M., Bublitz, E. F., Dappen, E. R., Kawasaki, H., Nourski, K. V., Banks, M. I."
date: 2026-07-02
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.01.735904v1.full.pdf"
tags: ["query:neuro-mental"]
score: 6.0
evidence: 使用iEEG和fMRI分析内在时间尺度
tldr: 大脑内在神经时间尺度反映信息维持时长，先前研究显示其沿皮质层级变化。本研究利用人类颅内脑电图记录，通过扩散图嵌入定义层级位置，提取非周期成分估计时间尺度。结果发现时间尺度从感觉区到联合区单调增加，且网络枢纽节点最长。睡眠期间层级组织消失，感觉区时间尺度显著增加。该工作建立了时间尺度、皮质层级与网络拓扑的直接联系，并揭示脑状态对层级组织的动态调制。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究皮质层级中神经时间尺度的组织规律及其与网络拓扑的关系，以及睡眠如何调制这种层级组织。
method: 采集46名患者静息态iEEG，利用扩散图嵌入映射记录点位层级，通过频谱参数化提取非周期成分计算时间尺度。
result: 时间尺度随层级单调增加；枢纽节点和强连通区域时间尺度更长；睡眠中层级梯度在REM和深睡期消失，感觉区时间尺度增多。
conclusion: 神经时间尺度的层级组织由网络拓扑支撑，并受脑状态动态调控，为理解大脑多时间尺度信息处理提供新视角。
---

## 摘要
内在神经时间尺度表征信息在神经回路中维持的特征持续时间。证据表明，神经时间尺度在皮层层级中系统性地变化，初级感觉区域时间尺度较短，而高级联合区域时间尺度较长。以往研究中，层级被定义为分类性的、解剖性的，或基于扩散图嵌入（DME）导出的静息态fMRI功能连接的主梯度。在此，我们通过将个体颅内脑电图（iEEG）记录位点的MNI坐标投影到该嵌入空间（来自人类连接组计划静息态fMRI数据）来分配其层级位置。我们从成年神经外科患者（n=46，25名女性）的静息态iEEG记录中，通过频谱参数化提取局部场电位功率谱的非周期性成分，从而估计神经时间尺度。时间尺度随层级位置单调递增，并与从参与者iEEG功能连接的DME导出的两个感兴趣区域（ROI）级网络拓扑度量相关：平均功能连接更强的ROI表现出更长的时间尺度，作为枢纽（定义为靠近嵌入空间中心）的ROI也是如此。最后，时间尺度随睡眠阶段变化，非快速眼动（NREM）期间最慢，清醒和快速眼动（REM）期间最快。清醒和N1睡眠期间的层级梯度在REM、N2和N3睡眠中不再被检测到，这是由于层级较低水平的时间尺度选择性增加所致。这项工作提出了一种可应用于iEEG数据的层级新度量，建立了人iEEG中神经时间尺度、皮层层级和网络拓扑之间的直接联系，并证明了这种层级组织受大脑状态动态调节。

意义声明大脑同时在多个时间尺度上处理信息，不同皮层区域专门负责快速感觉处理或缓慢情境整合。我们从人类颅内电生理记录中测量了内在神经时间尺度，并应用一种新方法将每个记录位点沿皮层层级定位。时间尺度从感觉区到联合区系统性地增加，在网络枢纽（即与大脑其他部分均匀广泛连接的区域）中最长。在睡眠期间，这种层级组织未被检测到，感觉区时间尺度增加最多。这些发现促进了我们对大脑时间组织如何由网络架构塑造并受大脑状态调节的理解。

## Abstract
Intrinsic neural timescales represent the characteristic duration over which information is maintained in neuronal circuits. Evidence suggests that neural timescales vary systematically across the cortical hierarchy, with shorter timescales in primary sensory areas and longer timescales in higher-order association regions. In previous studies, hierarchy has been defined categorically, anatomically, or from the principal gradient of resting-state fMRI functional connectivity derived using diffusion map embedding (DME). Here, we assign hierarchical position to individual human intracranial electroencephalography (iEEG) recording sites by projecting their MNI coordinates onto this embedding space, derived from Human Connectome Project resting-state fMRI data. We estimated neural timescales from resting-state iEEG recordings in adult neurosurgical patients (n=46, 25 female) by extracting the aperiodic component of the local field potential power spectrum using spectral parameterization. Timescales increased monotonically with hierarchical position and associated with two region of interest (ROI)-level measures of network topology derived from DME of participants iEEG functional connectivity: ROIs with stronger mean functional connectivity exhibited longer timescales, as did ROIs functioning as hubs, defined by proximity to the center of embedding space. Finally, timescales varied with sleep stage, with slowest values during NREM and fastest during wake and REM. The hierarchical gradient present during wake and N1 was no longer detected during REM, N2, and N3 sleep, driven by a selective increase in timescales at lower levels of the hierarchy. This work presents a novel metric of hierarchy that can be applied to iEEG data, establishes a direct link between neural timescales, cortical hierarchy, and network topology in human iEEG, and demonstrates that this hierarchical organization is dynamically modulated by brain state.

Significance StatementThe brain processes information across multiple timescales simultaneously, with different cortical regions specialized for fast sensory processing or slow integration of context. We measured intrinsic neural timescales from human intracranial electrophysiological recordings and applied a novel method to locate each recording site along the cortical hierarchy. Timescales increased systematically from sensory to association areas, and were longest in network hubs, i.e., regions that are uniformly and widely connected to the rest of the brain. During sleep, this hierarchical organization was not detected, with sensory areas showing the largest increases in timescale. These findings advance our understanding of how the brains temporal organization is shaped by network architecture and modulated by brain state.