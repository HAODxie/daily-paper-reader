---
title: "HARMONY: A large-scale harmonized neuroimaging dataset for research on anxious misery disorders"
title_zh: HARMONY：用于焦虑痛苦障碍研究的大规模协调化神经影像数据集
authors: "Jarukasemkit, S., Harms, M. P., Lenzini, P., Chen, A., Glasser, M. F., Hamilton, K., Li, L., Luo, X., Myers, M., Pines, A. R., Reid, E., Tozzi, L., Zavaliangos-Petropulu, A., Zhang, J., Whitfield-Gabrieli, S., Narr, K. L., Williams, L. M., Sheline, Y., Bijsterbosch, J. D."
date: 2026-07-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.26.732748v1.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 大规模多模态神经影像数据集，用于焦虑痛苦障碍和心理健康研究
tldr: 焦虑和抑郁的脑回路功能障碍模式需跨人群验证。HARMONY数据集整合四个HCP风格队列，涵盖青少年至成年晚期，提供标准化预处理、质量控制和统一症状测量。合并队列显著提高检测影像-症状关联的统计功效，但效应量较小；功能影像衍生表型具有最强多变量预测性能。该资源为可重复精神健康神经影像研究奠定基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 焦虑和抑郁的脑功能障碍模式需大规模跨队列验证其泛化性。
method: 整合四个HCP风格队列，进行标准化预处理、质量控制与症状测量统一。
result: 合并队列增强统计功效，功能影像预测性能最佳，但效应量较小。
conclusion: HARMONY提供大规模多队列公共资源，促进可重复精神健康神经影像研究。
---

## 摘要
抑郁症和焦虑症背后的大脑回路功能障碍模式已被越来越多地刻画，包括维度及亚型变异。一个关键挑战是如何确定这些模式在人群和测量框架中的普适性。在此，我们介绍HARMONY，一个协调化的多模态神经影像数据集，支持对症状定义维度上大脑-行为关联的大规模研究。HARMONY整合了四个人类连接组计划风格的疾病相关人类连接组队列，涵盖从青少年到成年后期，并捕捉焦虑痛苦症状。该资源将标准化的HCP风格预处理、质量控制、影像衍生表型以及协调化的症状测量整合为一个临床丰富的公共数据集。使用HARMONY进行的概念验证分析表明，合并异质性队列可提高检测影像衍生表型与快感缺失及抑郁严重度之间关联的统计功效。效应量仍然较小，与跨异质性样本的症状基测量一致。功能影像衍生表型显示出最强的多变量预测性能。总之，HARMONY为可重复的心理健康神经影像研究提供了一个大型多队列资源。

## Abstract
Patterns of brain circuit dysfunction underlying depression and anxiety have been increasingly characterized, including dimensional and subtype variation. A key challenge is determining how such patterns generalize across populations and measurement frameworks. Here, we introduce HARMONY, a harmonized multimodal neuroimaging dataset supporting large-scale investigation of brain-behavior associations across symptom-defined dimensions. HARMONY integrates four Human Connectome Project-style Connectomes Related to Human Disease cohorts spanning adolescence to later adulthood and capturing anxious misery symptoms. The resource combines standardized HCP-style preprocessing, quality control, imaging-derived phenotypes, and harmonized symptom measures into a clinically enriched public dataset. Proof-of-concept analyses using HARMONY showed that pooling heterogeneous cohorts increased statistical power for detecting associations between imaging-derived phenotypes and anhedonia and depression severity. Effect sizes remained modest, consistent with symptom-based measures across heterogeneous samples. Functional imaging-derived phenotypes showed the strongest multivariate predictive performance. In summary, HARMONY provides a large multi-cohort resource for reproducible mental health neuroimaging research.

---

## 论文详细总结（自动生成）

# HARMONY：用于焦虑痛苦障碍研究的大规模协调化神经影像数据集——论文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **研究动机**：焦虑和抑郁等“焦虑痛苦”障碍的脑回路功能障碍模式已被广泛刻画（如维度、亚型），但尚不清楚这些模式能否在不同人群和测量框架中泛化。大多数现有研究样本量较小、队列间处理不一致，限制了可重复性和泛化能力。
- **整体含义**：本文构建并公开了一个大规模、协调化的多模态神经影像数据集（HARMONY），整合了四个源自人类连接组计划（HCP）风格的疾病相关队列（CRHD），覆盖青少年至老年，统一预处理、质量控制和症状测量，旨在支持跨队列、数据驱动的脑-行为关联研究，推动精神健康神经影像的可重复科学。

## 2. 方法论：核心思想、关键技术细节
- **核心思想**：通过标准化处理管道、严格质量控制、提取成像衍生表型（IDPs）、并用统计协调化方法去除站点效应，同时保留症状相关变异，实现四个异质性队列的无缝整合。
- **关键技术细节**：
  - **预处理管道**：基于QuNex实现更新版HCP最小预处理管道，包括：
    - 手动检查并编辑Freesurfer皮层表面（5.3%受试者需修改）。
    - 扩展fMRI预处理：ICA-FIX去除结构化噪声、MSMAll多模态表面配准改善功能对齐、Reclean模块优化ICA分类、temporal ICA去除非结构化噪声。
    - dMRI预处理：TOPUP/EDDY校正、运动-敏感性移位校正、切片-体积运动校正。
  - **IDP提取**：分6个家族（每种模态2个），共13种IDP类型，覆盖：
    - sMRI：灰质体积、皮层厚度、髓鞘（来自T1w/T2w比），基于DKT、HCP-MMP1.0、ASEG图谱。
    - rfMRI：功能振幅（标准差）、全相关/偏相关连接性，基于ICA-25、ICA-200、HCP2016FS图谱；还提供双侧合并版本。
    - dMRI：分数各向异性、平均扩散率、NODDI衍生指标（NDI、ODI、IVF），基于JHU-81图谱及TBSS骨架化版本。
  - **协调化方法**：
    - **ComBat-GAM**：使用广义加性模型拟合年龄非线性效应，仅在健康对照组上训练，然后应用到病例，以保留症状相关变异。
    - **CovBat-GAM**：也纳入年龄、性别和快感缺失评分作为协变量，但无法分离训练集（在全样本上训练）。
    - 评估：通过交叉验证的SVM站点分类精度（越低越好）和年龄-体积关联曲线。

## 3. 实验设计：数据集、基准、对比方法
- **使用的数据集**：四个CRHD队列：
  - HCP-BANDA（青少年，14-17岁，N=152病例+63对照）
  - HCP-DES（年轻成人，18-36岁，N=222+50）
  - HCP-DAM（成人，基于神经质评分，N=197+49）
  - HCP-PDC（治疗抵抗抑郁，20-76岁，N=172+58）
  - 总计743例病例，220例健康对照。
- **基准（Baselines）**：
  - 对比**单独队列** vs **合并后的HARMONY数据集**。
  - 对比**ComBat-GAM**（对照组训练） vs **CovBat-GAM**（全样本训练）两种协调化效果。
- **评估方法**：
  - **多变量预测**：主成分回归（PCR，k=25），100次重复5折交叉验证，预测快感缺失（SHAPS）和抑郁严重度（HAMD）。评估指标为交叉验证R²。
  - **单变量关联**：年龄、性别校正后偏相关，FDR校正（q<0.05），展示效应量分布。
  - **站点效应评估**：SVM多类分类，平衡准确率。

## 4. 资源与算力
- **文中未明确说明使用的GPU型号、数量或训练时长**。仅提及计算在华盛顿大学研究计算与信息学设施（RCIF）上完成，该设施获得NIH S10资助（1S10OD025200-01A1, 1S10OD030477-01）。预处理和IDP提取主要依赖CPU密集型流程（FreeSurfer、FSL、QuNex），未涉及深度学习训练，因此算力需求相对常规。

## 5. 实验数量与充分性
- **实验组数**：
  - 13个IDP类型 × 2种症状（SHAPS, HAMD）× 2种协调化方法（ComBat-GAM, CovBat-GAM）+ 无协调化，进行多变量预测（共约52组主要PCR实验）。
  - 单变量分析：3个代表性IDP（灰质体积、偏相关ICA25、FA）分别对应两种症状，FDR校正。
  - 站点分类实验：13个IDP × 2种协调化方法 + 无协调化，分别在对照组和病例组。
  - 对比单独队列 vs 合并数据集：选择3个IDP展示。
- **充分性评价**：实验设计合理，覆盖了主要模态、症状、协调化策略。但由于论文本身是资源介绍，未进行大规模消融或跨多个独立验证集的泛化测试。结果仅作为概念验证，效应量较小，但统计显著。实验足够支撑论文核心结论（合并提高功效、功能IDP预测最优、ComBat-GAM保留更多症状变异）。

## 6. 主要结论与发现
- **合并队列提升统计功效**：HARMONY数据集（N=743）相比单独队列，多变量预测的交叉验证R²显著更高，且训练-测试差距（过拟合指标）显著降低。
- **功能IDP预测性能最强**：在13个IDP类型中，双侧化偏相关连接性（bilat_partial_corr_HCP2016FS）对快感缺失的预测R²最高；对抑郁严重度预测不显著。
- **ComBat-GAM（对照组训练）优于CovBat-GAM**：在保留症状变异方面更有效，表现为更高的预测R²，且站点分类准确率在病例组仍较高（反映真实的临床差异）。
- **单变量关联效应量小**：灰质体积与快感缺失呈负相关（平均r≈-0.12），主要涉及额、顶、扣带等区域；功能连接与快感缺失/抑郁严重度均有关联（平均|r|≈0.14-0.15）；dMRI中仅胼胝体压部（负相关）和穹窿（正相关）与快感缺失显著。
- **资源公开**：提供原始IDP、ComBat-GAM协调化IDP、QC指标、症状数据及数据字典，可从NDA和BALSA下载。

## 7. 优点：方法或实验设计的亮点
- **大规模统一处理**：四个队列均采用相同HCP管道、手动皮层表面审核、MSMAll配准、ICA-FIX/Reclean/Tclean去噪，保证数据高度一致。
- **创新的协调化策略**：在ComBat-GAM中仅用健康对照训练，避免移除与症状关联的变异；并与CovBat-GAM对比，展示优势。
- **丰富的IDP集合**：提供多模态、多图谱、从低维到高维的特征，覆盖体积、厚度、髓鞘、功能幅度、全/偏相关、扩散张量和微结构，便于用户灵活选择。
- **严格的QC共享**：提供信号、运动、ICA成分等多项QC指标，鼓励用户自定义排除标准。
- **概念验证实验设计严谨**：多变量预测使用嵌套交叉验证避免泄露；单变量进行FDR校正；效应量报告实际大小，不夸大结果。

## 8. 不足与局限
- **症状覆盖有限**：仅快感缺失（SHAPS）和抑郁严重度（HAMD）在所有成人队列中可用，缺乏焦虑等其他关键维度；青少年队列无HAMD。
- **严重度分布偏轻中度**：虽然病例均经筛选，但多数仍处于轻中度范围，可能限制对上重度或亚型特异效应的检测。
- **站点效应与临床差异混淆**：由于各队列症状严重度系统性不同，协调化时难以完全分离；ComBat-GAM虽保留部分变异，但病例组的站点分类精度仍较高。
- **无独立外部验证**：所有分析均在HARMONY自身内部进行，未在完全独立的数据集上验证泛化性。
- **算力细节缺失**：未报告GPU型号、数量、训练时长，不利于复现或评估计算成本（不过本工作主要依赖CPU）。
- **未提供纵向/治疗数据深入分析**：虽有随访设计，但本文主要聚焦基线横断面分析。
- **谱系非随机采样**：各队列入选标准不同（年龄、治疗抵抗、神经质等），可能引入选择偏倚。

（完）
