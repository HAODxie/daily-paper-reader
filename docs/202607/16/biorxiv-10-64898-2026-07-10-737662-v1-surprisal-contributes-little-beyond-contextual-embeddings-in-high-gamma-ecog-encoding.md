---
title: Surprisal contributes little beyond contextual embeddings in high-gamma ECoG encoding
title_zh: 在高伽马ECoG编码中，惊讶度在上下文嵌入之外贡献甚微
authors: "Sakuma, T."
date: 2026-07-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.10.737662v1.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 使用GPT-2 XL的上下文嵌入和惊异度预测高γECoG反应
tldr: 语言理解神经编码中，上下文嵌入和surprisal均源自大语言模型。本文利用高伽马ECoG公开数据，直接检验在GPT-2 XL嵌入基础上加入surprisal能否提升预测。结果发现，添加单个surprisal预测器后，留出验证的相关性几乎不变，且效应在预设等价范围内。这表明surprisal没有独立贡献，应视为嵌入已捕获预测状态的压缩读出。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1588, \"height\": 610, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1690, \"height\": 390, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1575, \"height\": 616, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1588, \"height\": 611, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1587, \"height\": 542, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1698, \"height\": 683, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1695, \"height\": 1271, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1717, \"height\": 539, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1713, \"height\": 264, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 889, \"height\": 239, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1394, \"height\": 238, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1511, \"height\": 238, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1389, \"height\": 236, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1273, \"height\": 194, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-10-737662-v1/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1382, \"height\": 197, \"label\": \"Table\"}]"
motivation: 明确surprisal在已有上下文嵌入之外是否提供额外神经预测信息。
method: 使用自然语音ECoG记录，构建基于GPT-2 XL嵌入和surprisal的岭回归编码模型进行预测比较。
result: 加入surprisal后留出相关性无提升，效应在等价边界内，增量近乎零。
conclusion: Surprisal不是独立预测因子，而是嵌入状态的部分重复。
---

## 摘要
惊讶度（Surprisal）和上下文嵌入都源自大型语言模型，并被广泛用于预测语言理解过程中的神经反应，但尚不清楚惊讶度是否提供了嵌入之外的信息。我们直接对此进行了测试：在包含GPT-2 XL上下文嵌入后，单词惊讶度是否能改善高伽马ECoG响应的样本外预测？利用自然语音的公开ECoG记录，我们使用基线刺激特征、GPT-2 XL嵌入和GPT-2 XL惊讶度拟合了词对齐的岭编码模型。添加一个惊讶度预测因子后，中心延迟下的留出相关性基本保持不变，并且在其他延迟和敏感性分析中，效果仍保持在预先指定的等效范围内。这种近乎为零的增量表明，惊讶度并非一个独立的预测因子。它更好地被理解为嵌入已经捕捉到的相同更广泛预测状态的一种压缩读出。

## Abstract
Surprisal and contextual embeddings are both derived from large language models and are widely used to predict neural responses during language comprehension, but it is unclear whether surprisal adds information beyond embeddings. We test this directly: does word surprisal improve out-of-sample prediction of high-gamma ECoG responses after GPT-2 XL contextual embeddings are included? Using public ECoG recordings from natural speech, we fit word-aligned ridge encoding models with baseline stimulus features, GPT-2 XL embeddings, and GPT-2 XL surprisal. Adding one surprisal predictor left held-out correlation essentially unchanged at the center lag, and the effect remained within a prespecified equivalence margin across alternative lags and sensitivity analyses. This near-zero increment suggests that surprisal does not act as an independent predictor. It is better understood as a compressed readout of the same broader predictive state that the embeddings already capture.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：惊讶度（Surprisal）和上下文嵌入都源自大型语言模型（如GPT-2），并被广泛用于预测语言理解过程中的神经反应。然而，先前研究通常只单独测试surprisal或单独使用嵌入，未检验**在已有上下文嵌入的情况下，surprisal是否能提供额外的预测信息**。本文直接回答这一增量预测问题。
- **整体含义**：通过对公开ECoG数据集的分析，发现添加surprisal后留出预测性能几乎没有变化（Δr ≈ -6.6×10⁻⁵），且效应在预设的等价边界内。这表明surprisal不是独立的预测因子，而是上下文嵌入所表征的预测状态的压缩读出。该结果对语言理解的神经机制解释（如预测编码理论）提出了谨慎的映射限制。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：使用线性岭回归编码模型，以**单词**为基本单元，对齐ECoG高伽马（high-gamma, 70–200 Hz）响应。通过逐步加入不同特征组，比较留出预测性能的增量。
- **关键技术细节**：
  - 模型公式：\( y_t = \alpha + \mathbf{x}_t^\top \boldsymbol{\beta} + \varepsilon_t \)，其中 \( y_t \) 为词 \( t \) 对应的神经响应（固定电极和延迟），\( \mathbf{x}_t \) 包含不同特征组合。
  - 特征组：
    - 基线特征（\( \mathbf{b}_t \)）：梅尔频谱功率、语音特征、句法特征、静态词嵌入（非上下文）。
    - GPT-2 XL上下文嵌入（\( \mathbf{e}_t \)）：1600维，经PCA降至100维。
    - Surprisal（\( S_t \)）：标量，基于GPT-2 XL token概率求和得到（自然对数）。
  - 主要对比模型：
    - \( M_{\text{base}} \)：仅基线特征。
    - \( M_{\text{emb}} \)：基线 + 上下文嵌入。
    - \( M_{\text{emb+surp}} \)：基线 + 上下文嵌入 + surprisal。
  - 评估指标：留出皮尔逊相关系数 \( r \)，对比 \( \Delta r = r(M_{\text{emb+surp}}) - r(M_{\text{emb}}) \)。
  - 等价检验：使用双单侧检验（TOST），预设最小效应量 ±0.001 相关系数单位。
  - 交叉验证：5折块留出，训练与测试段间隔25个词。特征标准化和PCA仅在训练折进行。
  - 正则化：共享脊回归，惩罚参数网格 {1, 10, 10², ..., 10⁶}；另外也进行了**带脊回归**（特征块独立正则化）作为敏感性分析。

## 3. 实验设计：数据集、基准、对比方法

- **数据集**：
  - 主分析：OpenNeuro ds005574 “Podcast” ECoG数据集，8名参与者听取30分钟自然语音故事。预处理文件 `all_data.pkl`（来自Zenodo记录15220273），包含词对齐的高伽马响应（161个延迟窗口，中心延迟索引80）、基线特征、GPT-2 XL嵌入和surprisal。
  - 辅助分析：使用公开教程代码（MNE-Python/BIDS），仅可用于3名参与者，作为实现验证和频率带变体分析。
- **基准（Baseline）**：\( M_{\text{base}} \)（仅非上下文基线特征）。
- **对比方法**：
  - \( M_{\text{emb}} \)：基线 + 嵌入。
  - \( M_{\text{emb+surp}} \)：基线 + 嵌入 + surprisal。
  - 额外探索性特征：嵌入旋转（1 - cos(\( \mathbf{e}_t, \mathbf{e}_{t-1} \))）、嵌入步长（\( \|\mathbf{e}_t - \mathbf{e}_{t-1}\|_2 \)）、熵降（\( H_{t-1} - H_t \) 截断为正）。
- **敏感性分析**：
  - 不同延迟选择：中心延迟、嵌入峰值延迟、频谱峰值延迟、surprisal-only峰值延迟。
  - 特征块重叠分析（独特R²）。
  - 替代神经网络目标：θ（4–8 Hz）和β（13–30 Hz）包络。
  - 不同正则化：共享脊 vs 带脊。
  - 注入分析：向神经响应矩阵人工注入surprisal形状的信号（η = 0.05, 0.10），检验方法能否恢复。

## 4. 资源与算力

- **文中未明确说明**：未提及使用的GPU型号、数量或训练时长。论文使用了预训练的GPT-2 XL模型提取特征，且在标准CPU/GPU上完成岭回归拟合，计算需求较低。因此没有单独讨论算力资源。

## 5. 实验数量与充分性

- **实验数量**：
  - 主对比：8名参与者，每个参与者多个电极，报告均值和参与级Δr。
  - 敏感性分析：表2（4种延迟规则）、表3（特征块重叠）、表5（替代实现3名参与者）、表6（3种频率带）、表7（共享脊 vs 带脊）、表8（注入分析及不同η值）。
  - 探索性更新度量：表4（旋转、步长、熵降）。
  - 图1–7展示了不同层次的比较。
- **充分性**：实验覆盖了多种可能的混淆（延迟选择、正则化、神经信号频带、实现细节），并通过注入正控制验证了分析能够检测到微弱的信号。总体较为充分和客观。
- **公平性**：使用预设等价边界，避免零假设的过度接受；采用留出交叉验证和独立预处理步骤；对比条件明确。但参与者数量偏少（仅8人），辅助分析仅3人，统计效力有限。

## 6. 论文的主要结论与发现

1. **上下文嵌入**显著提升高伽马预测：\( M_{\text{emb}} \) 平均 \( r = 0.169 \)，远高于 \( M_{\text{base}} \) 的 0.003。
2. **添加surprisal几乎没有改善**：中心延迟下 \( \Delta r = -6.6\times10^{-5} \)，90% CI完全落在预设等价边界 ±0.001 内，TOST支持等价于零（p = 2.4×10⁻⁹）。
3. **结论稳健**：不同延迟、正则化、频率带、实现代码下，Δr均保持近零。
4. **探索性更新度量**（嵌入旋转、步长）产生小但一致的增量（Δr ≈ +2.3×10⁻⁴、+2.1×10⁻⁴），而surprisal和熵降几乎无增量。这表明神经活动可能更多与状态更新相关，而非概率读出。
5. **注入分析**表明，当人工信号强度约为响应标准差的5%时，所恢复的增量接近等价边界，说明方法灵敏度足够。

## 7. 优点：方法或实验设计上的亮点

- **增量检验设计**：直接比较在已有嵌入基础上加入surprisal的效果，避免边际相关性的误导。
- **等价检验**：使用预设最小效应量和TOST，明确声明是否“可忽略”，而非仅报告不显著。
- **广泛的敏感性分析**：涵盖延迟、正则化、频带、实现、注入正控制等多维度，增强结论可信度。
- **开源数据和代码**：使用公开ECoG数据集和发布的分析文件，促进复现。
- **探索性特征**：提供了嵌入旋转/步长等候选特征，为后续研究指明方向。

## 8. 不足与局限

- **线性模型**：未能捕捉非线性关系，且限于词对齐，无法细粒度到子词或连续时间分辨率。
- **信号局限**：仅考虑幅度包络（高伽马、θ、β），未涉及相位、跨频耦合或层流分离。
- **参与者样本小**：主分析仅8名参与者，辅助分析仅3名；统计推断泛化性有限。
- **单一语言模型**：仅使用GPT-2 XL，未测试BERT、LLaMA等其他架构。
- **潜在遗漏的预测误差信号**：方法可能错过分布式、多维度的预测误差成分，这些成分可能体现在更细的时标或不同神经信号中。
- **应用限制**：结论仅适用于自然语音中的词对齐高伽马ECoG，不能直接推广至阅读或其他认知任务。

（完）
