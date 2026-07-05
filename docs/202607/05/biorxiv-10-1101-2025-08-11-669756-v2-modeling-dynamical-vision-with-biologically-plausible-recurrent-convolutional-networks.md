---
title: Modeling Dynamical Vision with Biologically Plausible Recurrent Convolutional Networks
title_zh: 使用生物合理的循环卷积网络对动态视觉进行建模
authors: "Gutzen, R., Lindsay, G. W."
date: 2026-06-26
pdf: "https://www.biorxiv.org/content/10.1101/2025.08.11.669756v2.full.pdf"
tags: ["query:neuro-mental"]
score: 8.0
evidence: 生物合理的递归卷积网络用于视觉神经科学
tldr: "标准卷积神经网络缺乏生物视觉皮层中的递归连接，难以模拟自适应、延迟归一化和噪声鲁棒等时空现象。为此，我们提出DynVision开源工具箱，采用配置驱动设计，支持五种递归类型和异构延迟的ODE求解器，计算效率提升52%。系统参数探索表明，递归整合目标和损失计算时间窗口等建模选择对动态特性影响显著。连续时间递归可自然产生皮层时间现象，无需显式归一化，且特定配置的噪声鲁棒性接近人类水平，凸显了构建统一建模框架的必要性。"
source: biorxiv
selection_source: carryover_cache
motivation: 现有前馈CNN缺乏递归连接，无法捕捉视觉皮层的时空动力学现象。
method: 开发模块化开源工具箱DynVision，实现含异构延迟的ODE求解器，支持五种侧向递归类型。
result: 递归配置选择显著影响动态特性，连续时间递归自发产生皮层现象，噪声鲁棒性接近人类。
conclusion: 不同递归配置功能各异，需综合性建模框架以探索生物视觉的完全真实模型。
---

## 摘要
摘要：用于图像识别的卷积神经网络（CNN）已被证明与灵长类动物腹侧视觉通路具有显著的概念相似性，但其标准的前馈架构缺乏视觉皮层中普遍存在的循环连接。这种循环被认为构成时空现象的基础，包括适应、延迟归一化以及对噪声输入的鲁棒性。然而，将功能有益的循环纳入CNN以捕捉生物视觉的时空现象仍然具有挑战性。尽管最近的进展已纳入神经生物学约束，但该领域缺乏可访问的工具来系统地比较不同架构选择（例如循环类型、时间延迟和连接模式）如何塑造神经动力学和行为。在此，我们介绍DynVision，一个模块化的开源工具箱，用于构建和评估生物合理的循环卷积神经网络（RCNN）。DynVision实现了具有异构延迟的数值ODE求解器，支持五种类型的横向循环，从简单的自连接到皮层组织的局部循环，并通过配置驱动的设计将科学建模决策与实现细节分开。训练计算效率高，比参考实现加速52%。我们通过系统探索参数空间来演示该框架，揭示时间动力学的定性差异对通常隐含的建模选择（如循环整合的目标位置和损失计算的时间窗口）高度敏感。关键的是，我们发现连续时间循环动力学可以自然地产生皮层时间现象，而无需显式的分式归一化，而不同的循环配置则产生接近人类水平的噪声鲁棒性。这些发现提示了功能上不同的循环配置，并强调了创建完全现实模型的挑战，从而突出了需要一个全面且连贯的建模框架来辅助探索。代码和文档可在https://github.com/Lindsay-Lab/DynVision/获取。

## Abstract
AO_SCPLOWBSTRACTC_SCPLOWConvolutional Neural Networks (CNNs) trained for image recognition have demonstrated remarkable conceptual similarities to the primate ventral visual pathway, but their standard feedforward architectures lack the recurrent connections that are ubiquitous in visual cortex. Such recurrence is thought to underlie spatiotemporal phenomena including adaptation, delayed normalization, and robustness to noisy input. However, incorporating functionally beneficial recurrence into CNNs that captures spatiotemporal phenomena of biological vision remains challenging. Although recent advances have incorporated neurobiological constraints, the field lacks accessible tools for systematically comparing how different architectural choices, such as recurrence type, temporal delays, and connectivity patterns, shape neural dynamics and behavior. Here, we introduce DynVision, a modular open-source toolbox for constructing and evaluating biologically plausible recurrent convolutional neural networks (RCNNs). DynVision implements numerical ODE solvers with heterogeneous delays, supports five types of lateral recurrence ranging from simple self-connections to cortically-organized local recurrence, and separates scientific modeling decisions from implementation details through a configuration-driven design. Training is computationally efficient, achieving a 52% speedup over reference implementations. We demonstrate the framework through systematic exploration of the parameter space, revealing that qualitative differences in temporal dynamics are highly sensitive to often-implicit modeling choices such as the target location of recurrent integration and the temporal window used for loss computation. Critically, we find that continuous-time recurrent dynamics can naturally give rise to cortical temporal phenomena without requiring explicit divisive normalization, while a different recurrent configuration produces noise robustness approaching human-level performance. These findings suggest functionally distinct configurations of recurrence and highlight the challenge of creating fully realistic models, thus emphasizing the need for a comprehensive and cohesive modeling framework to aid exploration. Code and documentation are available at https://github.com/Lindsay-Lab/DynVision/.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：标准前馈卷积神经网络（CNN）虽然与灵长类腹侧视觉通路有概念相似性，但缺失视觉皮层中普遍存在的递归连接。这种递归连接被认为是产生适应、延迟归一化、对噪声输入鲁棒性等时空动力学现象的基础。然而，如何将功能有益的递归整合到CNN中以捕捉生物视觉的时空现象仍面临挑战，且当前缺乏可访问的工具来系统比较不同架构选择（如递归类型、时间延迟、连接模式）对神经动力学和行为的影响。
- **整体含义**：本文旨在提供一个统一的建模框架，通过开发开源工具箱DynVision，使研究者能够比较不同递归配置在模拟生物视觉时空现象中的功能差异，从而推进对生物视觉真实模型的理解。

### 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：构建模块化、配置驱动的循环卷积神经网络（RCNN）工具箱，将科学建模决策与实现细节分离，支持灵活的实验设计。
- **关键技术细节**：
  - 实现了具有**异构延迟**的数值ODE求解器（连续时间动力学）。
  - 支持**五种类型的横向递归**：从简单的自连接到皮层组织的局部循环连接。
  - 采用**配置驱动设计**：通过配置文件定义递归类型、时间延迟、连接模式等参数，无需修改底层代码。
  - 训练计算效率高，比参考实现加速**52%**（通过优化实现细节）。
  - 递归整合的目标位置（如残差连接或旁路连接）和时间窗口（用于损失计算）可作为可调参数。

### 3. 实验设计：数据集、基准与对比方法

- **数据集**：摘要中未明确指明具体图像数据集。推测可能是标准图像识别数据集（如ImageNet等），但文中未给出名称。
- **基准**：以参考实现（可能是标准前馈CNN或现有RCNN实现）为基准，评估训练速度（52%加速）。
- **对比方法**：
  - 系统探索参数空间，比较不同递归配置（五种类型）下的时间动力学行为。
  - 对比不同建模选择的影响：递归整合的目标位置、损失计算的时间窗口等。
  - 噪声鲁棒性实验：对比人类水平噪声鲁棒性（未明确具体人类实验基准）。
  - 未提及与其他现有生物视觉模型（如HMAX、PredNet等）的直接性能比较。

### 4. 资源与算力

- **文中未明确说明**：未提及GPU型号、数量或具体训练时长。仅提到“训练计算效率高，比参考实现加速52%”，但未给出参考实现的算力细节。
- **结论**：无法从摘要中获取算力信息；需查阅全文或代码仓库。

### 5. 实验数量与充分性

- **实验数量**：主要进行了**系统参数空间探索**，包括：
  - 不同递归类型的定性比较（五种）
  - 建模选择（整合目标位置、损失时间窗口）的敏感性分析
  - 噪声鲁棒性测试（与人类水平对比）
  - 未提及具体的消融实验组数或数据集数量。
- **充分性与客观性**：
  - **优点**：实验设计系统，揭示了不同递归配置对动力学影响的敏感性，强调了隐含假设的重要性。
  - **局限**：缺少与其他SOTA生物模型或标准CNN在相同基准下的定量比较；未报告在标准图像识别任务（如ImageNet）上的准确率；噪声鲁棒性实验可能仅基于合成噪声，未涉及真实视觉噪声；实验覆盖可能不足（如未探索不同延迟模式组合、深层网络结构等）。
  - **公平性**：代码开源促进复现，但需完整论文确认实验细节。

### 6. 论文的主要结论与发现

- **连续时间递归动力学可自然地产生皮层时间现象**：无需显式的分式归一化机制，即可模拟适应、延迟归一化等行为。
- **递归配置选择显著影响动态特性**：不同递归类型（自连接 vs. 局部循环）产生定性不同的时间动力学。
- **噪声鲁棒性接近人类水平**：特定递归配置（未明确指定）在噪声环境下达到类似人类的鲁棒性。
- **建模选择高度敏感**：递归整合的目标位置和损失计算时间窗口等隐含参数对结果有显著影响。
- **统一建模框架的必要性**：不同递归配置功能各异，完全真实的生物视觉模型需要综合考虑各种连接模式。

### 7. 优点

- **开源模块化：DynVision** 提供配置驱动设计，降低实验门槛，促进可重复性。
- **支持异构延迟和多种递归类型**：覆盖简单到皮层组织的递归模式，灵活性高。
- **计算效率提升52%**：优化后训练速度显著快于参考实现。
- **关键发现具有启发性**：连续时间递归自发产生皮层现象，无需显式归一化，为生物视觉建模提供了新视角。
- **系统参数探索**：揭示了对建模选择的高度敏感性，有助于避免冗余假设。

### 8. 不足与局限

- **实验覆盖不全面**：未在主流基准数据集（如ImageNet）上评估标准识别性能，难以与现有CNN或生物模型直接比较。
- **缺少与现有模型的对比**：未对比其他生物约束RCNN或神经科学模型（如PredNet、局部回路模型）。
- **噪声鲁棒性实验细节缺失**：未说明人类数据来源、噪声类型及测试条件，结论推广需谨慎。
- **算力与训练细节未披露**：无法判断计算成本及应用可行性。
- **应用限制**：主要面向生物视觉科学建模，可能不直接适用于工程任务（如实时视频处理）。
- **偏差风险**：参数空间探索可能偏向于证明框架有效性，需独立第三方验证。

（完）
