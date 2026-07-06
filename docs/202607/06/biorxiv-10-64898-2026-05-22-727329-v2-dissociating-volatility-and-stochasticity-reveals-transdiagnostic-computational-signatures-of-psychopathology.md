---
title: Dissociating volatility and stochasticity reveals transdiagnostic computational signatures of psychopathology
title_zh: 区分波动性和随机性揭示精神病理学的跨诊断计算特征
authors: "Fang, X., Piray, P."
date: 2026-07-05
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.22.727329v2.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 跨诊断的精神病理学计算特征
tldr: 自适应学习需区分环境波动性与随机性，二者对学习率要求相反且计算困难。研究通过计算建模识别三种表型：正常、随机性盲（将噪声当变化过度更新）和波动性盲（将变化当噪声更新不足）。在两个大样本、三个任务中，发现随机性盲与内化症状（焦虑、抑郁）相关，波动性盲与外部化症状（行为成瘾、强迫）相关，呈现双重分离。该发现支持学习缺陷的选择性而非一般性理论，为跨诊断精神病理学提供计算机制。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究个体在区分环境波动性与随机性上的计算差异是否与跨诊断精神病理学症状维度存在特定关联。
method: 通过计算建模拟合行为数据，识别三种学习表型（正常、随机性盲、波动性盲），并在两个大样本三个任务中分析其与内化/外部化症状的关系。
result: 随机性盲学习者在内化症状上得分更高，波动性盲学习者在外部化症状上得分更高，呈现双重分离。
conclusion: 精神病理学中的学习缺陷是选择性的，不同症状维度对应不同的不确定性推断失败。
---

## 摘要
适应性学习需要区分波动性（环境潜在状态的变化）和观测的逐时随机性。两者对学习速率要求相反：波动性需要更快的更新，而随机性则需要更慢的更新。在计算上区分它们很困难，因为两者都会膨胀经验方差，使得推断容易受到系统性个体差异的影响，进而可能对精神病理学产生影响。三种计算表型捕捉了这种变异：完整学习者；随机性盲学习者，他们将噪声视为变化而过度更新；以及波动性盲学习者，他们将变化视为噪声而更新不足。在两个大型在线样本和三个任务中，我们发现这些表型与跨诊断精神病理维度之间存在双重分离：随机性盲学习者在内化维度（焦虑、抑郁）上得分更高，而波动性盲学习者在内外化维度（行为成瘾、强迫性）上得分更高。因此，不同的症状维度对应着关于不确定性推断的不同失败，支持了精神病理学中不确定性下学习缺陷的选择性而非普遍性解释。

## Abstract
Adaptive learning requires distinguishing volatility, changes in the latent state of the environment, from moment-to-moment stochasticity of observations. The two demand opposite adjustments to the learning rate: volatility calls for faster updating, stochasticity for slower. Disentangling them is computationally difficult because both inflate experienced variance, leaving the inference prone to systematic individual differences with potential consequences for psychopathology. Three computational phenotypes capture this variation: intact learners; stochasticity-blind learners, who over-update by treating noise as change; and volatility-blind learners, who under-update by treating change as noise. In two large online samples and across three tasks, we found a double dissociation between these phenotypes and transdiagnostic psychiatric dimensions: stochasticity-blind learners scored higher on Internalizing (anxiety, depression), volatility-blind learners on Externalizing (behavioral addiction, compulsivity). Distinct symptom dimensions thus correspond to distinct failures of inference about uncertainty, supporting a selective rather than generalized account of learning-under-uncertainty deficits in psychopathology.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **研究动机**：自适应学习需要区分环境中的两类不确定性——波动性（volatility，潜在状态的变化）和随机性（stochasticity，观测的逐时噪声）。两者对学习率的要求相反：波动性需要加快更新，随机性需要减慢更新。然而，由于两者都膨胀经验方差，在计算上区分它们非常困难，容易产生系统性个体差异，并可能影响精神病理学。现有计算精神病学模型大多只关注波动性而忽略随机性，导致将个体差异可能错误地归因于“波动敏感性”。
- **整体含义**：本文通过联合推断波动性和随机性，识别出三种计算表型（intact、stochasticity-blind、volatility-blind），并发现它们与跨诊断症状维度（内化/外化）存在双重分离（double dissociation），支持了精神病理学中学习缺陷是选择性的而非一般性的观点。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程
- **核心思想**：基于贝叶斯框架同时推断波动性（v）和随机性（s），学习率应随波动性增加而增加、随随机性增加而减少。三种计算表型对应不同的归因失败：stochasticity-blind 将噪声误认为变化，导致高随机性下学习率升高；volatility-blind 将变化误认为噪声，导致高波动性下学习率降低。
- **关键技术细节**：
  - **实验1（连续任务）**：采用模型中性回归，在每个 block 内将信念更新 Δr_t 回归到预测误差 δ_t 上，回归系数即为该 block 的学习率。基线学习率、波动性效应、随机性效应分别通过 2×2 因子设计的对比计算。
  - **实验2（二元任务）**：采用 Categorical Bayes Filter (CBF) 结合 Hidden Markov Model (HMM)。HMM 描述了隐藏状态 x_t ∈ {0,1} 的二元扩散过程（波动性 v 控制状态切换概率）和观测 o_t ∈ {0,1} 的噪声过程（随机性 s 控制错误概率）。CBF 用一个确定性网格覆盖可能的 (v, s) 值，维护每个网格点的后验权重，计算加权平均信念。响应模型加入了 choice stickiness 参数 ρ。每个被试拟合5个自由参数：μ_v, η_v, μ_s, η_s, ρ（前四个分别控制两个 Beta 先验的均值和离散度）。
- **算法流程**：对每个被试，使用 MAP 估计（cbm 工具箱，Laplace 近似）拟合参数，10次随机初始化取最优解。从拟合参数生成 trial-by-trial 预测，再在 block 层面计算学习率（通过回归或导数）。

## 3. 实验设计
- **使用的数据集/场景**：
  - **实验1**：在线样本（Prolific），N=2532（排除后）。连续奖励任务“bird task”，四块（2×2因子设计：高/低波动性 × 高/低随机性）。每块40 trial，被试推断隐藏鸟的位置并移动桶接硬币包。
  - **实验2**：在线样本（从实验1被试邀请），N=723。两个二元任务：奖励版（寻找海狮宝藏）和损失版（躲避海龟水母刺伤），结构相同（2×2因子设计，每块40 trial）。两个任务在不同天完成，顺序固定。
  - 未使用外部 benchmark 数据集或对比其他计算方法，但独立使用先前已发表数据（N=643）的均值作为分类阈值（c_v, c_s）。
- **对比方法**：主要与仅操纵波动性的范式对比，本文通过同时操纵波动性和随机性来解耦二者。

## 4. 资源与算力
- **未明确说明**：论文未提及 GPU 型号、数量、训练时长等算力信息。分析使用 MATLAB R2023b 和 Python 3.11.5，以及 cbm 工具箱进行 MAP 估计（CPU 即可完成，无需大规模 GPU）。未提供具体硬件配置。

## 5. 实验数量与充分性
- **实验数量**：两个主要实验，覆盖三个任务（连续、奖励二元、损失二元），总体样本量超过3200。实验1做了分类分析（定义三组表型）、维度回归（将学习效应回归到因子分数）等。实验2进行了跨任务共享成分和效价对比的回归分析，以及逐任务回归。
- **充分性**：样本量大（实验1>2500，实验2~700），统计检验充分（t检验、ANOVA、GLM），结果稳定。分类阈值来自独立公开数据，避免过拟合。因子分析基于多量表，跨诊断维度合理。实验设计严格（2×2因子设计，注意检查、排除不认真被试）。结论一致性强，支持双重分离假说。整体充分、客观、公平。

## 6. 论文的主要结论与发现
- **主要发现**：双重分离——stochasticity-blind 学习者在内化症状（焦虑、抑郁）上得分显著更高；volatility-blind 学习者在外部化症状（行为成瘾、强迫性）上得分显著更高。
- **维度分析补充**：内部控制维度（Internalizing）与基线学习率正相关（且损失情境下更强）；外部控制维度（Externalizing）与波动性敏感性（降低）负相关，且不受效价调节。
- **总体结论**：精神病理学中的学习缺陷是选择性的，不同症状维度对应不同的不确定性归因失败（随机性盲→内化，波动性盲→外化），支持了选择性而非一般性缺陷理论。

## 7. 优点
- **大样本跨诊断设计**：实验1 N>2500，实验2 N~723，提供了足够的统计检验力。
- **因子操纵解耦**：同时操纵波动性和随机性，避免了传统仅操纵波动性导致的天花板效应和混淆。
- **模型中性分析与计算建模互补**：实验1用模型中性回归直接估计学习率，实验2用CBF-HMM拟合，结果相互印证。
- **独立阈值定义**：分类阈值来自先前大样本（N=643），避免了数据集依赖的阈值选择。
- **跨任务、跨效价验证**：三个任务（连续、二元奖励、二元损失）复现了核心模式，提升了泛化能力。
- **维度与分类分析结合**：既识别了离散表型，也在连续维度上发现关联，全面刻画了个体差异。

## 8. 不足与局限
- **样本局限**：非临床样本，使用自我报告症状测量，无结构化临床访谈。结果需在临床样本中重复。
- **外部化因子覆盖不全**：主要涵盖行为成瘾和强迫性，未充分代表品行障碍、反社会、物质使用等更广泛的外部化维度。
- **随机性相关关联较弱**：在维度分析中随机性效应与精神病理学关系不如基线学习率和波动性效应一致，可能因随机性加工个体差异较小或任务设计未充分放大。
- **实验2顺序固定**：奖励和损失任务在不同天固定顺序，可能存在顺序效应（尽管作者认为疲劳和延续效应不相关）。
- **计算负荷**：CBF-HMM的拟合需10次随机初始化，但未报告具体运行时间或资源要求。
- **纵向稳定性未知**：未检验这些计算表型在时间上的稳定性或对治疗的敏感性。

（完）
