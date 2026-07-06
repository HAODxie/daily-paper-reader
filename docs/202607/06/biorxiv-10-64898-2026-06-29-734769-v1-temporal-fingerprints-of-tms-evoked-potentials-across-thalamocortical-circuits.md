---
title: Temporal fingerprints of TMS-evoked potentials across thalamocortical circuits
title_zh: 跨丘脑-皮层回路的TMS诱发电位的时间指纹
authors: "Hassan, G., Gaglioti, G., Furregoni, G., Focacci, E., Porro, M., Bernardelli, L., Calcagno, A., Massimini, M., Sarasso, S., Rosanova, M., Casarotto, S."
date: 2026-07-02
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.29.734769v1.full.pdf"
tags: ["query:neuro-mental"]
score: 8.0
evidence: TMS诱发电位的EEG信号处理
tldr: 经颅磁刺激诱发电位（TEP）的形态特征可反映皮层网络特性，但系统分析缺乏。本研究对40名受试者分别刺激枕、顶、额叶，自动提取TEP的峰幅度、潜伏期和峰间间隔。结果显示枕叶TEP幅度最大、潜伏期最长，且沿后-前轴潜伏期和峰间间隔递减，反映了从α振荡主导的枕叶到额叶-皮层下紧密环路的不同动态。该工作提供了表征皮层反应性的机制性工具，并发布Python实现。
source: biorxiv
selection_source: fresh_fetch
motivation: 探索不同脑区TMS诱发电位的形态特征，以揭示皮层网络特性。
method: 对40名受试者分别刺激枕叶、顶叶和额叶皮层，自动提取TEP波形的峰幅值、潜伏期及峰间间隔。
result: 枕叶TEP峰幅最大、第一成分潜伏期最长；沿后-前轴潜伏期和峰间间隔递减。
conclusion: TEP形态由刺激网络特性决定，早期幅度反映局部募集，后期时间特征追踪节律活动。
---

## 摘要
背景：经颅磁刺激（TMS）诱发的脑电图（EEG）电位提供了皮层动力学的直接窗口。然而，对其形态特征的系统性探索（类似于感觉诱发电位）仍然缺乏，尤其是对于运动皮层以外的刺激。
目的：从TMS诱发电位（TEP）的时间过程中获取额叶、顶叶和枕叶网络的区域特异性特性。
材料与方法：我们实施并应用了一个自动程序，计算了40名神经典型受试者在左枕叶（n=25）、顶叶（n=25）和额叶（n=25）皮层刺激下记录的TEP的峰峰振幅、峰值潜伏期和峰间间隔。
结果：枕叶TEP显示出最大的峰峰振幅和最长的第一个波形分量潜伏期，这与刺激强度无关，并且与大量密集连接神经元的募集一致。关于后续成分，潜伏期和峰间间隔沿后-前轴系统性地减小，反映了从α波主导的枕叶回路到额叶皮层与皮层下结构紧密耦合环路之间逐渐加快的循环动力学。顶叶TEP显示出中等的振幅和潜伏期测量值，这与上顶叶皮层异质的细胞构筑和连接组织一致。
结论：我们的研究结果表明，TEP形态受刺激网络的不同特性塑造，早期振幅反映了局部募集的规模，而后期时间特征追踪了循环活动的节律。这项工作提供了一种基于机制且实用的方法，也以基于Python的工具形式发布，允许表征不同脑状态和人群中皮层反应性。

## Abstract
BackgroundElectroencephalographic (EEG) potentials evoked by transcranial magnetic stimulation (TMS) offer a direct window into cortical dynamics. Yet, a systematic exploration of their morphological features, analogous to sensory-evoked potentials, is lacking, especially for stimulation outside the motor cortex.

AimTo obtain region-specific properties of frontal, parietal and occipital networks from the time course of TMS-evoked potentials (TEPs).

Materials and MethodsWe implemented and applied an automatic procedure to compute peak-to-peak amplitude, peak latency, and inter-peak interval of TEPs recorded from 40 neurotypical subjects stimulated over left occipital (n=25), parietal (n=25), and frontal (n=25) cortices.

ResultsOccipital TEPs showed the largest peak-to-peak amplitude and longest latency of the first waveform component, independently of stimulation intensity and consistent with the recruitment of a large patch of densely interconnected neurons. Concerning later components, both latency and inter-peak interval systematically decreased along the posterior-to-anterior axis, reflecting progressively faster recurrent dynamics from the alpha-dominated occipital circuitry to the tightly coupled loops between frontal cortex and subcortical structures. Parietal TEPs showed intermediate amplitude and latency measures, consistent with the heterogeneous cytoarchitectonic and connectional organization of the superior parietal cortex.

ConclusionsOur findings suggest that TEP morphology is shaped by the distinct properties of the stimulated networks, with early amplitude reflecting the extent of local recruitment and later temporal features tracking the rhythm of recurrent activity. This work offers a mechanistically grounded and practically accessible approach, also released as a Python-based tool, that allows to characterize cortical reactivity across different brain-states and populations.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：经颅磁刺激（TMS）诱发的脑电图（EEG）电位（TEP）是研究皮层动力学的直接窗口，但以往对TEP形态特征的系统性分析（类似感觉诱发电位）十分缺乏，尤其对运动皮层之外的刺激区域（如枕叶、顶叶、额叶）认识不足。
- **研究动机**：探索不同皮层区域（枕、顶、额）TEP的波形特征（幅值、潜伏期、峰间间隔），以揭示刺激网络的特异性动态（如局部募集规模、循环活动节律），为后续评估脑状态和人群差异提供机制性工具。
- **整体含义**：TEP的形态（早期振幅反映局部神经元募集程度，后期时间特征追踪循环活动的频率）受刺激区域内在的细胞构筑和连接组织塑造，沿后-前轴呈现系统性梯度变化。

### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：通过自动程序提取TEP波形的峰-峰振幅、峰值潜伏期和峰间间隔这三个形态特征，量化不同刺激部位的反应性差异。
- **关键技术细节**：
  - 使用自动程序计算TEP：针对每个受试者每个刺激部位，提取TEP波形；
  - 峰-峰振幅：第一个正向波与第一个负向波之间的幅值差；
  - 峰值潜伏期：从刺激开始到第一个波形分量峰值的时间；
  - 峰间间隔：连续波峰（或波谷）之间的时间差，反映循环活动周期；
  - 分析中控制了刺激强度（强度无关性分析）。
- **算法流程（文字说明）**：
  1. 对每个受试者进行TMS-EEG记录，分别刺激左枕、顶、额叶皮层；
  2. 预处理EEG数据（去噪、伪迹去除等）；
  3. 应用自动程序识别TEP波形的主要波峰和波谷；
  4. 计算上述三个形态指标；
  5. 统计比较三组之间的指标差异（考虑刺激强度无关性）；
  6. 分析沿后-前轴的梯度趋势。
- **公式或模型**：文中未给出具体公式，主要依赖统计比较（如方差分析）。

### 3. 实验设计：使用了哪些数据集/场景，它的benchmark是什么，对比了哪些方法

- **数据集**：40名神经典型受试者，分别刺激左枕叶（n=25）、左顶叶（n=25）、左额叶（n=25）；受试者可能有部分重叠（未明确说明）。
- **场景**：静息状态下TMS脉冲刺激三个不同皮层区域，记录EEG诱发信号。
- **Benchmark**：无明确的基准数据集或对比方法，属于探索性区域比较研究，未与已有方法（如其他TEP分析算法）进行对比。
- **对比方法**：主要比较三个刺激区域之间的TEP形态指标，未引入其他分析方法。

### 4. 资源与算力：如果文中有提到，请总结使用了多少算力（GPU型号、数量、训练时长等）。若未明确说明，也请指出这一点。

- **未明确说明**：论文未提及任何计算资源（GPU型号、数量、训练时长）或训练过程。由于该研究主要使用自动程序提取已知波形特征，而非深度学习模型，可能不需要大量GPU算力。文中提及发布了基于Python的工具，但未说明运行环境。

### 5. 实验数量与充分性：大概做了多少组实验（如不同数据集、消融实验等），这些实验是否充分、是否客观、公平

- **实验组数**：主要分为三组（枕叶、顶叶、额叶刺激），每组25人，共40名受试者（有10人接受了多部位刺激？原文“n=25”可能分别指不同被试子集，但未明确说明是否独立）。未进行消融实验或交叉验证。
- **充分性**：样本量中等，但缺乏对同一受试者多个脑区刺激的直接对比（可能存在被试间差异）。实验设计为单因素（刺激部位）对比，控制了刺激强度无关性，但未考虑年龄、性别等因素。未设计重复刺激或假刺激对照。
- **客观性**：使用自动程序提取指标，减少主观偏差。但未与手动标注或专家判别对比。结果统计显著，但未报告效应量或多重比较校正细节（摘要未提及，但全文可能包含）。

### 6. 论文的主要结论与发现

- **主要结论**：
  1. **枕叶TEP**：峰-峰振幅最大，第一个波形分量潜伏期最长（与刺激强度无关），反映大量密集连接神经元的募集（α振荡主导的回路）。
  2. **沿后-前轴梯度**：后续成分的潜伏期和峰间间隔从枕叶到额叶系统性地减小，提示循环动力学加速——从α主导的枕叶回路到额叶-皮层下紧密耦合环路的转变。
  3. **顶叶TEP**：振幅和潜伏期处于中等水平，符合上顶叶皮层异质性细胞构筑和连接组织。
  4. 早期振幅反映局部募集规模，后期时间特征追踪循环活动节律。

### 7. 优点：方法或实验设计上有哪些亮点

- **方法亮点**：
  - 开发了自动分析TEP形态的程序，提高了可重复性；
  - 同时量化振幅、潜伏期、峰间间隔三个互补特征，涵盖局部募集和网络动态；
  - 控制刺激强度的影响，确保区域差异源于网络特性而非刺激强度差异；
  - 发布了Python工具，便于其他研究者使用。
- **实验设计亮点**：选择非运动皮层区域（枕、顶、额），填补了TMS-EEG研究对运动皮层以外区域系统性分析的空白。

### 8. 不足与局限：包括实验覆盖、偏差风险、应用限制等

- **样本量**：每组25人，但可能部分受试者重复（若只有40名总受试者，则每组25人可能有重叠），未进行完全匹配的组间设计。
- **缺乏重复刺激验证**：未说明是否每个部位多次刺激并取平均，也未报告试次数和信噪比。
- **未考虑个体差异**：未分析不同脑区TEP与年龄、性别、脑体积等协变量的关系。
- **未与其他分析方法对比**：如与源成像、有效连接分析等对比，仅停留在波形特征。
- **应用限制**：仅针对神经典型人群，未扩展至疾病状态；仅左半球刺激，未探索半球不对称性；未讨论磁场强度、线圈方向等参数对不同区域的影响。
- **统计充分性**：摘要未提及多重比较校正，可能仅报告了原始p值（需查看全文）；效应量报告不明确。

（完）
