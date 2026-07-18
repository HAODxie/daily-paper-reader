---
title: Edge controllability is associated with treatment response to repetitive transcranial magnetic stimulation in depression.
title_zh: 边缘可控性与抑郁症重复经颅磁刺激治疗反应的相关性
authors: "Dey, S."
date: 2026-07-17
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.11.737986v1.full.pdf"
tags: ["query:neuro-mental"]
score: 8.0
evidence: 脑网络控制理论应用于抑郁症治疗反应
tldr: "重复经颅磁刺激（rTMS）治疗抑郁症（MDD）的疗效存在个体差异。本文采用网络控制理论，首次从边的可控性角度分析结构连接组与rTMS疗效的关系。对25名难治性抑郁患者治疗前弥散MRI构建结构连接组，计算基于边的可控性指标。发现额中回与多个脑区（上额回、海马、角回、眶回）之间的边可控性与HAMD-24评分变化显著相关（r=0.470-0.597, p<0.05）。研究提示边可控性可捕获与治疗反应相关的环路特性，有助于个性化神经调控策略。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-11-737986-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 826, \"height\": 1494, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-11-737986-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 819, \"height\": 1514, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-11-737986-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1874, \"height\": 281, \"label\": \"Table\"}]"
motivation: rTMS疗效个体差异大，先前网络控制研究多关注节点层面，边层面可控性是否关联治疗反应尚不清楚。
method: 25名难治性抑郁患者治疗前弥散MRI构建结构连接组（Destrieux图谱），计算基于边的可控性指标，分析其与高频rTMS（靶向背外侧前额叶）5周后HAMD-24评分变化的关系。
result: "额中回与上额回、海马、角回、眶回之间的边可控性与HAMD-24评分变化显著相关（r=0.470-0.597, p<0.05）。"
conclusion: 边可控性可捕获与rTMS疗效相关的环路特性，为个性化神经调控提供潜在生物标记。
---

## 摘要
重复经颅磁刺激（rTMS）是治疗重度抑郁障碍（MDD）的既定方法，但治疗反应的变异性仍然是一个重大挑战。网络控制理论提供了一个量化大脑网络如何促进状态转换的框架，但以往工作主要关注节点层面指标。本研究探讨了结构连接组的边缘可控性是否与rTMS结果相关。25名难治性抑郁症患者在为期5周的高频rTMS治疗（靶向背外侧前额叶皮层）前接受了弥散MRI扫描。使用MRtrix3和Destrieux图谱构建结构连接组，并计算基线时的边缘可控性指标。特定以中央额回为中心的边缘的可控性与HAMD-24评分变化显著相关，包括与额上回、海马、角回和眶回的连接（r = 0.470 - 0.597, p < 0.05）。这些发现表明，边缘可控性捕捉了与治疗反应相关的回路层面特性，并可能为个性化神经调控策略提供信息。

## Abstract
Repetitive transcranial magnetic stimulation (rTMS) is an established treatment for major depressive disorder (MDD), yet variability in treatment response remains a significant challenge. Network control theory provides a framework to quantify how brain networks facilitate state transitions, but prior work has focused primarily on node level metrics. Here, we investigate whether edge based controllability of the structural connectome is associated with rTMS outcomes. Twenty five patients with treatment-resistant depression underwent diffusion MRI prior to a 5 week course of high frequency rTMS targeting the dorsolateral prefrontal cortex. Structural connectomes were constructed using MRtrix3 and the Destrieux atlas, and edge based controllability metrics were computed at baseline. Controllability of specific middle frontal gyrus centered edges showed significant associations with changes in HAMD-24 scores, including connections to the superior frontal gyrus, hippocampus, angular gyrus, and orbital gyrus (r = 0.470 - 0.597, p < 0.05). These findings suggest that edge based controllability captures circuit level properties relevant to treatment response and may inform personalized neuromodulation strategies.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：重复经颅磁刺激（rTMS）是治疗重度抑郁障碍（MDD）的有效手段，但个体对治疗的反应差异很大，其原因尚不清楚。现有研究多从“节点”层面（脑区）分析网络控制性，但忽略了特定白质通路（边）的作用。本文旨在探索结构连接组中**基于边的可控性**是否与rTMS疗效相关。
- **背景意义**：网络控制理论认为大脑是一个动态系统，节点平均可控性反映低能量状态转换能力，节点模态可控性反映高能量转换能力。以往工作多聚焦节点，缺乏空间精度。将可控性分析从“节点”拓展到“边”，可以更精细地定位与治疗反应相关的神经回路，为个性化神经调控提供潜在生物标记。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：将结构连接组转化为边连接矩阵，定义边平均可控性和边模态可控性，量化每条白质纤维在促进全局状态转换中的能力。
- **关键技术细节**：
  - 结构连接组构建：使用Destrieux图谱（164个脑区），基于弥散MRI纤维追踪（MRtrix3），采用SIFT2加权，边权重为标准化后的纤维数量。
  - 边连接矩阵：从节点邻接矩阵 \( W_a \) 导出边邻接矩阵 \( W_{ae} \)，维度为 \( 0.5 \times n \times (n-1) \)（n=164时，边数为13366）。
  - 边平均可控性：由边格拉姆矩阵 \( G_e \) 的迹计算：\( \text{trace}(G_e) \)，其中 \( G_e = \sum_{p=0}^\infty W_{ae}^p W_{be} W_{be}^\top W_{ae}^p \)。
  - 边模态可控性：基于边特征向量 \( o_{eij} \) 和特征值 \( \lambda_j(W_{ae}) \) 计算：\( \phi_{e,i} = \sum_{j=1}^{N_e} (1 - \lambda_j^2(W_{ae})) o_{eij}^2 \)。
  - 分析策略：仅保留在所有被试中一致存在的边，且要求一条节点为左/右额中回（MFG）——因为rTMS靶点是左侧背外侧前额叶（dlPFC），而MFG是该区域的关键节点。

## 3. 实验设计：数据集、基准、对比方法

- **被试与数据集**：
  - 25名难治性抑郁患者（年龄21-68岁），来自Weill Cornell Medical College。
  - 每天接受10 Hz rTMS刺激左侧dlPFC，每周5天，持续5周。
  - 治疗前后使用24项汉密尔顿抑郁量表（HAMD-24）评估疗效；反应者定义为HAMD下降≥50%。
  - 基线时采集3T弥散张量成像（DTI）和T1结构像，治疗前后均采集，但本分析仅用基线数据。
- **基准与对比方法**：
  - 本文未设置外部对比方法（如节点可控性、其他图谱等），而是重点展示边可控性与HAMD变化的相关性。
  - 结果仅报告了4条显著相关的边（表1），并通过散点图展示相关趋势，区分响应者与非响应者。
- **分析方法**：Pearson相关，p<0.05（未校正多重比较）。

## 4. 资源与算力

- **未明确说明**：文中未提及使用任何GPU型号、数量、训练时长等计算资源信息。仅提到使用MRtrix3、FSL、FreeSurfer等软件在标准工作站上完成处理。

## 5. 实验数量与充分性

- **实验数量**：只有一组主要分析（25名被试，4条显著边缘相关），未进行交叉验证、独立重复或显著阈值校正（如FDR）。
- **充分性评价**：
  - **不足**：样本量较小（n=25），仅做皮尔逊相关，未控制多重比较（p值为未校正），存在假阳性风险。
  - 缺少消融实验（如对比节点可控性、随机置换检验等）及外部验证数据集。
  - 仅分析以MFG为中心的边缘，未全脑探索。
  - 结果仅报告了正向显著相关（r在0.47-0.60之间），未展示不显著或负相关结果，可能有报告偏倚。

## 6. 论文的主要结论与发现

- 基线时特定边（尤其连接额中回与额上回、海马、角回、眶回的边缘）的平均可控性与rTMS治疗后HAMD-24评分下降显著正相关。
- 边模态可控性与平均可控性遵循逆相关关系（满足能量景观假设），但未展示具体数值。
- 结论：基于边的可控性可能比节点可控性更精确地捕获与治疗反应相关的回路特性，有望指导个性化靶点选择。

## 7. 优点：方法或实验设计上的亮点

- **创新性**：首次将网络控制理论的“边可控性”概念应用于抑郁症rTMS疗效预测，而非传统节点分析。
- **理论深度**：从线性动力系统推导边控性格拉姆矩阵，并给出离散时间表示，数学基础扎实。
- **数据质量**：采用先进的弥散处理流程（降噪、Gibbs矫正、eddy、N4偏置场校正）、ACT纤维追踪、SIFT2权重校正，提高了连接组生物学准确性。
- **临床意义**：识别的特定回路（如额中回-海马、额中回-眶回）与抑郁症核心神经环路（情绪调节、奖赏处理）一致，具有合理性和可解释性。

## 8. 不足与局限

- **样本量与统计效力**：25名患者，统计效力低，未进行多重比较校正，显著结果可能为偶然发现。
- **缺乏独立验证**：未设置独立验证集或交叉验证，结果推广性存疑。
- **因果推断限制**：仅发现了相关，不能证明边可控性预测治疗效果或与机制有直接因果联系。
- **分析方法限制**：仅聚焦以MFG为中心的边缘，可能忽略其他重要环路；未与节点可控性定量比较以证明边指标的优越性。
- **技术限制**：弥散MRI追踪精度有限（尤其交叉纤维），结构连接组不能完全反映功能突触交互。
- **报告偏差**：仅展示显著结果，未全面报告所有检测边缘的数量和结果分布。

（完）
