---
title: "Healthy-to-Stroke Translation of EEG-Based BMIs: EEG Characterization and Reinforcement Learning-Based Decoder Evaluation"
title_zh: 基于EEG的BMI从健康到中风的迁移：EEG特征描述与基于强化学习的解码器评估
authors: "Via, Z., Kruse, A., Thapa, B. R., Bae, J."
date: 2026-06-29
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.23.733831v1.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 基于脑电的脑机接口用于中风康复
tldr: "基于脑电的脑机接口有望辅助中风康复，但患者间脑电变异性大。本研究对比健康与急性中风受试者的运动想象脑电特征，利用Q学习核时序差分（Q-KTD）解码器进行迁移学习。结果发现，健康来源迁移学习使58%的中风受试者首次解码成功率提升，平均成功率从49.46%升至51.82%，但部分受试者出现负迁移。该工作为跨群体脑电解码迁移提供了可行性基础，但需个性化策略应对变异性。"
source: biorxiv
selection_source: fresh_fetch
motivation: 验证健康人群训练的解码器能否迁移至急性中风患者，以减少个体校准负担。
method: 分析109健康与50急性中风受试者的运动想象脑电特征，使用Q-KTD解码器进行健康-中风迁移学习。
result: "迁移学习使58%中风受试者首次解码成功率提升，平均成功率从49.46%升至51.82%，最大增益18.75%，但21人负迁移。"
conclusion: 健康来源Q-KTD迁移学习可提升多数急性中风受试者的解码性能，但受试者间变异性大，需个性化迁移或自适应策略。
---

## 摘要
目的：基于脑电（EEG）的脑机接口（BMI）可通过将神经活动转换为外部设备的控制命令，为中风相关运动障碍患者提供辅助技术支持。然而，中风后的神经重组和个体间EEG变异性给可靠解码带来了挑战。本研究描述了健康和中风急性期患者运动想象脑电特征，并评估了基于群体训练的Q学习核时间差分（Q-KTD）解码器能否通过迁移学习改善个体中风解码。这些分析评估了基于EEG的BMI神经解码从健康到中风的迁移可行性。材料与方法：使用公开可用的健康受试者（n=109）和中风急性期患者（n=50）的运动想象脑电数据集，分析左右手运动想象试验。选择这些数据集是因为样本量相对较大且运动想象任务可比。EEG特征描述包括基线期和运动想象期频带功率、ERD/ERS、半球不对称性和时频表示。对于Q-KTD解码，使用运动想象开始后0-0.5秒的滤波时域脑电作为神经状态输入。将在健康群体上训练的Q-KTD模型迁移到个体中风受试者，通过重复蒙特卡洛模拟比较有无迁移学习在多学习轮次中的解码性能。结果：健康和中风急性期参与者表现出共享的运动想象相关EEG结构，包括运动开始后的μ节律抑制，但中风组表现出更大的受试者间变异性、更弥散的时频调制和改变的半球不对称性。经错误发现率校正后，窗口频带功率无通道级健康-中风差异保持显著。健康源迁移学习提高了50名中风参与者中29名（58%）的首轮Q-KTD成功率。在所有参与者中，平均成功率从无迁移学习的49.46%提高到有迁移学习的51.82%。在表现出正迁移的参与者中，平均增益为7.34%，最大增益为18.75%。然而，21名参与者出现负迁移，显示出显著个体水平变异性。结论：健康源Q-KTD迁移学习提高了大多数中风急性期参与者的首轮运动想象BMI解码性能，支持群体信息驱动的Q-KTD解码在中风中的离线可行性。尽管存在显著的受试者间变异性和负迁移，表明需要个体化的迁移选择或适应策略，这些早期性能提升可能减少受试者特定的校准负担。

## Abstract
Purpose: EEG-based brain-machine interfaces (BMIs) may support assistive technologies for individuals with stroke-related motor impairment by translating neural activity into control commands for external devices. However, post-stroke neural reorganization and interindividual EEG variability challenge reliable decoding. This study characterized motor imagery EEG features in healthy and acute stroke participants and evaluated whether population-trained Q-learning Kernel Temporal Difference (Q-KTD) decoders could improve individual stroke decoding through transfer learning. These analyses assess the feasibility of healthy-to-stroke translation for EEG-based BMI neural decoding. Materials and Methods: Publicly available motor imagery EEG datasets from healthy participants (n = 109) and individuals with acute stroke (n = 50) were analyzed using left- and right-hand motor imagery trials. The datasets were selected because of their relatively large sample sizes and comparable motor imagery tasks. EEG characterization included baseline and motor imagery-period band power, ERD/ERS, hemispheric asymmetry, and time-frequency representations. For Q-learning Kernel Temporal Difference (Q-KTD) decoding, filtered time-domain EEG from 0-0.5 s after motor imagery onset was used as the neural-state input. A Q-KTD model trained on the healthy population was transferred to individual stroke participants, and repeated Monte Carlo simulations compared decoding performance with and without transfer learning across multiple learning epochs. Results: Healthy and acute stroke participants showed shared motor imagery-related EEG structure, including post-onset mu-band suppression, while the stroke group exhibited greater interparticipant variability, more diffuse time-frequency modulation, and altered hemispheric asymmetry. No channel-level healthy-stroke differences in windowed band power remained significant after false discovery rate correction. Healthy-source transfer learning improved first-epoch Q-KTD success rates in 29 of 50 stroke participants (58%). Across all participants, mean success rate increased from 49.46% without transfer learning to 51.82% with transfer learning. Among participants showing positive transfer, the mean gain was 7.34% and the maximum gain was 18.75%. However, 21 participants showed negative transfer, demonstrating substantial subject-level variability. Conclusion: Healthy-source Q-KTD transfer learning improved first-epoch motor imagery BMI decoding for a majority of acute stroke participants, supporting the offline feasibility of population-informed Q-KTD decoding in stroke. These early performance gains may reduce subject-specific calibration burden, although substantial interparticipant variability and negative transfer indicate the need for individualized transfer-selection or adaptation strategies.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **研究动机**：脑电图（EEG）脑机接口（BMI）有望为中风后运动障碍患者提供辅助技术，但中风后神经重组及个体间EEG变异性严重阻碍了可靠解码。
- **核心问题**：健康人群训练的运动想象（MI）EEG解码器能否迁移到急性中风患者，以提高首次解码性能并减少患者特定校准负担。
- **整体含义**：验证从健康到中风的“跨群体”迁移学习在EEG-BMI中的可行性，为减少临床校准时间、提高中风患者BMI实用性提供理论基础。

## 2. 论文提出的方法论

- **核心思想**：利用强化学习中的Q-学习核时序差分（Q-KTD）解码器，先在健康群体上训练源模型（学习核中心及权重），再将其直接初始化给每个中风患者的目标模型，实现迁移学习（Transfer Learning, TL）。
- **关键技术细节**：
  - **EEG特征提取**：包括窗口频带功率（0.1-4,4-8,8-13,13-30,30-80Hz）、事件相关去同步/同步（ERD/ERS）、半球不对称指数（ASSI）和时频表示（连续小波变换）。
  - **Q-KTD框架**：将EEG特征向量视为状态\(x(t)\)，解码器输出为动作\(a_i\)，任务反馈为奖励\(r(t+1)\)。利用核函数（高斯核）进行非线性函数逼近，避免表格型Q函数。
  - **更新公式**：时序差分误差\(e_{TD_i}(j) = r(j+1) + \gamma \max_a Q(x(j+1), a) - Q(x(j), a_i)\)，用于更新动作值估计。
  - **核扩展控制**：通过量化阈值\(\zeta_U=0.1\)，仅当新EEG状态与现有核中心距离大于阈值时才添加新核，控制模型复杂度。
- **迁移学习流程**：健康群体数据训练至收敛→保存核中心及权重→直接赋值给每个中风患者模型→继续在线式训练（每个epoch一次决策，模拟中心外伸任务）。

## 3. 实验设计

- **数据集**：
  - **健康组**：PhysioNet EEG Motor Movement/Imagery Dataset（109人，64通道，160Hz采样），仅使用单侧左手/右手运动想象任务（每侧约90-100次试验）。
  - **中风组**：Liu等公开的急性中风数据集（50人，33通道，500Hz采样下采样至160Hz），含40次左右手抓握想象试验，发病1-30天。
- **预处理对齐**：通道统一（29个共享通道）、参考转换为CPz、基线窗口不同（健康用MI前，中风用休息期），使用0.5s和1.0s两种分析窗。
- **对比设置**：每个中风患者进行两种条件——无迁移学习（Non-TL）与健康源迁移学习（TL）。每个条件运行10次蒙特卡洛重复（随机化试验顺序和初始权重），最多50个epoch，早停条件为连续3个epoch平均成功率提升<0.01。
- **基准**：二元解码任务（左/右手），机遇水平为50%。不对比其他迁移方法或静态分类器，仅比较Q-KTD自身有无TL。

## 4. 资源与算力

- **文中未明确说明**：未提及GPU型号、数量、训练时长或任何硬件配置。所有实验均在MATLAB R2025a上完成，但无具体算力信息。

## 5. 实验数量与充分性

- **实验数量**：
  - 生理特征分析：对所有5个频带、29个通道进行窗口频带功率、ERD/ERS、不对称性、时频图的组间比较（健康 vs 中风），并采用FDR校正。
  - 窗口长度比较：对0.5s和1.0s两种分析窗分别计算转移适宜性评分。
  - 解码实验：50个中风患者 × 2条件（TL/Non-TL） × 10次蒙特卡洛重复，共1000次解码运行。
- **充分性与公平性评价**：
  - **优点**：使用了相对较大的健康（109人）和中风（50人）样本，蒙特卡洛重复减少随机性影响；统计采用Welch t检验与FDR校正，控制多重比较。
  - **不足**：
    1. 数据集间存在多种差异（采集系统、参考、任务结构、基线定义），可能混淆结果。
    2. 未进行现实闭环人机交互实验，仅为离线模拟。
    3. 未与其他迁移学习方法（如传统迁移成分分析、域适应）对比。
    4. 未消融分析Q-KTD超参数（如探索率、折扣因子、量化阈值）的影响。
  - 总体而言，实验在单一框架内较充分，但缺乏算法对比和闭环验证，公平性受限于数据集不一致性。

## 6. 论文的主要结论与发现

- **生理特征**：健康和中风组均表现出MI后μ节律抑制，但中风组变异性更大、时频调制更弥散、半球不对称性方向改变。窗口频带功率无FDR校正后显著差异。
- **迁移学习效果**：
  - 平均首轮成功率从49.46%（Non-TL）提升至51.82%（TL），增益2.36%。
  - 29/50（58%）出现正迁移，平均增益7.34%，最大增益18.75%。
  - 21/50出现负迁移，最大降低-14.0%。
- **结论**：健康源Q-KTD迁移学习可改善多数急性中风患者的首轮解码，但绝对成功率仅略高于机遇水平，且负迁移明显。需个性化迁移策略。

## 7. 优点

- **方法创新**：将强化学习迁移框架首次用于健康→中风跨群体EEG运动想象解码，而非传统静态分类。
- **生理分析与解码结合**：深入分析了多个EEG特征（频带功率、ERD/ERS、不对称性、时频图）在两组间的异同，为迁移失败原因提供线索。
- **统计严谨**：使用Welch t检验（不等方差）和FDR校正，避免多重比较假阳性。
- **实验设计合理**：蒙特卡洛重复+早停，评估性能稳定性；个体水平统计分析而非仅群体均值。

## 8. 不足与局限

- **数据集不一致**：健康与中风数据采集系统、参考、任务时序、基线定义不同，可能引入混杂变量。
- **离线模拟**：非真实人机闭环，无法反映用户共适应、疲劳、非平稳性。
- **性能水平低**：迁移后平均首轮成功率仅51.82%，接近机遇水平，实际实用性不足。
- **负迁移存在**：21/50受试者出现负迁移，未深入分析原因（如病灶位置、损伤程度、EEG与健康分布差异）。
- **缺乏对比基准**：未与域适应、协方差对齐等经典迁移方法比较，也未对比无迁移的完整训练曲线（后期收敛性）。
- **超参数未优化**：Q-KTD超参数（γ, ε, ζ_U）固定，未进行个体化调整或消融实验。
- **未明确资源消耗**：无算力或时间统计，可重复性受限。

（完）
