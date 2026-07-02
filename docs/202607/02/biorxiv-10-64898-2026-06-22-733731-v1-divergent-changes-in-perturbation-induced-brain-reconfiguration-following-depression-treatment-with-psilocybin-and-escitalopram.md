---
title: Divergent changes in perturbation-induced brain reconfiguration following depression treatment with psilocybin and escitalopram
title_zh: 裸盖菇素和艾司西酞普兰治疗抑郁症后扰动诱发的大脑重构的变化差异
authors: "Dagnino, P. C., Acero-Pousa, I., Carhart-Harris, R., Erritzoe, D., Nutt, D. J., Kringelbach, M. L., Sanz Perl, Y., Deco, G."
date: 2026-06-26
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.22.733731v1.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 使用fMRI研究抑郁症治疗，比较裸盖菇素和艾司西酞普兰
tldr: 抑郁症治疗后的全脑组织重组机制尚不明确。本研究构建治疗前后静息态fMRI全脑模型，通过系统局部扰动和重新优化获取反应性有效连接，并计算网络重组指数。结果发现裸盖菇素增加全局重组，艾司西酞普兰降低重组，且重组指数与层级动态脑区相关。扰动诱导的脑重组指数可作为区分不同抗抑郁干预神经可塑性的新指标。
source: biorxiv
selection_source: fresh_fetch
motivation: 探索裸盖菇素与艾司西酞普兰治疗抑郁症后全脑组织在扰动下的重组差异，揭示神经可塑性变化。
method: 基于治疗前后静息态fMRI构建全脑模型，施加系统局部扰动并重新优化，计算反应性有效连接和网络重组指数。
result: 裸盖菇素增加全局脑网络重组指数，艾司西酞普兰降低；重组指数与层级动态脑区相关。
conclusion: 扰动诱导的脑重组指数可揭示不同抗抑郁干预的神经变化，裸盖菇素促进灵活性，艾司西酞普兰稳定化。
---

## 摘要
神经科学的一个核心挑战是理解人脑如何组织以支持最佳功能和适应性。表征复杂大脑动态的一种方法是通过人工扰动全脑模型。在此，我们探究了在重度抑郁症（MDD）中，经裸盖菇素和艾司西酞普兰干预后，扰动下的全脑组织是否发生变化。首先，我们构建了治疗前后静息态功能磁共振成像（fMRI）的全脑模型，并为每个个体获得初始生成有效连接（GEC）矩阵。然后，我们系统地施加不同强度的局部人工扰动，重新优化每个模型以生成响应GEC（GECr），并通过量化脑网络重构指数（NRI）来评估大脑重构的程度。结果显示，全球脑NRI在裸盖菇素治疗后增加，而在艾司西酞普兰治疗后减少。不同阶段和干预措施中，较高的全球NRI与协调大脑层级动态的脑区局部扰动相关。传统方法补充了我们的研究。我们的发现表明，MDD每种治疗后神经变化不同。裸盖菇素后扰动诱发的脑重构增加与更大的脑灵活性和可变性一致，而艾司西酞普兰后的减少则表明脑动态更稳定。总体而言，扰动诱发的脑NRI可能代表一种揭示抑郁症不同干预后神经变化的有用方法。

## Abstract
A central challenge in neuroscience is understanding how the human brain is organised to support optimal functioning and adaptability. One approach to characterise complex brain dynamics is by artificially perturbing whole-brain models. Here, we asked whether whole-brain organisation under perturbation in major depressive disorder (MDD) changes after intervention with psilocybin and escitalopram. First, we built whole-brain models of pre- and post-treatment resting-state functional magnetic resonance imaging (fMRI) and obtained an initial generative effective connectivity (GEC) matrix for each individual. Then, we employed systematic and local artificial perturbations across intensities, re-optimised each model to create a response GEC (GECr), and assessed the extent of brain reorganisation by quantifying the brain network reconfiguration index (NRI). Our results showed that the global brain NRI increases with psilocybin and decreases with escitalopram. Across sessions and interventions, higher global NRI was related with localised perturbations in brain areas orchestrating the brains hierarchical dynamics. Traditional approaches complemented our investigation. Our findings suggest distinct neural changes following each treatment for MDD. The increase in brain reorganisation under perturbation following psilocybin is consistent with greater brain flexibility and changeability, whereas the decrease following escitalopram suggests more stabilised brain dynamics. Overall, perturbation-induced brain NRI may represent a useful approach for uncovering neural changes following different interventions for depression.

---

## 论文详细总结（自动生成）

# 论文详细总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：理解人脑如何组织以支持最佳功能和适应性，特别是重度抑郁症（MDD）患者在接受不同治疗后，大脑在扰动下的重组能力是否发生差异变化。
- **背景**：MDD是一种高负担神经精神疾病，治疗困难。已有研究表明裸盖菇素（psilocybin）和艾司西酞普兰（escitalopram）都能改善抑郁症状，但神经机制可能不同：裸盖菇素与大脑灵活性、可塑性增加相关，而艾司西酞普兰与情绪钝化、稳定性增加相关。目前缺乏直接比较两种治疗后大脑在扰动下重组能力的定量指标。
- **整体含义**：通过量化“扰动诱发的脑网络重组指数（NRI）”，揭示不同抗抑郁干预的神经可塑性差异，为理解治疗机制提供新视角。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：构建全脑模型，施加系统局部扰动，然后重新优化模型以“抵抗”扰动，通过比较初始模型与响应模型的相似性（去相关）来量化网络重组程度。NRI越高，表示大脑在扰动下重组越强。
- **关键技术细节**：
  - **全脑模型**：使用Stuart-Landau振荡器（Hopf模型）表示每个脑区（DK80分区：62个皮层+18个皮层下区域），并结合结构连接（SC）和功能连接（FC）生成有效连接（GEC）矩阵。
  - **GEC优化**：基于热力学“时间箭头”概念，通过迭代调整连接强度，使模型拟合经验fMRI数据，得到初始GEC。
  - **扰动与再优化**：对每个脑区独立施加不同强度（0.02-0.10，步长0.01）的高斯噪声扰动（其他脑区保持0.01），然后重新优化整个GEC（即响应GEC，GECr），使其尽可能接近初始模型输出。
  - **NRI计算**：计算GECr与初始GEC之间的去相关（1 - 相关系数），值越高表示重组越大。
- **流程步骤**：
  1. 从个体结构连接和功能连接构建全脑Hopf模型，优化得到初始GEC。
  2. 对每个脑区（i）和每个扰动强度（s），施加局部噪声，重新优化得到GECr(i,s)。
  3. 计算NRI(i,s) = 1 - corr(GECr(i,s), GEC)。
  4. 汇总平均得到全局NRI（所有脑区和强度平均）和区域NRI（每个脑区平均）。

## 3. 实验设计：使用了哪些数据集/场景，它的benchmark是什么，对比了哪些方法

- **数据集**：来自一项双盲II期随机对照试验（Carhart-Harris et al., 2021），包含22名裸盖菇素组（平均41.9岁）和20名艾司西酞普兰组（平均38.7岁）MDD患者。均接受了治疗前后闭眼静息态fMRI扫描。试验注册号：NCT03429075。
- **场景**：仅使用静息态fMRI数据，未涉及任务态或外部刺激。
- **Benchmark**：无明确的外部基准，但论文对比了两种治疗方法（裸盖菇素 vs 艾司西酞普兰）在治疗前后的NRI变化。
- **对比方法**：传统图论方法，包括：
  - **Cascone et al. (2021)**：按节点度降序移除节点，计算全局效率（GE）曲线下面积（AUC）。
  - **Kotlarz (2024)**：按介数中心性降序移除节点，计算最大簇大小（CS）和全局介数中心性（BC）的峰值距离。
  - 两种方法均在加权和二值化GEC矩阵上实施，并采用不同阈值（5%-100% top边）。

## 4. 资源与算力

论文**未明确说明**使用的GPU型号、数量、训练时长等算力细节。仅提及分析在MATLAB R2022a和R2024a上运行，使用了Brain Connectivity Toolbox和自定义代码。未提供硬件配置。

## 5. 实验数量与充分性

- **实验数量**：
  - 主要NRI分析：对两种治疗（psilocybin, escitalopram）× 两个时间点（治疗前、后）× 80个脑区 × 9个扰动强度（0.02-0.10） × 42名患者，总计约60,480个NRI值。
  - 传统方法分析：在加权和二值化GEC上执行，每个阈值（约20个）重复节点移除过程。
  - 区域NRI与扰动性（perturbability）的相关分析（使用先前研究的扰动性数据）。
- **充分性与客观性**：
  - 样本量较小（n=22和20），统计效力有限，但属于临床神经影像常用规模。
  - 使用了非参数置换检验（Wilcoxon符号秩检验，1000次置换）和FDR多重比较校正，统计方法合理。
  - 没有进行独立的交叉验证或外部数据集验证，所有结果来自同一试验，可能限制泛化性。
  - 论文未报告效应量或置信区间，但提供了个体轨迹（图2A）和标准差（图2B），透明度较好。

## 6. 论文的主要结论与发现

- **主要发现**：
  1. 全局NRI在裸盖菇素治疗后**显著增加**，在艾司西酞普兰治疗后**显著减少**（图2A-B）。效应在多数扰动强度（≥0.03）上显著。
  2. 区域NRI变化：裸盖菇素组几乎所有脑区NRI增加，艾司西酞普兰组几乎全部减少，且皮层下区域变化最突出。裸盖菇素组默认模式网络（DMN）变化明显，艾司西酞普兰组背侧注意网络（DAN）变化明显（图3A）。
  3. 区域NRI与脑区扰动性（反映非平衡动态层次组织能力）呈**显著正相关**（所有组和阶段）（图3B）。
  4. 传统图论方法结果一致：裸盖菇素后全局效率AUC在加权情况下降低（连接强度减弱），在二值化高阈值下增加（连接路径增多）；艾司西酞普兰结果相反。节点移除导致集群大小崩溃的距离在裸盖菇素后增加，艾司西酞普兰后减少（图5）。
- **结论**：裸盖菇素治疗促进了大脑在扰动下更强的重组能力（灵活性增强），而艾司西酞普兰治疗使大脑动态更稳定（重组减少）。两种临床改善可能通过不同的神经可塑性机制实现。

## 7. 优点：方法或实验设计上的亮点

- **创新性**：提出NRI作为量化扰动下脑网络重组能力的指标，区别于传统“敏感性”或“响应”测量，聚焦于系统在持续扰动下保持功能的能力。
- **方法论优势**：
  - 基于全脑Hopf模型，能合理模拟经验fMRI动态，且优化GEC利用了热力学“时间箭头”不对称性，捕捉信息流方向。
  - 扰动后重新优化模型以逼近初始状态，模拟了大脑“抵抗”扰动并维持原有组织的自然过程，比单纯移除节点或测量响应更贴近生理。
  - 不需要预先定义节点重要性排序，避免了主观偏差。
- **互补验证**：结合传统图论方法（节点移除）进行多角度验证，增强了结论的可靠性。
- **统计严谨**：使用非参数置换检验和FDR校正，控制多重比较错误。
- **可重复性**：代码可从作者处获得，数据可请求（但受限于原始试验伦理）。

## 8. 不足与局限

- **样本量小**：每组约20人，统计效力有限，可能存在对个体差异的敏感度不足。
- **缺乏独立验证**：所有分析基于同一临床试验数据，无外部数据集验证泛化性。
- **结构连接来自健康被试**：使用的SC矩阵来自健康人群，而非患者个体化数据，尽管优化过程有所缓解，但可能引入偏差。
- **脑分区选择**：使用DK80分区，不同分辨率或图谱可能影响结果，未进行跨图谱验证。
- **模型假设**：Hopf模型是线性化近似，可能无法完全捕捉非线性脑动力学；扰动方式（均匀加噪声）可能不反映真实生理扰动。
- **未报告效应量**：虽然显著，但未提供Cohen's d或类似指标，无法比较效应大小。
- **传统方法局限性**：节点移除方法在加权/二值化选择上高度依赖阈值，不同阈值下结果相反（如Cascone方法在高阈值时方向反转），解释需谨慎。
- **临床意义间接**：NRI变化与临床症状改善的直接关联未报道（论文侧重于机制而非临床结果）。

（完）
