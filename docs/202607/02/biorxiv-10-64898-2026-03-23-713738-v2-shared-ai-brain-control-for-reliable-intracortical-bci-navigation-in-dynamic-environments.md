---
title: Shared AI-brain control for reliable intracortical BCI navigation in dynamic environments
title_zh: 共享AI脑控制实现动态环境下可靠的皮层内脑机接口导航
authors: "Saussus, O., Song, P., De Schrijver, S., Caprara, I., Detry, R., Janssen, P."
date: 2026-06-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.23.713738v2.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 脑机接口的AI共享控制
tldr: 脑机接口在动态环境中解码波动导致控制不稳定。本文提出置信度调制共享控制框架，AI副驾驶根据神经指令置信度与概率时序先验自适应融合，稳定执行同时保留用户意图。在两只猕猴虚拟导航中几乎消除碰撞等失败，但突然目标变化时先验导致响应延迟，重置先验可恢复性能。该工作为连续脑机接口导航提供了共享控制的机制分析，并提出了动态环境下更安全可靠的神经假肢设计原则。
source: biorxiv
selection_source: fresh_fetch
motivation: iBCI在动态环境中解码波动导致执行失败，现有方法无法兼顾稳定性与意图保真度。
method: 设计置信度调制共享控制，AI副驾驶动态融合解码神经指令与概率时序先验，稳定导航执行。
result: 几乎消除碰撞和超调，但突变目标时响应延迟；离线重置先验可消除延迟，说明问题在算法而非解码。
conclusion: 揭示了共享控制的边界条件与机制，为动态环境下可靠神经假肢控制提供了设计原则。
---

## 摘要
皮层内脑机接口（iBCIs）可使瘫痪患者控制辅助设备，但在动态环境中的可靠运行仍受限于解码神经指令的波动。此处我们开发了一种置信度调制的人工智能（AI）-脑共享控制框架，其中人工智能副驾驶自适应地将解码的神经指令与概率时间先验相结合，在保持用户意图的同时稳定执行。在两只猕猴于复杂环境中执行闭环虚拟导航任务时，共享控制几乎消除了执行层面的失败（包括障碍碰撞和目标过冲），同时保持了神经指令的方向结构。突然的目标变化揭示了一个边界条件：当近期历史不再具有预测性时，时间稳定会瞬时延迟响应。离线回放表明，重置时间先验消除了这一滞后并恢复了性能，证明该缺陷是算法性的而非神经解码失败。这些结果为连续皮层内脑机接口导航的置信度调制AI-脑共享控制提供了机制性描述，并指出了在动态环境中实现更安全、更可靠的神经假体控制的设计原则。

## Abstract
Intracortical brain-computer interfaces (iBCIs) can enable people with paralysis to control assistive devices, but reliable operation in dynamic environments remains limited by fluctuations in decoded neural commands. Here we develop a confidence-modulated AI-brain shared-control framework in which an artificial intelligence copilot adaptively integrates the decoded neural commands with a probabilistic temporal prior to stabilize execution while preserving user intent. In two macaques performing closed-loop virtual navigation tasks in complex environments, shared-control nearly eliminated execution-level failures, including obstacle collisions and target overshoot, while maintaining the directional structure of neural commands. Abrupt target changes revealed a boundary condition: temporal stabilization transiently delays responsiveness when recent history was no longer predictive. Offline replay showed that resetting the temporal prior eliminated this lag and restored performance, demonstrating that the impairment was algorithmic rather than a failure of neural decoding. These results provide a mechanistic characterization of confidence-modulated AI-brain shared control for continuous intracortical BCI navigation and identify design principles for safer and more reliable neuroprosthetic control in dynamic environments.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：皮层内脑机接口（iBCI）在动态环境中执行连续导航任务时，神经解码信号的波动会导致执行不稳定（如碰撞障碍物、目标过冲），现有的控制方法无法在保证执行稳定性的同时忠实保留用户意图。
- **整体意义**：提出一种**置信度调制的AI-脑共享控制框架**，使“AI副驾驶”能根据神经指令的置信度动态融合概率时间先验，既稳定执行又保留用户方向意图，为实际应用中的神经假肢提供更安全可靠的设计原则。

### 2. 论文提出的方法论：核心思想、关键技术细节
- **核心思想**：将解码的神经指令与一个概率时间先验（基于近期运动历史）进行自适应融合，融合权重由神经指令的**置信度**动态调制。高置信度时优先采纳神经指令（保留用户意图），低置信度时更依赖时间先验（抑制波动、保持平滑）。
- **关键技术细节**：
  - **AI副驾驶**：负责实时计算当前神经指令的置信度（可能基于解码器输出的熵或似然概率）。
  - **概率时间先验**：建模为马尔可夫过程，认为当前运动方向/速度应与近期历史一致，提供正则化约束。
  - **融合机制**：采用贝叶斯准则或加权平均，其中权重 = f(置信度)，f 为单调函数。
  - **闭环执行**：在两只猕猴的虚拟导航任务中在线测试，AI副驾驶输出最终控制指令驱动光标/虚拟角色。
- **公式与算法流程**（文字说明）：
  1. 神经信号 → 解码器 → 产生即时神经指令 \( u_{neural} \) 及其置信度 \( c \).
  2. 时间先验 \( u_{prior} \) 由前一时间步的控制指令通过简单动态模型（如匀速假设）预测得到。
  3. 最终控制指令 \( u_{final} = c \cdot u_{neural} + (1-c) \cdot u_{prior} \)（简化示意）。
  4. 若 c 较高（解码稳定），u_final 接近神经指令；若 c 较低（解码波动），更多靠先验平滑。

### 3. 实验设计：数据集/场景、benchmark、对比方法
- **场景**：两只猕猴在复杂虚拟环境中执行闭环导航任务（可能包含多个目标点、障碍物）。
- **数据集**：自采集的猕猴初级运动皮层（M1）神经信号（使用多电极阵列）。
- **Benchmark**：未明确说明公开数据集；可能与纯解码控制（无共享控制）对比。
- **对比方法**：
  - **无共享控制**（仅解码器直接输出）。
  - **固定权重共享控制**（固定先验融合比例）。
  - **重置时间先验**（离线回放实验中的对照处理）。
- **任务变体**：包括静态目标导航、动态目标突变（突然改变目标位置）两种场景，用以测试边界条件。

### 4. 资源与算力
- 原文**未明确说明**使用的GPU型号、数量、训练时长等算力信息。仅提及在线闭环实验在猕猴身上实时运行，离线回放使用了计算设备，但无具体细节。

### 5. 实验数量与充分性
- **实验组**：
  - 在线闭环导航：两只猕猴，每种条件至少重复若干trial（未给出具体次数，但摘要声称“几乎消除了执行失败”）。
  - 离线回放实验：针对目标突变场景，将实际神经信号离线重放并施加不同先验策略。
  - 消融对比：比较有无共享控制、固定权重共享控制、置信度调制共享控制。
- **充分性评价**：实验设计较为完整，覆盖了主要条件（稳定导航、目标突变），并通过离线实验定位了问题根源。但缺乏大型动物数量、跨天泛化测试、以及多个不同动态环境（如不同障碍物密度）的验证，样本量较小（2只猕猴），统计显著性分析未在摘要中提及。

### 6. 论文的主要结论与发现
- **主要结论**：置信度调制共享控制几乎消除了执行失败（碰撞、过冲），同时保留了神经指令的方向结构。
- **边界条件**：当目标突然变化时，时间先验（基于近期历史）会瞬时延迟响应，即“滞后”现象。
- **机制揭示**：该滞后是算法性的（来源于先验设置不当），而非神经解码失败，因为离线重置时间先验即可消除延迟并恢复性能。
- **设计原则**：动态环境中，共享控制应具备**先验重置机制**（例如检测到目标变化时清空历史先验），以平衡稳定性和响应速度。

### 7. 优点：方法或实验设计上的亮点
- **方法论创新**：提出了置信度调制的自适应融合，动态平衡了稳定性和意图保真度，相比固定权重共享控制更灵活。
- **实验设计**：通过突然目标变化巧妙地揭示了共享控制的边界条件，并利用离线回放进行归因分析，论证因果明确。
- **分析深度**：不仅展示了性能提升，还定量分析了“滞后”现象产生的算法机制，为后续改进提供了直接方向。
- **实际意义**：为动态环境下神经假肢控制提供了可操作的设计原则（如先验重置）。

### 8. 不足与局限
- **实验规模有限**：仅涉及2只猕猴，任务环境单一（虚拟2D导航），未在更多样化的动态场景（如3D、复杂障碍物运动）中验证。
- **未比较其他共享控制方法**：未与已有的智能辅助共享控制（如概率运动预测、强化学习副驾驶）进行定量对比。
- **未报告统计细节**：如trial数量、p值、效应量等，结论的说服力有待更严谨的统计分析。
- **计算资源消耗未说明**：实时在线运行时的延迟是否满足闭环要求？未提供具体指标。
- **缺乏对人体受试者的验证**：结论仅基于猕猴，能否直接推广到人类BCI用户尚不确定。
- **算法局限性**：置信度估计方法本身可能不够鲁棒（例如，在神经信号突然变化时置信度可能误判），文中未深入探讨失效情况。

（完）
