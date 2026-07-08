---
title: Night-to-night sleep EEG variability over one year
title_zh: 一年内夜间睡眠脑电图的可变性
authors: "Rosenblum, Y., Bovy, L., Hemmsen, M. C., Duun-Henriksen, J., Ahrens, E., Dresler, M."
date: 2026-07-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.02.736125v1.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 一年内睡眠脑电变异性研究（皮下EEG记录）
tldr: "本研究通过分析20名健康受试者一年内6429晚皮下脑电图数据，利用非周期斜率、sigma和慢波功率的时间序列作为整夜睡眠宏观结构单元，采用动态时间规整量化夜夜差异。结果表明整体模式相似度约80%，但时间对齐需扭曲约60%；较低宏观结构变异与更好主观睡眠质量相关。不同睡眠指标变异程度差异显著：谱功率、睡眠时长、N2和REM变异低（<20%），N3和宏观结构差异中等（20-40%），睡眠周期时长、清醒和N1变异高（>40%）。该发现揭示睡眠变异更依赖具体指标而非尺度，可能区分特质稳定与动态变化特征。"
source: biorxiv
selection_source: fresh_fetch
motivation: 探索健康人群长期睡眠宏观结构夜夜变异模式及其与主观睡眠质量的关系。
method: 采用皮下EEG记录一年数据，以非周期斜率、sigma和慢波功率时间序列为宏观结构单元，用动态时间规整计算夜夜差异。
result: "夜夜宏观结构相似度80%，时间对齐扭曲60%；宏观结构差异与睡眠质量负相关(r=-0.25)；不同指标变异系数跨度大，宏观结构差异中等。"
conclusion: 睡眠夜夜变异更多是指标特异而非尺度依赖，可能反映特质与动态特征的区分。
---

## 摘要
本研究旨在通过分析20名健康参与者一年内（每人205-388个夜晚，共6429个夜晚）的皮下脑电图（sqEEG），探索多尺度睡眠模式的夜夜变异性。我们利用非周期性斜率、sigma波和慢波功率的时间序列作为睡眠宏观结构的新整夜单位。使用动态时间规整，我们计算这些时间序列之间的距离（差异）来评估夜夜间睡眠宏观结构的差异。我们发现，整体睡眠宏观结构模式在不同夜晚之间相对相似（20%的差异），而它们的时间对齐则相当多变（最佳对齐所需的时间序列扭曲约60%）。宏观结构差异性的较低变异与更好的主观睡眠质量相关（r=-0.25）。然后，我们定性地比较了宏观尺度、微观尺度（睡眠阶段比例、平均频谱功率）和中观尺度（睡眠周期持续时间）指标的年度变化。我们发现，个体内夜间变异性为：频谱功率、睡眠持续时间、N2和REM睡眠为“低”（变异系数<20%）；N3和宏观结构差异性为“中等”（20-40%）；睡眠周期持续时间、清醒和N1为“高”（>40%）。总之，不同的睡眠指标显示出不同的夜夜变异性，这种变异性更多地与指标本身相关而非尺度依赖性。这可能反映了睡眠中更像特质与更动态变化的特征之间的区别，尽管这一假设需要进一步澄清。

## Abstract
This study aimed to explore night-to-night variability of multiscale sleep patterns by analyzing subcutaneous electroencephalography (sqEEG) from 20 healthy participants over one year (205-388 nights per participant, 6,429 nights in total). We utilized the time series of aperiodic slopes, sigma and slow-wave power as a new whole-night unit of sleep macrostructure. Using dynamic time warping, we calculated the distances (differences) between those time series to assess night-to-night sleep macrostructure dissimilarity. We found that the overall sleep macrostructural patterns were relatively similar across nights (20% dissimilarity), while their temporal alignment was quite variable (time series warped by ~60% for the best alignment). Lower variation in macrostructure dissimilarity was associated with better subjective sleep quality (r=-0.25). Then, we qualitatively compared yearlong variation in macroscale, microscale (sleep stage proportions, mean spectral power) and mesoscale (sleep cycle duration) metrics. We found that intra-individual night-to-night variation was '"low (coefficients of variation < 20%) for spectral power, sleep duration, N2 and REM sleep; ''medium'' (20-40%) - for N3 and macrostructure dissimilarity; and "high" (>40%) - for sleep cycle duration, wake and N1. In summary, different sleep metrics showed differential night-to-night variability, which was more metric-specific than scale-dependent. This might reflect a distinction between more trait-like versus more dynamically varying features of sleep, although this assumption needs further clarification.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **传统睡眠研究的局限**：标准的实验室多导睡眠图（PSG）只能提供单夜“快照”，无法捕捉睡眠的时间动态和夜夜规律性。而睡眠规律性对身心健康的贡献可能不亚于睡眠时长。
- **技术突破**：近年来发展出的皮下脑电图（sqEEG）设备可实现超长期（长达一年）的连续EEG监测，这是传统PSG或家用可穿戴设备难以做到的。
- **研究目标**：利用迄今最长连续健康人sqEEG数据集，探索健康人睡眠的多尺度（微观、中观、宏观）夜夜变异模式，并引入新的宏观结构度量（基于全夜EEG时间序列）来刻画夜夜差异，最终区分更像“特质”的稳定特征和更像“状态”的动态变化特征。

## 2. 方法论：核心思想、关键技术细节

- **核心思想**：将整夜睡眠EEG视为一个宏观结构单元——使用**非周期性斜率**、**sigma波功率**和**慢波活动（SWA）**的平滑时间序列；通过**动态时间规整（DTW）**量化连续两夜之间的宏观结构差异。
- **技术细节**：
  - **EEG预处理**：对双通道sqEEG信号（平均后）进行30秒分段，利用Irregularly Resampled Auto-Spectral Analysis分离周期性与非周期性成分。计算非周期性成分在1-28Hz范围内的斜率（幂律指数），周期性成分中sigma（11-16Hz）和SWA（1-4Hz）的相对功率。
  - **宏观时间序列构建**：对每一夜的每个睡眠周期进行z标准化，再使用Savitzky-Golay滤波器平滑，形成整夜（截取前5小时睡眠）的EEG时间序列。
  - **DTW距离计算**：对相邻两夜的时间序列应用DTW，允许非线性拉伸/压缩以实现最佳对齐，然后计算对齐后对应点之间的欧氏距离之和，再除以时间长度（5小时）得到归一化的**差异性指标**（dissimilarity，%）。同时记录**扭曲量**（warping amount，即为了对齐需要的时间轴变形比例）。
  - **变异系数（CV）**：对每个参与者计算各指标（微观、中观、宏观）一年内的CV，按固定阈值分类：非常低（<0.1）、低（0.1-0.2）、中（0.2-0.4）、高（>0.4）。
- **算法流程简述**：原始EEG → 谱分析 → 提取非周期性斜率和周期性功率 → 生成整夜时间序列（前5h） → 对相邻夜进行DTW → 得到距离和扭曲量 → 计算差异性指标 → 计算各指标的CV → 与主观睡眠质量做相关分析。

## 3. 实验设计：数据集、基准与对比方法

- **数据集**：
  - **主要数据集**：Ultra-Long-Term Sleep项目，20名健康参与者（11女，年龄19-62岁），每人205-388夜，共6429夜有效睡眠（>5小时且清醒＜25%）。使用植入式两通道sqEEG设备（24/7 EEG SubQ, UNEEG Medical A/S），采样率207Hz，0.5-48Hz滤波。睡眠分期由适配sqEEG的U-Sleep算法自动完成。
  - **复制验证数据集**：两个PSG数据集（每人3夜）和一个可穿戴EEG数据集（最多连续15夜），具体见补充表2。
- **基准与对比**：
  - **微观尺度指标**：睡眠阶段比例（WASO、N1、N2、N3、REM）、总睡眠时长、REM/NREM比值、平均谱功率（sigma在N2、SWA在N2/N3）、各阶段平均非周期性斜率。
  - **中观尺度指标**：基于非周期性斜率的“睡眠分形周期”参数（周期时长、下降/上升时长、下降/上升幅度）。
  - **宏观尺度指标**：DTW距离（基于三种时间序列：sigma、SWA、非周期性斜率）及其CV。
  - **对比逻辑**：定性比较各尺度指标夜夜变异（CV）的量级，探索是否“尺度越大变异越大”的假设。
- **其他分析**：将每月CV与主睡眠质量（单条目Likert量表）做Spearman相关；与WHO-5幸福指数和MDI抑郁量表做相关。

## 4. 资源与算力

- **未明确说明**：论文未提及使用的计算资源，如GPU型号、数量、训练时长等。所有分析基于MATLAB R2021b，Fieldtrip工具箱和自定义脚本。无大规模深度学习模型训练，因此算力需求不大。

## 5. 实验数量与充分性

- **实验组数**：
  - 对20名参与者分别计算各指标的CV（共23个指标），并汇总群体均值。
  - 复制验证在另外两个独立数据集（PSG 3夜、可穿戴15夜）上进行DTW分析，确认主要发现（结果见补充表2）。
  - 相关性分析：主观睡眠质量（逐月平均值）与23个指标的CV（逐月计算）做Spearman相关，并做Benjamini-Hochberg多重比较校正（23次检验）。
- **充分性与客观性**：
  - **优点**：数据量极大（>6000夜），长期连续监测是显著优势；复制验证增强了结论的可推广性；多维度指标比较全面。
  - **不足**：样本仅20人，年龄范围宽，但未细分亚组（如性别、年龄）；CV分类阈值（0.1, 0.2, 0.4）虽参考文献设定，仍有一定主观性；DTW仅比较相邻两夜，未考虑更长时间尺度模式（如周、月）；相关性较弱（r<0.3），可能受限于样本量和测量工具；缺乏对睡眠阶段过渡、微觉醒等精细特征的分析；未控制可能的影响因素（如季节、工作日/周末、社会时差）。

## 6. 主要结论与发现

- **宏观结构**：相邻两夜的EEG时间序列在最佳对齐后仅有约20%的残余差异，但需要约58%的时间扭曲才能对齐。这表明夜夜差异主要体现在时间相位上，而非整体模式形状。
- **变异程度分类**：
  - “非常低”变异（CV<0.1）：sigma功率（N2）、SWA（N2/N3）、非周期性斜率（N2,N3,REM睡眠）。
  - “低”变异（CV 0.1-0.2）：N2比例、REM比例、睡眠时长、REM/NREM比。
  - “中等”变异（CV 0.2-0.4）：N3比例、宏观结构差异性（sigma/SWA/非周期性斜率DTW距离）、分形周期振幅。
  - “高”变异（CV>0.4）：WASO、N1比例、分形周期时长（尤其是上升相和下降相）。
- **变异模式**：**更依赖指标本身而非尺度**。例如，同为微观层面的N1变异高，而sigma功率变异极低；中观层面周期时长变异高，但振幅变异中等。
- **与主观睡眠质量的关系**：宏观结构差异性（sigma/SWA/非周期性斜率DTW距离）的较小变异与更高主观睡眠质量相关（r≈-0.25）；微观指标中CV极低的（如SWA、sigma）与较好睡眠质量正相关，而CV中等的（如N3比例、非周期性斜率在N2/N3）与更好睡眠质量正相关（但方向相反）。整体相关性较弱。
- **与主观幸福感和抑郁**：无显著相关（可能由于所有参与者幸福感偏高的“天花板效应”）。

## 7. 优点

- **创新性**：首次提出基于DTW的“宏观结构差异性”度量，将整夜EEG时间序列作为睡眠实体，而非仅分期比例。
- **数据规模**：长达一年的连续sqEEG，超过6000夜，是目前健康人最长数据集，能真实反映夜夜波动。
- **方法严谨**：采用动态时间规整解决不同夜时间轴的偏移问题，更适合比较具有时间动态的序列。使用变异系数统一各指标比较标准，并给出具体分类。
- **复制验证**：在独立PSG和可穿戴EEG数据集上验证了主要发现，增强了结果的可靠性。
- **多尺度视角**：同时分析微观、中观、宏观指标，有助于理解睡眠层级结构间的联系，并发现“指标特异性”而非“尺度依赖性”的变异模式。

## 8. 不足与局限

- **样本偏倚**：仅健康志愿者（20人），年龄范围虽广但数量少；未分析不同年龄、性别亚组；可能无法推广至临床人群（如失眠、癫痫）。
- **设备记录限制**：sqEEG仅两通道，且设备自动在记录6小时后停止（重启），导致无法分析完整睡眠周期（尤其是后半段REM丰富的睡眠）；截断前5小时可能丢失重要变异源（如周末REM反弹）。
- **分析局限性**：DTW仅针对相邻两夜，未探索更长周期（如星期、月）模式；未区分工作日/周末影响；相关性分析仅使用单条目主观睡眠质量，可靠性有限。
- **统计不足**：CV分类阈值（0.1,0.2,0.4）有一定任意性；未对“尺度依赖性”假设进行直接统计检验（如ANOVA）；未考虑季节、社会时差等混杂变量。
- **机械解释缺失**：虽然提出指标特异性可区分“特质vs状态”，但未通过纵向模型（如方差分解、因子分析）直接证明；结论更多为描述性。
- **重复性验证较弱**：复制数据集仅3-15夜，远少于主要数据的1年长度，可能无法捕捉长期变异模式。

（完）
