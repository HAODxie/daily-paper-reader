---
title: "Seamless interaction in VR: decoding user intent with eye gaze and passive brain-computer interfaces"
title_zh: VR中的无缝交互：利用眼动和被动脑机接口解码用户意图
authors: "Pan, Y., Rabe, L., Zander, T., Klug, M."
date: 2026-07-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.06.736575v1.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 使用基于EEG的被动脑机接口在虚拟现实中解码交互意图
tldr: "VR交互依赖显式运动输入，限制自然交互。本研究提出结合眼动与基于EEG的被动脑机接口，在动态VR游戏中解码交互意图（包括affordance评价和趋避评价）。离线分类准确率66.28%，在线闭环游戏达69.64%，特定类别最高80.84%。用户体验显示BCI范式比传统控制器更有趣。这是首次在动态VR中实时解码交互意图，为沉浸式环境中的自适应生理接口奠定基础。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-06-736575-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1358, \"height\": 837, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-06-736575-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1290, \"height\": 1011, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-06-736575-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 783, \"height\": 1375, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-06-736575-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1283, \"height\": 1045, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-06-736575-v1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1241, \"height\": 1036, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-06-736575-v1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1189, \"height\": 1409, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-06-736575-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1359, \"height\": 414, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-06-736575-v1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1330, \"height\": 434, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-06-736575-v1/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1214, \"height\": 739, \"label\": \"Table\"}]"
motivation: 现有VR交互依赖显式操作，缺乏直觉性。本研究探索是否能用眼动和被动BCI解码交互意图，实现无缝适应。
method: 23名参与者玩VR游戏，包含校准和在线BCI会话。通过EEG和眼动数据解码交互意图的两个成分：affordance评价和趋避评价。
result: "离线趋避分类准确率66.28%，在线达69.64%；affordance评价准确率77.76%-83.50%。用户体验中BCI范式更有趣。"
conclusion: 首次在动态VR中实时解码交互意图，BCI可增强交互自然性，尽管有控制感损失。
---

## 摘要
虚拟现实（VR）交互目前仍主要依赖显式的运动输入，限制了无缝和自适应的交互。本研究探讨了基于脑电图（EEG）的被动脑机接口（BCI）与眼动相结合，是否可以在动态VR游戏过程中直接从其潜在的神经生理关联中解码交互意图。我们将交互意图操作化为两个组成部分：可供性相关评估，指示被关注的物体是否提供交互；以及趋避评估，指示交互朝向期望或不期望结果的倾向性。23名参与者完成了一个VR游戏，包括两个校准环节和一个在线BCI环节。离线分析显示，在所有可操作试验中，二元趋避决策分类的解码效果高于随机水平，参与者间的总体平均准确率为66.28%。这种解码效果转移到了在线闭环游戏过程中，总体平均准确率仍高于随机水平，达到69.64%。类别层面的分析进一步揭示了分类可分离性的显著变异性。对于趋避相关的分类，在明确效价的奖励和惩罚类别之间的最明显配对中，准确率达到80.84%，但在更依赖上下文且动机效价模糊的配对中，准确率下降至接近随机水平的59.03%。在不可操作和可操作物品类别之间的可供性相关分类始终较高，范围在77.76%至83.50%之间。用户体验问卷结果显示，尽管存在局限性导致感知控制感丧失和易用性降低，但参与者发现基于BCI的交互范式本身比控制器基线更有趣。据我们所知，这是在动态VR游戏过程中实时EEG解码交互意图的首次演示，为在沉浸式环境中由生理信号驱动的直观用户自适应界面做出了贡献。

## Abstract
Virtual reality (VR) interaction remains largely dependent on explicit motor input, limiting seamless and adaptive interaction. This study investigated whether electroencephalography (EEG)-based passive brain-computer interfaces (BCIs), combined with eye gaze, can decode interaction intent directly from its underlying neurophysiological correlates during dynamic VR gameplay. We operationalized interaction intent as comprising two components: affordance-related evaluation, indicating whether an attended object affords interaction, and approach-avoidance evaluation, indicating the directional tendency of interaction toward desirable or undesirable outcomes. Twenty-three participants completed a VR game with two calibration sessions and one online BCI session. Offline analyses showed above-chance decoding of the binary approach-avoidance decision classification across all actionable trials, with a grand-average accuracy of 66.28% across participants. This decoding transferred to online closed-loop gameplay, where grand-average accuracy remained above chance at 69.64%. Category-level analyses further revealed substantial variability in classification separability. For approach-avoidance-related classifications, accuracy reached 80.84% for the most distinct pairing between clearly valenced reward and punishment categories, but dropped to near chance at 59.03% for the more context-dependent pairing with ambiguous motivational valence. Affordance-related classifications between non-actionable and actionable item categories were consistently high, ranging from 77.76% to 83.50%. User Experience questionnaire results showed that, despite limitations leading to perceived loss of control and reduced ease of use, participants found the BCI-based interaction paradigm itself more fun than the controller baseline. To our knowledge, this is the first demonstration of real-time EEG decoding of interaction intent during dynamic VR gameplay, contributing toward intuitive user-adapted interfaces driven by physiological signals in immersive environments.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：当前虚拟现实（VR）交互主要依赖显式运动输入（如手柄、手部追踪），导致交互摩擦、任务中断、对运动能力受限用户不友好，且系统无法感知用户的认知状态（如意图、工作负荷）。
- **整体含义**：论文旨在探索是否可以利用**眼动**（提供空间目标）和**被动脑机接口（pBCI）**（解码认知状态）相结合，在动态VR游戏过程中直接解码用户的“交互意图”，从而实现更无缝、自适应的交互。这是首次在动态VR场景中实现实时EEG意图解码的尝试，为神经自适应HCI提供了新范式。

### 2. 论文提出的方法论：核心思想、关键技术细节、算法流程

- **核心思想**：将“交互意图”操作化为两个可分离的成分：
  - **可供性评估（affordance evaluation）**：判断被注视物体是否可交互（二分类：可操作 vs 不可操作）。
  - **趋避评估（approach–avoidance evaluation）**：判断交互的方向（二分类：采取 vs 丢弃），即用户期望获得奖励还是避免惩罚。
- **关键技术细节**：
  - **EEG信号处理**：64通道EEG（actiCAP slim），采样率500Hz，重采样至250Hz；带通滤波0.1–15 Hz；共同平均参考；离线分割时窗：-200 to 1000 ms相对物品呈现时刻，基线校正；特征提取：0–800 ms窗口内每50 ms取平均幅度，形成64×16=1024维特征向量。
  - **分类器**：正则化线性判别分析（RLDA）带自动协方差收缩和类别平衡；使用5折时间交叉验证评估离线性能。
- **算法/流程**：
  1. **校准阶段**：用户用手柄执行动作（take/discard），记录EEG和标签，训练二分类器（take vs discard）。
  2. **在线阶段**：预训练分类器实时解码EEG（约300ms延迟），预测的意图通过LSL传给Unity自动执行动作；用户仅在系统错误时通过按钮纠正（提供在线标签）。
  3. **事后分析**：使用ICA（AMICA）去除眼动和肌肉伪迹，并重新训练分类器对不同物品类别配对进行分析。

### 3. 实验设计：数据集/场景、基准、对比方法

- **数据集/场景**：自制的VR游戏（Unity实现），参与者坐在Meta Quest Pro头显中，通过眼动注视飞来的岩石并停下，然后评估内部物品决定take或discard。物品包括：硬币（奖励）、炸弹（惩罚）、食物（上下文相关奖励）、盔甲（上下文相关奖励）、岩石碎片（不可操作）。任务难度随时间增加。
- **基准**：离线分类以模拟随机水平为基准（二项分布模拟，p=0.05）；在线分类同样以模拟随机水平为基准；用户体验以控制器基线为基准（问卷7点Likert量表，4=与控制器相同）。
- **对比方法**：论文未对比其他机器学习或BCI方法（如SVM、CNN），主要聚焦于所提RLDA在离线/在线、不同类别配对上的性能差异，以及用户体验上BCI与控制器的主观对比。

### 4. 资源与算力

- **文中未明确说明具体的GPU型号、数量、训练时长等算力信息**。仅提到实验用计算机配置：AMD Ryzen 7 5800X 8核处理器、NVIDIA GeForce RTX 3070 Ti。EEG处理在MATLAB中使用EEGLAB和BCILAB完成，在线分类延迟约300ms，表明计算资源要求不高。

### 5. 实验数量与充分性

- **实验数量**：
  - 校准阶段：2个session，每个session 4个wave，共约493个有效试验/人（离线分析19人）。
  - 在线阶段：1个session，4个wave，约260个有效试验/人（18人）。
  - 事后分析：对7种不同类别配对进行二分类（如coins vs bombs, coins vs rock等）。
  - 用户体验：18人填写问卷，包含当前BCI和理想BCI两个条件的8个维度评价。
- **充分性**：
  - **优点**：覆盖了离线、在线、事后分析，并包含主观评价；使用统计检验（模拟随机水平、Wilcoxon符号秩检验）确保结果可靠性；在线准确率经保守调整后仍高于随机。
  - **不足**：
    - 未进行消融实验（如不同特征组合、不同分类器对比）。
    - 样本量较小（19/18），可能限制统计功效。
    - 在线标签通过用户反馈获得，存在响应误差（平均4.35%），虽然手动排除了一名超标参与者，但仍有残余误差。
    - 控制器基线未作为完全匹配的实验条件（固定顺序，非平衡设计），用户体验对比可能受顺序效应影响。

### 6. 论文的主要结论与发现

- 离线二分类（take vs discard）平均准确率66.28%，高于随机水平；在线闭环准确率69.64%（保守调整后约65.29%），表明意图解码可以从校准转移到实际游戏。
- 类别层面分析表明：
  - **可供性评估**（可操作 vs 不可操作）分类准确率持续高（77.76%–83.50%），说明EEG能可靠区分物体是否可交互。
  - **趋避评估**在明确效价（硬币 vs 炸弹）时准确率达80.84%，但在上下文依赖（非硬币take vs 非炸弹discard）时降至59.03%（接近随机），表明趋避解码受决策模糊性影响。
- 用户体验：当前BCI系统相比控制器更有趣，但控制感、易用性、满意度更低；理想BCI（高准确率、低延迟）的评分普遍优于控制器，说明局限性主要源于技术性能而非概念本身。

### 7. 优点

- **创新性**：首次在动态VR游戏中实现实时EEG意图解码，突破以往仅离线或依赖代理信号（如SPN）的方法。
- **方法论严谨**：明确将交互意图分解为可供性和趋避两个神经可分离的成分，并分别验证其可解码性。
- **实验设计完整**：包含校准、在线闭环、事后分析、用户体验评估，并控制了响应错误率（15%排除标准）。
- **转化验证**：离线训练的模型成功在线运行，并保持高于随机水平的性能。
- **开放性**：代码、数据、材料均公开（GitHub/Zenodo）。

### 8. 不足与局限

- **样本量小**（N=19/18），且参与者主要为年轻健康人群，缺乏代表性。
- **视觉混淆**：不同物品类别（如硬币更亮）存在视觉特征差异，无法完全排除低层知觉因素对EEG信号的贡献。
- **在线标签质量**：依赖用户手动纠错，可能遗漏或误判，影响在线准确率评估的准确性。
- **缺乏多模态融合**：仅使用EEG特征，未结合瞳孔、微眼动等眼动特征提升分类性能。
- **实验环境限制**：实验室条件且需要导电凝胶EEG，实用性受限；未来需发展干电极或头显集成系统。
- **未进行消融与基准对比**：没有比较不同分类器、不同特征窗口、是否使用ICA等对性能的影响，也未与其他BCI范式（如基于P300或错误电位）对比。
- **用户经验评估**：控制器基线为固定顺序，可能存在顺序效应；理想BCI条件为假设性评分，与实际体验脱节。

（完）
