---
title: Prefrontal activation predicts response latency and is shaped by age and lifestyle
title_zh: 前额叶激活预测反应延迟且受年龄和生活方式影响
authors: "Mitchell-Heggs, R., Tamkin, D., Scherdel, L., Snowdon-Farrell, A., Curry, A., Rosenior-Patten, O., Schultz, S. R."
date: 2026-06-28
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.22.733821v1.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 结合可穿戴睡眠指标与fNIRS测量的前额叶激活
tldr: 神经精神疾病与生活方式相关，但皮层血流动力学关系不明。LUCID纵向研究92名健康成人，结合可穿戴睡眠与活动数据及TD-fNIRS测量的dlPFC血氧。发现dlPFC激活与反应时间负相关，激活具有稳定个体差异，年龄是最强预测因素。该研究证明TD-fNIRS dlPFC激活是可扩展追踪可改变风险的功能神经标志。
source: biorxiv
selection_source: fresh_fetch
motivation: 揭示dlPFC血流动力学与生活方式、年龄的关系，建立可扩展的神经标志物。
method: LUCID纵向研究92健康成人，用TD-fNIRS测任务态dlPFC血氧，结合可穿戴睡眠活动数据。
result: dlPFC激活与反应时间显著负相关，激活具有中等重测信度，年龄为最强预测因素。
conclusion: TD-fNIRS测量的dlPFC激活是稳定、行为相关的功能神经标志，可用于追踪可改变风险。
---

## 摘要
神经和精神疾病影响全球43%的人口，其中许多受到可改变的生活方式暴露的影响，但它们与皮层血流动力学的关系尚不明确。背外侧前额叶皮层（dlPFC）是一个特别易处理的目标：它支撑执行功能，在神经精神和年龄相关疾病中受到干扰，并且位于皮层表面，可通过可扩展、可穿戴级的光学神经成像进行检测。我们提出了LUCID，一项针对92名健康成年人的纵向研究，结合了可穿戴消费级睡眠和身体活动指标，以及由时域功能近红外光谱（TD-fNIRS）测量的任务诱发dlPFC血流动力学。在2N-Back和Stroop任务以及两个半球中，对数转换的峰值dlPFC激活与反应时间（RT）呈负相关（r = -0.37至-0.53），更大的激活伴随更快的反应，这与容量/招募模型一致。激活表现出中等的重测信度（组内相关系数，ICC = 0.56-0.71），个体间变异超过个体内波动，表明稳定的个体差异。人口统计学和生活方式特征逐步预测激活，年龄是最强的预测因子，睡眠和身体活动的贡献适度。这些发现确立了TD-fNIRS dlPFC激活作为纵向稳定、行为相关的功能性神经标记，用于可扩展追踪可改变风险因素。

## Abstract
Neurological and neuropsychiatric conditions affect 43% of the global population, many shaped by modifiable lifestyle exposures, yet their relationship to cortical haemodynamics is poorly characterised. The dorsolateral prefrontal cortex (dlPFC) is a particularly tractable target: it underpins executive function, is disrupted across neuropsychiatric and age-related conditions, and lies on the cortical surface, within reach of scalable, wearable-grade optical neuroimaging. We present LUCID, a longitudinal study of 92 healthy adults combining consumer wearable sleep and physical activity metrics with task-evoked dlPFC haemodynamics, measured by time-domain functional near-infrared spectroscopy (TD-fNIRS). Log-transformed peak dlPFC activation was negatively associated with reaction time (RT) across the 2N-Back and Stroop tasks and both hemispheres (r = -0.37 to -0.53), greater activation accompanying faster responses, consistent with a capacity/recruitment account. Activation showed moderate test-retest reliability (intraclass correlation coefficient, ICC = 0.56-0.71), with between-person variance exceeding within-person fluctuation, indicating stable individual differences. Demographic and lifestyle features incrementally predicted activation, with age the strongest predictor and modest contributions from sleep and physical activity. These findings establish TD-fNIRS dlPFC activation as a longitudinally stable, behaviourally relevant functional neural marker for scalable tracking of modifiable risk.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：神经精神疾病（影响全球43%人口）与可改变的生活方式暴露密切相关，但这些暴露与大脑皮层血流动力学的关系尚不清楚。背外侧前额叶皮层（dlPFC）因支撑执行功能、在神经精神和年龄相关疾病中受损，且位于皮层表面适合可穿戴光学成像，成为理想研究目标。
- **研究动机**：现有研究多为单次或急性操纵设计，无法区分稳定的个体差异与日常波动；且很少针对dlPFC的特异性任务诱发激活。论文旨在评估dlPFC的血流动力学激活是否可作为纵向稳定、行为相关的功能神经标记，并揭示年龄和可穿戴设备测量的生活方式（睡眠、身体活动）如何塑造这种激活。
- **整体含义**：建立可扩展、可重复的神经标记，用于追踪可改变风险因素对大脑功能的影响，为上游预防和干预提供新工具。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：通过纵向多次测量，结合时域功能近红外光谱（TD-fNIRS）测量任务诱发的dlPFC氧合血红蛋白变化，与消费者可穿戴设备提供的长期睡眠和身体活动数据，评估激活的稳定性及其与行为和生活方式的关系。
- **关键技术细节**：
  - **TD-fNIRS**：发射皮秒光脉冲，测量光子飞行时间分布（DTOF），深度灵敏度更高，可部分分离皮层与表层信号。使用Kernel Flow2系统，两个波长（690和905 nm），采样率3.76/4.76 Hz，覆盖双侧dlPFC。
  - **预处理**：使用制造商Hb Moments管道获得HbO/HbR浓度变化，带通滤波（0.02–0.2 Hz），限制于长分离通道。运动校正和全局信号回归（短分离通道平均信号回归）。
  - **任务诱发激活估计**：采用一般线性模型（GLM），有限脉冲响应（FIR）基函数（20秒后刺激窗口），拟合全部任务期HbO时间序列。引入短分离通道前10个主成分作为系统性和表层贡献的回归量。提取每个任务（2N-Back、Stroop）的峰值激活β_max。
  - **可穿戴特征提取**：从Oura、Whoop等设备获取每日睡眠（时长、效率）和身体活动（步数、活跃时间等）指标。对每个指标定义三个回顾窗口（前1天、7天、30天），计算均值、标准差、偏度、峰度和线性趋势等统计量。还包含以个人为中心偏差特征。
  - **预测模型**：Ridge回归（α=2.98），特征包括人口统计学（年龄组、性别）、三个选定可穿戴特征（前一日步数、30天活跃时间标准差、30天睡眠时长峰度）、时间混淆变量（一天中的小时）。采用参与者分组的5折交叉验证重复100次，评估池化R²。SHAP值用于特征重要性。
  - **重测信度**：使用ICC（A,1）评估跨三次会话的稳定性，分解个体间和个体内方差。
  - **相关分析**：Pearson相关检验log(β_max)与反应时间和准确率的关系。
  - **公式**：后期指数 \( LI = (l-dlPFC - r-dlPFC)/(l-dlPFC + r-dlPFC) \)，范围[-1,1]。

## 3. 实验设计：使用了哪些数据集/场景，benchmark是什么，对比了哪些方法

- **数据集**：LUCID研究，92名健康成年人（42女，年龄18–55岁），每人完成三次扫描会话（间隔约10天），同时收集TD-fNIRS、认知任务（2N-Back和转换Stroop）和可穿戴生活方式数据（持续3个月基线+研究期间）。最终具有完整可穿戴数据的子样本53人（159次扫描）。
- **场景/任务**：
  - 2N-Back工作记忆任务（78试次，外定速，需判断当前图片是否与前两幅匹配）。
  - 转换Stroop颜色-词语干扰任务（60试次，自定速，含一致、不一致和转换试次）。
- **基准（Baseline）**：预测模型中采用“均值基线”（预测训练集均值）作为对照组；重测信度无明确基准；激活与行为相关无对比方法。
- **对比方法**：论文主要对比不同特征域（人口统计学、睡眠、活动、时间混淆）单独和组合的预测性能，以及不同目标类型（神经激活、行为指标、复合指标RT/激活、Perf/激活）的可预测性。没有与其他机器学习模型比较（只用了Ridge回归）。消融实验通过逐步添加特征域评估贡献。

## 4. 资源与算力

- **文中未明确说明使用的GPU型号、数量和训练时长**。
- 分析使用Python 3.14.2，库包括NumPy、SciPy、pandas、scikit-learn、Pingouin、SHAP、MNE-NIRS、Nilearn。数据存储在Connectome Health平台。可穿戴数据通过Terra API获取。
- 由于主要进行统计分析和轻度机器学习（Ridge回归），算力需求较低，可能使用CPU完成。

## 5. 实验数量与充分性

- **实验类型**：
  - 相关性分析（4个区域-任务组合，与RT和准确率的Pearson r）。
  - ICC及方差分解（每个神经和行为指标的ICC、个体间/内方差）。
  - 两因素ANOVA（年龄组×性别）分析β_max和RT（4个区域-任务组合）。
  - 预测模型：对每个任务（2N-Back、Stroop）预测多个目标（左、右、双侧dlPFC激活，中位RT，正确数，以及两个复合指标RT/bilateral激活、Perf/bilateral激活）。使用100次重复5折交叉验证，每次参与者分层。SHAP重要性。还测试不同特征域组合（睡眠、活动、人口统计学、时间混淆）。
  - 补充分析：半球后期指数、组间比较、跨会话变化（Wilcoxon检验）。
- **充分性评估**：
  - **优点**：纵向设计（三次测量），交叉验证严格避免数据泄露（参与者分层），重测信度量化稳定，多种目标对比，SHAP解释模型。
  - **不足**：
    - 样本量中等（92人），完整子样本更小（53人）。
    - 未进行外部验证或独立测试集，只在内部交叉验证。
    - 缺少与更复杂模型（如随机森林、神经网络）的比较，只用了线性Ridge。
    - 未控制组间差异（如年龄组样本量不均：13/30/28/21）。
    - 任务结构差异（2N-Back外定速 vs Stroop自定速）可能限制跨任务直接比较。
    - 部分分析（如ANOVA）仅基于扫描观测276个，未做严格多重比较校正（除交互作用外）。
  - 总体而言，实验设计合理，但在外部验证、模型多样性、校正方面有提升空间。

## 6. 论文的主要结论与发现

1. **dlPFC激活与行为相关**：log(β_max)与中位反应时间呈显著负相关（r = -0.37到-0.53），更大的激活伴随更快反应，支持“容量-招募”假说而非传统效率假说。
2. **激活具有稳定个体差异**：ICC为0.56–0.71，个体间方差超过个体内方差（比值>1），表明dlPFC激活是“特质性”而非状态性。
3. **年龄是激活的最强预测因素**：年龄组效应所有区域-任务组合显著，效应量中等偏小（η²=0.087–0.173），年龄增长伴随激活降低。性别无显著主效应，只有一次轻微交互。
4. **生活方式贡献较小但存在**：可穿戴睡眠和活动指标在人口统计学基础上增加少量预测力（R²从0.181到0.209）。时间混淆（前一日步数、小时）增加最大增量（ΔR²=0.130）。
5. **复合指标（RT/激活）最可预测**：Stroop下复合指标R²=0.406，显著高于单独RT（0.218）和单独激活（0.339），但未显著高于激活成分。说明生活方式信号主要存在于血流动力学反应而非行为速度。
6. **半球后期指数无年龄/性别差异、可靠性低**（ICC=0.21），表明半球平衡非稳定特质。

## 7. 优点：方法或实验设计上的亮点

- **纵向重复测量**：三次会话允许分离个体间和个体内变异，评估重测信度，比单次测量设计提供更可靠的个体差异估计。
- **结合真实世界可穿戴数据**：使用消费级设备客观连续测量睡眠和身体活动，覆盖多个时间窗口（日、周、月），优于自我报告或单一域监测。
- **TD-fNIRS技术优势**：比连续波fNIRS具有更好深度敏感性和定量准确性，提高测量皮层信号的置信度。
- **严格交叉验证**：参与者分组折叠确保无数据泄露，100次重复稳定R²估计，置信区间使用bootstrap。
- **系统特征选择**：通过前向选择+SHAP一致性提取三个关键非冗余特征，避免过拟合。
- **多目标预测**：同时建模神经、行为和复合指标，揭示生活方式信号主要来源于激活而非行为。
- **分析全面**：包含ICC、相关性、ANOVA、预测、SHAP解释，方法透明。

## 8. 不足与局限：包括实验覆盖、偏差风险、应用限制等

- **样本限制**：全部健康成年人（18–55岁），不能推广到儿童、老年人或患者。年龄组样本不平衡（18-24岁仅13人），可能影响统计功效。
- **数据缺失**：可穿戴数据完整性不足，最终预测模型仅用53人（159次扫描），可能引入偏倚并降低功率。
- **设备异质性**：参与者使用不同品牌可穿戴设备（Whoop、Apple Watch等），算法差异可能引入测量噪声（虽会衰减效应）。
- **fNIRS信号质量偏倚**：头发类型和头皮-光极耦合影响信号质量，未量化或校正，存在公平性担忧（某些发质可能导致更差信号）。
- **任务结构不对称**：2N-Back外定速（时间压力）与Stroop自定速（自由决策）可能混淆反应时间含义，限制跨任务直接比较。
- **年龄效应为横截面**：年龄分组是不同个体，无法排除出生队列效应的干扰。
- **观察性设计**：无法推断因果关系；生活方式对激活的贡献可能受未测量的混杂因素（如遗传、社会经济地位）影响。
- **预测性能有限**：即使复合指标R²=0.406，大部分方差未解释；贡献增量小（睡眠+活动仅添加0.03），实际应用时需谨慎。
- **缺乏外部验证**：仅内部交叉验证，可能在外部数据集上表现下降。
- **不完整统计分析**：部分组间比较未校正多重比较（如交互作用p=0.046未校正），ANOVA仅针对扫描观察而非参与者均值。
- **伦理声明**：多名作者具有潜在利益冲突（来自资助方Connectome Health），可能影响客观性。

（完）
