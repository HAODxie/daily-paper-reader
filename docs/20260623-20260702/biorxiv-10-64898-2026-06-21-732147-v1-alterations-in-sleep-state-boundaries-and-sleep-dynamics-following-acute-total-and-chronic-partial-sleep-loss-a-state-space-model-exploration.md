---
title: "Alterations in sleep state boundaries and sleep dynamics following acute total and chronic partial sleep loss: a state space model exploration"
title_zh: 急性完全性与慢性部分性睡眠缺失后睡眠状态边界与睡眠动力学的改变：一项状态空间模型研究
authors: "Reutimann, S., Imbach, L., Burkhard, Z., Baumann, C. R., Maric, A."
date: 2026-06-25
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.21.732147v1.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 睡眠剥夺后睡眠状态边界和动力学的变化
tldr: 急性与慢性睡眠剥夺对睡眠结构的影响不同，本研究利用状态空间模型分析EEG动力学。结果显示慢性睡眠限制使REM与觉醒的频谱特征更相似，降低了状态边界区分度；而急性睡眠剥夺主要影响NREM谱组成，增强了慢波睡眠的稳定性。这些发现表明睡眠状态边界和动力学具有状态依赖性，未来可用于追踪睡眠障碍患者的治疗效果。
source: biorxiv
selection_source: fresh_fetch
motivation: 探究急性和慢性睡眠剥夺对睡眠状态边界和动力学的不同影响。
method: 使用状态空间模型对慢性睡眠限制和急性睡眠剥夺后夜间EEG进行动力学分析。
result: 慢性睡眠限制模糊了REM与觉醒的边界；急性睡眠剥夺仅增强慢波睡眠稳定性。
conclusion: 不同睡眠剥夺类型对睡眠结构的影响体现在状态边界和动力学差异上，具有状态依赖性。
---

## 摘要
慢性部分性和急性完全性睡眠缺失对睡眠结构有明显不同的影响。即急性睡眠剥夺主要导致慢波睡眠的强烈反弹，而慢性睡眠限制则导致快速眼动睡眠倾向增加。本研究旨在探讨这些不同效应是否会通过基于模型的方法转化为可量化的睡眠状态边界和动力学的变化。
除常规睡眠分期外，我们应用EEG模型（状态空间方法）对14名健康受试者在实验性慢性睡眠限制（连续7晚中最后一晚卧床5小时）和急性睡眠剥夺（40小时觉醒后的睡眠）下的夜间EEG记录进行动态分析，并与基线睡眠进行比较。
慢性睡眠限制下的受试者显示快速眼动睡眠和觉醒的频率组成相似性增加，从而两个行为状态之间的状态边界区分度降低。相反，急性睡眠剥夺影响了非快速眼动睡眠的频谱组成。只有急性睡眠剥夺导致更稳定的慢波睡眠。
我们的探索性研究证实，急性完全性和慢性部分性睡眠缺失后增加的快速眼动睡眠和慢波睡眠倾向的不同效应反映在行为状态边界和睡眠动力学的差异性变化中。这表明这些睡眠结构特征具有状态依赖性，未来可能允许使用这些指标来追踪以睡眠行为状态失调为特征的临床人群的治疗效果。

## Abstract
Chronic partial and acute total sleep loss have a distinct impact on sleep architecture. Namely, acute sleep deprivation primarily leads to a strong rebound of slow wave sleep, while chronic sleep restriction results in an increased propensity of REM sleep. The aim of this work was to examine whether these different effects would translate into quantifiable changes in sleep state boundaries and dynamics using a model-based method.

Besides conventional sleep stage scoring, we applied an EEG model (state space approach) for dynamic analysis of nocturnal EEG recordings in 14 healthy subjects under experimental chronic sleep restriction (last of 7 nights with 5 hours of time in bed) and after acute sleep deprivation (sleep following 40 hours of wakefulness), in comparison to baseline sleep.

Subjects under chronic sleep restriction revealed increased similarities in the frequency composition of REM sleep and wakefulness and thus, a decreased differentiation of state boundaries between the two behavioral states. Contrarily, acute sleep deprivation affected the spectral composition of NREM sleep. Only acute sleep deprivation resulted in more stable slow wave sleep.

Our explorative study confirmed that the distinct effects of increased REM sleep and slow wave sleep propensity following acute total and chronic partial sleep loss are reflected in differential changes of behavioral state boundaries and sleep dynamics. This suggests that these sleep structure characteristics are state dependent, which may allow using such measures in the future to track treatment effects in clinical populations characterized by sleep behavioral state dysregulation.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心科学问题**：急性完全性睡眠剥夺（ASD）和慢性部分性睡眠限制（CSR）对睡眠结构有着截然不同的影响——ASD主要引起慢波睡眠（SWS）的强烈反弹，而CSR主要增加快速眼动睡眠（REM）倾向。然而，这两种不同类型的睡眠缺失是否会在睡眠状态边界（state boundaries）和睡眠动力学（sleep dynamics）上产生可量化的差异，目前尚不清楚。
- **研究动机**：此前的研究已经应用状态空间分析（State Space Analysis, SSA）成功量化了临床人群（如帕金森病、发作性睡病）中睡眠结构的病理改变，但这些特征究竟是稳定的病理倾向还是可以被睡眠调节机制动态调制，一直未得到验证。本研究正是为了填补这一空白，通过比较同一健康受试者在不同睡眠缺失条件下的SSA指标变化，来检验SSA度量的状态依赖性。
- **整体含义**：如果SSA指标能够反映不同的睡眠调节反馈，那么未来这些指标可能用于追踪睡眠障碍（尤其是以睡眠行为状态失调为特征的疾病，如发作性睡病、睡眠不足综合征）患者的治疗效果或疾病进展。

### 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：利用EEG信号的频谱特征构建一个二维状态空间，将每一个睡眠/觉醒epoch映射为空间中的一个点。通过分析该空间中不同睡眠阶段所形成的簇（clusters）的位置、分离度、以及连续的轨迹速度，来定量描述睡眠状态之间的边界清晰度和睡眠状态的稳定性。
- **关键技术细节**：
  - **数据预处理**：用6个标准电极（F3、F4、C3、C4、O1、O2，平均参考）的EEG数据，分段为5秒epoch，并对应睡眠分期标签。计算Welch功率谱密度（5秒Hamming窗）。
  - **构建状态空间**：定义两个频谱比值：
    - Ratio1 = (8.6-19.3 Hz) / (1.0-10.9 Hz)  
    - Ratio2 = (11.5-20.3 Hz) / (17.9-31.5 Hz)  
    取两个比值的对数，分别作为x轴和y轴坐标。然后用50点Hann窗对时间序列进行平滑。
  - **速度与稳定性**：计算连续epoch之间的欧氏距离除以时间间隔作为速度。设定阈值0.01：速度<0.01视为“稳定状态”（构成簇），速度≥0.01视为“轨迹”（不稳定）。
  - **簇分析**：计算每个睡眠阶段所有稳定epoch的质心（centroid）位置；计算质心间欧氏距离衡量不同阶段频谱的相似性。
  - **点密度分析**：用核密度估计计算沿x轴和y轴的一维概率密度函数（仅稳定epoch，或包含所有epoch），进而计算峰-峰距离和重叠面积。
  - **过渡期分析**：用二维正态分布分配每个epoch到概率最高的睡眠阶段，然后计数相邻epoch间的阶段转换次数。
  - **数学本质**：整个方法不涉及复杂公式，核心是频谱比值的对数变换、欧氏距离、核密度估计，无端到端学习或神经网络。

### 3. 实验设计：数据集、场景、对比方法

- **数据集**：使用了一项先前发表的交叉设计研究中的14名健康年轻男性（平均21.9±3.0岁）的夜间高密度EEG数据（采样率500 Hz）。所有受试者均有规律的7–9小时睡眠习惯。
- **场景**：三种条件：
  1. **基线睡眠（BSL）**：一周规律睡眠后的一整夜记录。
  2. **慢性睡眠限制（CSR）**：连续7晚每晚仅卧床5小时，取第7晚的记录进行分析。
  3. **急性睡眠剥夺（ASD）**：40小时持续觉醒后的恢复夜记录。
  - 为了便于比较，所有记录被截短为295分钟（即5小时），与CSR时长一致。
  - 实验中禁止日间小睡、药物、酒精和咖啡因。
- **基准（benchmark）**：本研究没有与其他现有方法进行对比，而是将SSA指标与传统的基于AASM标准的睡眠分期参数（如各阶段比例、潜伏期、效率、碎片化指数）进行同期检验和对比。
- **统计方法**：由于数据不满足正态性，使用Wilcoxon符号秩检验进行两两比较（BSL vs CSR，BSL vs ASD，CSR vs ASD），并采用Bonferroni校正调整p值（乘以3）。所有分析在SPSS和MATLAB中完成。

### 4. 资源与算力

- **文中未提及任何GPU或专用计算硬件资源**。状态空间分析的运算量较小（基于功率谱密度、欧氏距离、核密度估计），估计在普通CPU（例如Intel i5/i7）上即可在几分钟到几十分钟内完成全部数据处理。作者明确使用了MATLAB R2018b运行算法。因此，本研究的算力需求非常低，不需专用算力。

### 5. 实验数量与充分性

- **实验数量**：
  - 共14名受试者 × 3个条件 = 42次夜间记录（但并非所有对比均有效，因为每名受试者在每个条件下只有一次记录）。
  - 主要分析包括：
    - 传统睡眠分期参数对比（表1）。
    - 状态空间中的簇质心位置（表2）、质心间距离（表3）。
    - 峰-峰距离（表4）、重叠面积（表5）。
    - 稳定epoch数量与比例（表6）。
    - 碎片化指数（图3）和过渡期数量（图4）。
  - 所有统计检验均为成对比较，无消融实验或交叉验证。
- **充分性评价**：
  - **优点**：实验设计为随机交叉、对照，且在同一批受试者内比较，消除了个体差异干扰，置信度较高。结果在统计上取得了显著差异（经过Bonferroni校正），方法学严谨。
  - **不足**：
    - 样本量较小（仅14人），且全部为年轻男性，无法推广到女性、老年或临床人群。
    - 仅有一个数据集（来自同一研究中心的同一研究），缺乏外部验证。
    - 仅比较了三种条件，没有设置其他类型的睡眠剥夺或恢复条件作为对照。
    - 由于记录被截短至5小时，可能会错过睡眠后期（REM较多、微觉醒较多）的效应，导致对整体睡眠结构的代表性有偏差。
    - 没有与传统的频谱分析方法（如绝对功率、慢波活动斜率）进行系统性对比，无法直接证明SSA提供了独特的增量信息。
    - 部分分析（如觉醒状态）由于睡眠压力高导致觉醒epoch数量极少，统计效力较低。

### 6. 论文的主要结论与发现

- **CSR效应**：主要导致REM睡眠与觉醒的频谱特征更加相似（簇质心距离显著减小、峰-峰距离减小、重叠面积增大），即**REM与觉醒的状态边界变模糊**。但REM本身的稳定性（稳定epoch比例）没有改变，仅REM总量增加。
- **ASD效应**：主要影响NREM睡眠（N2和N3簇在y方向显著移位，反映sigma频段活动降低），并导致**慢波睡眠（N3）的稳定性显著增强**（稳定epoch数量及比例均显著增加），而REM与觉醒的边界变化不明显。
- **状态边界与动力学独立**：CSR降低了状态边界但未改变稳定性，ASD增强了稳定性但边界变化主要体现在NREM内，表明这两个维度可以独立调制。
- **与常规睡眠分期的对应**：常规睡眠分期显示CSR显著增加REM%，ASD显著增加N3%，与SSA结果一致，但SSA能进一步揭示频谱组成相似性和稳定性等额外特征。
- **潜在临床应用**：由于健康受试者在不同睡眠缺失条件下出现可量化的差异化变化，说明SSA指标具有状态依赖性，未来可用于区分正常睡眠调节与病理性状态（如发作性睡病中的REM-觉醒边界模糊+不稳定），也可能用于评估失眠或睡眠不足综合征的治疗效果。

### 7. 优点：方法或实验设计上的亮点

- **方法创新性**：将状态空间分析引入睡眠剥夺研究，首次在同一受试者内比较急性和慢性睡眠缺失对状态边界和动力学的不同影响。
- **定量化进步**：SSA提供了超越传统分期的定量指标（簇距离、重叠面积、稳定epoch比例、过渡次数），能更精细地描述睡眠的“边界模糊性”和“稳定性”。
- **严谨的实验设计**：随机交叉对照，受试者内比较，消除了个体差异；使用统一的截短时长以消除记录时长差异；统计检验采用非参数检验并作多重比较校正。
- **结果解释清晰**：将SSA结果与传统睡眠分期结果相互印证，增强了结论的可信度；并且区分了“状态边界”和“稳定性”两个独立维度，提供了新的理论见解。

### 8. 不足与局限

- **样本代表性差**：仅14名健康年轻男性，无法推广到女性、老年、女性或患有睡眠障碍的人群。作者也承认未来需要研究性别、年龄的影响。
- **数据截断带来的偏差**：将全部记录缩短为5小时，丢失了正常睡眠后期（通常更多REM和微觉醒）的信息，可能改变了簇的总体组成和动力学指标。
- **觉醒epoch过少**：CSR和ASD条件下觉醒极多减少，关于觉醒的分析统计效力不足，需谨慎解释。
- **缺乏外部验证**：所有数据来自同一个研究中心的同一个实验，没有在其他独立数据集中复现结果。
- **未与已建立的方法对比**：没有将SSA指标与流行的睡眠微结构分析（如慢波活动斜率、纺锤波密度、循环交替模式）进行比较，以证明其增量价值。
- **未提及顺序效应或洗脱期**：虽然原文提到至少两周洗脱期，但未对可能的条件顺序效应进行统计控制（尽管交叉设计可平衡）。
- **算力需求未提及**：虽然算力需求低，但未报告具体运算时间，未来复现的细节稍微不足。
- **结果的可重复性**：由于样本量小且使用非参数检验，个别显著结果可能是偶然发现，需要更大样本和预注册研究验证。

（完）
