---
title: Effects of EEG Preprocessing on Channel-Wise Attention and Effective Connectivity Alignment in Visual EEG Decoding
title_zh: 脑电图预处理对视觉脑电解码中通道注意力与有效连接对齐的影响
authors: "Elichatiti, V. V., Basari, B., Arif, M., Ikhsan, M."
date: 2026-07-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.02.736026v1.full.pdf"
tags: ["query:neuro-mental"]
score: 8.0
evidence: 研究EEG预处理对基于Transformer的视觉解码的影响
tldr: Transformer模型在视觉EEG解码中表现优异，但其注意力机制与神经连接的对齐尚不明确。本研究对比了基线预处理与综合预处理（ICA+陷波滤波），利用ATM模型评估，并通过节点强度相关性和RSA分析注意力权重与有效连接网络（GPDC、PDC、DTF）的结构对应。综合预处理有效抑制伪迹，保持解码精度，且注意力模式的广泛空间组织跨管道稳定，捕获关键定向连接动态。工作为将数据驱动注意力与神经生理一致性对齐提供了经验性探索，促进更透明的脑机接口。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1784, \"height\": 1338, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1862, \"height\": 1063, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1876, \"height\": 824, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1871, \"height\": 1063, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1875, \"height\": 1137, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1855, \"height\": 1043, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 918, \"height\": 454, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 927, \"height\": 804, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 906, \"height\": 730, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 942, \"height\": 657, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1885, \"height\": 1029, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-02-736026-v1/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 812, \"height\": 917, \"label\": \"Table\"}]"
motivation: 探究EEG预处理策略对Transformer模型注意力机制与脑有效连接对齐的影响，以提升视觉解码的神经生理可解释性。
method: 使用ATM模型，对比MVNN基线预处理与集成ICA和陷波滤波的综合管道，进行交叉泛化、噪声鲁棒性和谱-时间消融分析，并通过节点强度相关性与RSA对齐注意力与GPDC/PDC/DTF网络。
result: 综合预处理有效抑制非神经伪迹，保持解码精度；注意力空间组织跨管道稳定，捕获与神经参考网络一致的定向连接动态，全局表征几何存在细微差异。
conclusion: 数据驱动注意力与神经生理一致性存在结构对应，预处理策略影响细微差异，为构建透明脑机接口提供了经验依据。
---

## 摘要
基于Transformer的深度学习模型在解码视觉脑电信号方面显示出巨大潜力。然而，其内部注意力机制通常主要基于优化目标进行评估，而与生物大脑连接的对齐程度仍是一个开放问题。本研究以自适应思维映射器（ATM）模型为框架，实证评估了脑电图预处理策略的变化如何影响这些注意力表示。我们比较了基线处理流程（仅MVNN）和整合了ICA与陷波滤波的综合清洁流程。通过跨泛化、噪声鲁棒性以及频谱-时间消融分析对模型进行了评估。此外，我们利用节点强度相关性和表征相似性分析（RSA）研究了模型数据驱动注意力权重与神经生理参考网络（GPDC、PDC和DTF）之间的结构对应关系。结果表明，综合预处理成功抑制了非神经伪影，如额叶噪声和电气干扰，同时保持了可比的解码准确性和基线鲁棒性。对齐分析显示，学习到的注意力模式的广泛空间组织在不同流程间保持高度稳定，捕捉了关键的定向连接动态，全局表征几何存在细微的、依赖于指标的差异。这项工作为弥合数据驱动注意力权重与神经生理一致性提供了实证探索，为更透明的脑机接口提供了见解。

## Abstract
Transformer-based deep learning models have shown great potential for decoding visual EEG signals. However, their internal attention mechanisms are often evaluated primarily on optimization objectives, leaving their alignment with biological brain connectivity an open question. This study empirically evaluates how variations in EEG preprocessing strategies affect these attention representations using the Adaptive Thinking Mapper (ATM) model as a framework. We compared a baseline pipeline (MVNN only) against a comprehensive cleaning pipeline integrating ICA and notch filtering. The models were evaluated through cross-generalization, noise robustness, and spectral-temporal ablation analyses. Furthermore, we investigated the structural correspondence between the model's data-driven attention weights and neurophysiological reference networks (GPDC, PDC, and DTF) using Node Strength Correlation and Representational Similarity Analysis (RSA). The results show that the comprehensive preprocessing successfully suppresses non-neural artifacts, such as frontal noise and electrical interference, while maintaining comparable decoding accuracy and baseline robustness. Alignment analyses revealed that the broad spatial organization of the learned attention patterns remains highly stable across pipelines, capturing key directed connectivity dynamics with subtle, metric-dependent variations in global representational geometry. This work provides an empirical exploration into bridging data-driven attention weights with neurophysiological consistency, offering insights toward more transparent brain-computer interfaces.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：基于Transformer的深度学习模型在视觉EEG解码中表现出优异性能，但其内部的通道注意力机制主要根据优化目标（如损失函数）学习，与生物大脑中真实的定向连接（有效连接）是否对齐尚不明确。此外，EEG预处理策略（如是否使用ICA和陷波滤波）会改变信号特征，进而可能影响模型学到的注意力表示及其神经生理可解释性。
- **整体含义**：本文试图搭建一座桥梁——将数据驱动的注意力权重与神经生理学上的有效连接度量进行比较，从而评估预处理对模型可解释性的影响。目标是促进更透明、更可信的脑机接口（BCI）的发展，为未来在神经解码中平衡算法性能与生物一致性提供经验基础。

### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：以自适应思维映射器（Adaptive Thinking Mapper, ATM）模型为框架，对比两种预处理管线，并分析模型学习到的通道注意力矩阵与三种神经生理有效连接度量（GPDC、PDC、DTF）之间的结构对应关系。
- **关键技术细节**：
    - **预处理管线**：
        - **基线**：仅使用多变量噪声归一化（MVNN）。
        - **提出的综合管线**：先进行50Hz陷波滤波 → ICA分解（63个成分）去除眨眼、肌肉等伪迹 → 分段（-0.2~1.0s，基线校正，降采样至250Hz）→ MVNN。
    - **模型架构**：ATM编码器，包含Subject Token（捕捉被试间变异）和63个Channel Token，经过多头自注意力层计算通道间关系。注意力公式：`Attention(Q,K,V) = softmax(QK^T / sqrt(dk)) V`。
    - **有效连接度量**：基于多元自回归模型（MVAR）计算，模型阶数p=5（通过BIC确定），采用512点FFT。
        - **PDC**（部分有向相干）：仅测量直接因果交互。
        - **GPDC**（广义PDC）：具有尺度不变性，克服幅度差异不足。
        - **DTF**（有向传递函数）：测量总因果影响（直接+间接）。
    - **对齐分析**：
        - **节点强度相关性**：计算每个通道的总节点强度（入强度+出强度），用Spearman秩相关比较注意力与有效连接矩阵的节点强度。
        - **表征相似性分析（RSA）**：分别构建注意力矩阵和有效连接矩阵的RDM，用Spearman秩相关测量全局结构相似性。
- **算法/流程说明**：
    1. 数据预处理（基线或综合）→ 2. 训练ATM模型 → 3. 提取最终epoch（epoch 40）的通道注意力矩阵（平均所有head和所有test trial）→ 4. 对同一批test数据计算被试/试次平均的GPDC/PDC/DTF矩阵 → 5. 进行节点强度相关性和RSA → 6. 统计检验（配对t检验，FDR校正）。

### 3. 实验设计：数据集、benchmark、对比方法

- **数据集**：THINGS-EEG2数据集，包含10名健康被试，采用快速序列视觉呈现（RSVP）范式。训练集16,540张图片，测试集200张图片。63通道EEG（参考Fz），采样率1000Hz，后降采样至250Hz。
- **Benchmark**：以基线预处理（仅MVNN）作为参考标准，综合预处理作为改进方案。主要评估指标包括：
    - 分类准确率（Top-1、Top-5、V10/V4/V2候选集设置）。
    - 交叉泛化性能（跨预处理测试）。
    - 频谱消融（δ/θ/α/β/γ/线噪声频带去除）。
    - 时间窗消融（0-200ms, 200-400ms, 400-600ms, 600-800ms, 800-1000ms）。
    - 噪声鲁棒性（注入高斯噪声标准差0.0~1.0）。
    - 对齐分析（节点强度相关性、RSA）。
- **对比方法**：该研究不与其他SOTA模型对比性能，而是聚焦于自身两种预处理下的内部表示变化，以及注意力与神经生理参考（GPDC/PDC/DTF）的对齐。

### 4. 资源与算力

- **文中未明确说明所用GPU型号、数量、训练时长等具体硬件资源**。仅提到模型使用AdamW优化器，学习率3e-4，batch size 64，训练40个epoch，随机种子固定24。但未提供训练耗时、功耗或硬件配置信息。

### 5. 实验数量与充分性

- **实验组数**：
    - 训练及主评估：10名被试 × 2种预处理（基线/综合） → 20个模型。
    - 交叉泛化：4种条件（基线训练+基线测试 / 基线训练+综合测试 / 综合训练+基线测试 / 综合训练+综合测试）。
    - 频谱消融：8种频带（None, LN, γ, β, α, θ, δ），针对两个模型，共16组。
    - 时间消融：6个时间窗（None, T1~T5），两个模型，共12组。
    - 噪声鲁棒性：5个噪声水平（σ=0.0, 0.1, 0.3, 0.5, 1.0），两个模型，共10组。
    - 节点强度相关性：3种有效连接方法 × 8个频带 × 2个预处理 → 48个Spearman相关系数（但只报告了总体的配对差异检验）。
    - RSA：类似结构，3方法×8频带×2预处理 → 48个RSA得分。
    - 此外还有可视化（PSD、拓扑图）。
- **充分性评估**：
    - **充分**：涵盖性能、泛化、消融（频域、时域）、鲁棒性、生物对齐等多个维度，实验设计较为全面。
    - **客观公平**：所有模型采用相同随机种子、相同epoch数（epoch 40，而非最佳epoch），避免选择偏差；所有统计检验使用配对t检验并做FDR校正，控制多重比较；effect size（Cohen's d）给出，便于量化差异大小。
    - **不足**：仅有10名被试；数据集是RSVP范式特定；未与不同架构（如CNN、EEGNet）或不同注意力机制对比；对齐分析中未考虑个体差异或动态时间窗口；预处理仅比较两种特定策略，未探索更广泛的组合。

### 6. 论文的主要结论与发现

1. **预处理效果**：综合预处理成功抑制了额叶眼电伪迹和50Hz线噪声，且未显著降低解码准确率（基线Top-1: 26.30% vs 综合: 24.70%，差异不显著），模型鲁棒性保持可比。
2. **频谱依赖性**：解码性能主要依赖低频（δ和θ频带），去除θ频带后Top-1准确率暴跌至约8%（Cohen's d > 2.5）；去除线噪声和γ频带影响不显著。
3. **时间依赖性**：0~400ms后刺激窗口（覆盖单试次100ms图像+100ms空白+T1和T2）对解码至关重要，去除后准确率降至5~6%，且效果量极大（d达-7.15）。
4. **生物对齐**：
    - 节点强度相关性表明，注意力的空间枢纽结构在不同预处理下保持稳定，与GPDC的对应最强（尤其θ和α波段），但与DTF和PDC的对应较弱且不显著。
    - RSA显示综合预处理后的全局表征几何与有效连接有轻微正向偏移（不显著，但部分中等效应量），表明综合预处理可能使注意力更接近神经生理全局结构，而基线预处理在局部拓扑上略有优势但无统计差异。
    - 注意力与GPDC在θ和α波段的空间拓扑高度相似（图6），表明模型捕捉了与视觉处理相关的定向连接动态。
5. **整体结论**：预处理改变会影响注意力的结构细微差异，但广泛的空间组织及与神经参考的对齐保持稳定。数据驱动的注意力权重确实与神经生理连接存在结构对应，但依赖于所用连接度量。

### 7. 优点

- **方法新颖**：首次系统地桥接Transformer注意力与神经生理有效连接，并引入RSA和节点强度两种互补对齐指标。
- **实验严谨**：采用配对t检验+FDR校正，避免了多重比较膨胀；使用最终epoch模型而非最佳epoch，避免选择偏差；报告effect size增强可解释性。
- **多维度评估**：不仅评估分类性能，还从谱、时、噪声鲁棒性、跨泛化、生物对齐等方面全面分析预处理影响。
- **可视化清晰**：PSD对比、拓扑节点强度图直观展示了预处理效果和对齐模式。
- **开源与可复现**：论文提到固定随机种子，且预处理流程详细，便于复现。

### 8. 不足与局限

- **样本量有限**：仅10名被试，统计检验力可能受限，尤其对齐分析中许多差异虽有效应量但未达显著，需更大样本验证。
- **数据集单一**：仅使用THINGS-EEG2（RSVP范式），结论不一定能推广到其他范式（如运动想象、稳态诱发电位）或不同任务难度。
- **预处理只比较两种策略**：未探索多种ICA拒绝标准、不同滤波器组合、重参考选择对注意力表示的影响，结论具有局限性。
- **缺乏与其它模型架构对比**：未比较CNN、EEGNet或图神经网络的注意力表示生物相关性，无法说明ATM的独特性。
- **对齐分析假设全局平均**：注意力矩阵和连接矩阵均跨试次、跨被试平均，可能掩盖个体差异和动态变化；且未考虑注意力头之间的特异性。
- **有效连接计算局限**：使用MVAR假设线性关系和短时期平稳性，可能与真实脑非平稳非线性动态有偏差；且仅用BIC选定阶数p=5，未考虑更复杂选择。
- **无真实神经生理验证**：仅以有效连接度量作为参考，这些度量本身是模型估计，不一定代表真实因果；缺乏通过靶向神经调控（如TMS）验证。
- **未评估重建质量**：本文仅关注注意力表示，未评估最终图像重建或CLIP对齐质量变化，可能遗漏预处理对下游任务的影响。
- **算力信息缺失**：无法评估资源开销或可扩展性。

（完）
