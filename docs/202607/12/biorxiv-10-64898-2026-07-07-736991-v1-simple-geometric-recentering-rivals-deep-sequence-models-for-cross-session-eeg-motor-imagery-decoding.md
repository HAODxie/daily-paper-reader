---
title: Simple Geometric Recentering Rivals Deep Sequence Models for Cross-Session EEG Motor-Imagery Decoding
title_zh: 简单几何重居中在跨会话脑电运动想象解码中匹敌深度序列模型
authors: "Rahimipour, M., Van Hulle, M."
date: 2026-07-11
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.07.736991v1.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 脑电运动想象解码用于脑机接口
tldr: "脑机接口中运动想象解码常采用复杂深度网络，但未经与简单几何基线的公平对比。本文固定协方差特征，比较切空间几何方法（含测试时最近化）与BiMamba等深度模型在8个公开数据集上的表现。跨会话场景下，几何方法显著优于所有深度模型（效应量d>1.06），且优势源于最近化机制而非模型容量。结论表明简单几何基线足够强大，挑战了深度学习在该任务中的必要性。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1664, \"height\": 674, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1659, \"height\": 719, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1637, \"height\": 637, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1180, \"height\": 763, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1179, \"height\": 646, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1260, \"height\": 649, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1658, \"height\": 619, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 947, \"height\": 527, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1156, \"height\": 375, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1094, \"height\": 526, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 961, \"height\": 223, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1486, \"height\": 595, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1391, \"height\": 527, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1365, \"height\": 527, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1368, \"height\": 265, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1482, \"height\": 635, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-07-736991-v1/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1293, \"height\": 530, \"label\": \"Table\"}]"
motivation: 验证脑电解码中深度学习架构的复杂性是否相对于简单几何方法具有实质性优势。
method: 固定单频带协方差特征，对比切空间几何方法（含测试时最近化）与BiMamba深度序列模型及SPDNet。
result: 跨会话中几何方法平均排名第一，对深度模型优势显著（p<1.1e-12）；深度模型表现弱于所有经典黎曼方法。
conclusion: 简单几何基线足以在跨会话解码中取得最优，深度模型需更审慎地评估其必要性。
---

## 摘要
大量且不断增长的工作将日益复杂的深度架构应用于脑电图运动想象（MI）解码，但很少在相同条件下测试这种复杂性是否优于一个强大、简单的几何基线。我们在八个公开MI数据集（3-128通道，2-3类，单会话和多会话）上进行了受控基准测试，固定特征表示，仅改变解码器。核心方法——在SPD流形上使用无监督测试时重居中的紧凑切空间流水线，此处称为几何感知——与三个经典黎曼基线（TS+SVM、FgMDM、MDM）以及基于我们自己先前架构（双向Mamba混合专家模型BiMamba+MoE，及其两个简化消融变体，以及一个SPDNet风格网络）的一系列深度模型进行比较，所有这些模型都使用相同的单波段协方差特征。在跨会话的88个受试者水平观察和会话内的120个观察中，几何感知在跨会话中取得最佳平均排名，在会话内统计上与最佳方法持平（按原始排名第二，但在关键差异检验下与TS+SVM无法区分）。其跨会话优势巨大且统计上具有决定性——在多重比较校正后，它以大的效应量（Cohen's d=1.06-1.50；所有p_FDR<1.1x10^-12）击败了所有竞争者——但在会话内，它与无重居中的对应方法（TS+SVM）的差异在统计上无法区分（d=-0.00，p=0.54）。这种跨/会话内双重分离表明重居中是操作机制，而非通用容量。深度序列模型（Mamba变体）尽管特征匹配且使用公平、固定的训练预算，但在两种协议中都远远逊于所有经典黎曼方法；SPDNet基线表现较好——击败了MDM——但仍从未在相同特征上击败简单的切空间流水线。我们认为这是一个积极、良好控制的结果，直接回答了架构复杂性是否合理的审稿式问题。我们说明了局限性——深度模型比较的公平性、缺乏直接机制探测以及数据集范围——并概述了每一点如何成为具体的下一步步骤。

## Abstract
A large and growing body of work applies increasingly complex deep architectures to EEG motor-imagery (MI) decoding, yet rarely tests whether that complexity is justified against a strong, simple geometric baseline under identical conditions. We report a controlled benchmark across eight public MI datasets (3-128 channels, 2-3 classes, single- and multi-session) that holds the feature representation fixed and varies only the decoder. The central method - a compact tangent-space pipeline on the SPD manifold with unsupervised test-time recentering, here called Geometry-Aware - is compared against three classical Riemannian baselines (TS+SVM, FgMDM, MDM) and a family of deep models built from our own prior architecture (a bidirectional Mamba mixture-of-experts, BiMamba+MoE, with two reduced ablation variants, and an SPDNet-style network), all consuming the same single-band covariance features. Across N=88 subject-level observations cross-session and N=120 within-session, Geometry-Aware achieves the best average rank cross-session and is statistically tied for the best within-session (second by raw rank but indistinguishable from TS+SVM under the critical-difference test). Its cross-session advantage is large and statistically decisive - it beats every competitor after multiple-comparison correction with large effect sizes (Cohen's d=1.06-1.50; all p_FDR<1.1x10^-12) - yet within session its advantage over its recentering-free twin (TS+SVM) is statistically indistinguishable (d=-0.00, p=0.54). This cross/within double dissociation points to recentering as the operative mechanism rather than generic capacity. The deep sequence models (the Mamba variants), despite matched features and a fair, fixed training budget, underperform every classical Riemannian method in both protocols by wide margins; the SPDNet baseline fares better - beating MDM - but still never beats the simple tangent-space pipeline on identical features. We argue this is a positive, well-controlled result that directly answers the reviewer-style question of whether architectural complexity is warranted. We state the limitations - fairness of the deep-model comparison, the absence of a direct mechanistic probe, and dataset scope - and outline how each becomes a concrete next step.

---

## 论文详细总结（自动生成）

# 论文总结：简单几何重居中在跨会话脑电运动想象解码中匹敌深度序列模型

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：跨会话脑电解码是运动想象脑机接口的实际瓶颈：一个会话训练的模型在下一个会话上性能显著下降，因为EEG的协方差结构在会话间发生漂移（电极更换、阻抗变化、基线唤醒度、疲劳等）。主流研究倾向于不断增加模型容量（更深网络、注意力机制、状态空间序列模型），但鲜有检验这种复杂性是否真的必要。
- **核心问题**：在添加架构复杂性之前，一个简单的、几何感知的基线在允许其在无标签测试会话上自我重居中时，能走多远？即：简单几何方法能否匹敌甚至超越深度序列模型？
- **整体含义**：通过固定特征表示、仅改变解码器，发现一个极其简单的线性管道（切空间投影+无监督测试时重居中）在跨会话场景中以大效应量显著优于所有深度模型，且优势源于重居中的机制而非模型容量。这一结果直接回应了“复杂性必须经过证明”的审稿要求，挑战了当前深度学习在该任务中的主导地位。

## 2. 方法论：核心思想、关键技术细节

### 核心思想
- 固定特征表示：所有方法使用相同的输入——由Oracle-Approximating-Shrinkage（OAS）估计的单个8-32 Hz频带的协方差矩阵，重采样至250 Hz。仅解码器不同，从而消除特征工程带来的混淆。
- 中心方法：**Geometry-Aware**——在SPD流形上执行切空间投影，加上无监督测试时重居中，然后使用L2正则化逻辑回归分类。

### 关键技术细节
- **协方差估计**：OAS正则化协方差估计（Oracle-Approximating-Shrinkage），确保协方差矩阵正定且良态。
- **切空间映射**：使用仿射不变 Riemann 度量，将每个协方差矩阵投影到由参考点定义的切空间。参考点（几何均值）在训练时确定。
- **测试时重居中**（tsupdate=True）：在跨会话协议中，将参考点重新估计为测试会话（无标签）所有试次的协方差矩阵的几何均值。这相当于将测试数据重居中到训练时分类器所在的流形点，校正会话间几何漂移。不依赖测试标签，是无监督转导校正。
- **分类器**：L2正则化逻辑回归（来自pyRiemann库）。

### 对比方法的关键差异
- 与TS+SVM对比：TS+SVM使用相同切空间投影但无重居中（tsupdate=False），且分类器为线性SVM。通过会话内实验（均无重居中）证明分类器选择无差异，因此跨会话性能差距完全归因于重居中。
- 深度模型：使用相同协方差特征，但以不同方式处理（BiMamba+MoE将协方差矩阵作为序列输入，SPDNet在相同切向量上接深度MLP）。

## 3. 实验设计

### 数据集
- 8个公开MOABB数据集：BNCI2014_001（22通道，3类，2会话）、BNCI2014_004（3通道，2类，5会话）、BNCI2015_001（13通道，2类，2会话）、Zhou2016（14通道，3类，3会话）、Lee2019_MI（62通道，2类，2会话）、Schirrmeister2017（128通道，3类，1会话）、AlexMI（16通道，3类，1会话）、Weibo2014（60通道，3类，1会话）。
- 跨会话分析仅包含前5个多会话数据集（≥2会话），共88个受试者水平观测；会话内分析包含全部8个数据集（120个受试者水平观测）。

### 基准（Baselines）
- **经典黎曼方法**：TS+SVM（无重居中切空间+线性SVM）、FgMDM（Fisher-测地最小距离到均值）、MDM（最小距离到均值）。
- **深度序列模型**（来自作者先前工作BiMoE-RCoMET但缩水）：
  - BiMamba+MoE：双向Mamba选择状态空间块+混合专家门控，多尺度聚合头。
  - BiMamba no-MoE：单Mamba路径（消融）。
  - Mamba uni：单向，无MoE（消融）。
- **SPDNet**：紧凑型SPDNet风格深度MLP（相同切向量作为输入，隐藏层256→128→类别数）。

### 评价协议
- **会话内**：每个会话内进行分层5折交叉验证。
- **跨会话**：标准MOABB留一会话评估（在每个会话上，用剩余所有会话训练，在留出会话上测试，平均所有分割）。
- **指标**：平衡准确率（统一用于2类和3类问题）。对于多于3类的数据集，只取前3类以保证内部一致性。

### 统计分析方法
- Friedman全方差检验（验证方法间存在差异）。
- 所有两两比较：Wilcoxon符号秩检验 + Benjamini-Hochberg FDR校正 + Holm校正（28个比较）。
- 配对Cohen's d效应量。
- 2000次重采样bootstrap置信区间。
- Nemenyi临界差异图（平均排名分析）。
- 鲁棒性检查：移除最大数据集Lee2019_MI后重复；数据集水平检验（仅5个跨会话数据集，每个一个平均值）。

## 4. 资源与算力

- 论文未明确提及使用的GPU型号、数量或训练时长。仅提及“in the Methods: All deep models share one training procedure ... Training runs for a fixed 20 epochs with batch size 128”。且“The full run was executed unattended on the KU Leuven VSC cluster with incremental saving and automatic resume”。未量化具体硬件资源。
- **注意**：这一点是本文的不足之处之一，对于可重复性和公平性评估不完整。

## 5. 实验数量与充分性

- **实验数量**：8个数据集，两种协议（跨会话/会话内），共88+120=208个受试者水平观测。每个受试者每个方法得到一个得分，共8种方法，产生大量配对数据。
- **消融实验**：
  - 对深度序列模型本身有消融（BiMamba+MoE vs. no-MoE vs. uni）。
  - 关键消融：Geometry-Aware vs. TS+SVM（有无重居中），并控制分类器差异（通过会话内实验证明分类器不影响）。
- **充分性与公平性评估**：
  - 所有方法使用完全相同特征（OAS协方差），特征固定，仅解码器不同，消除特征工程混淆。
  - 深度模型使用固定训练预算（Adam，cosine学习率衰减，20 epoch，batch size 128，梯度裁剪，固定随机种子42），无数据集特定调整。作者承认这可能不是最优设置，但这是有意为之：测试“开箱即用”的额外复杂性是否合理，而非寻找最强深度模型。
  - 统计分析全面严格（非参数检验、多重比较校正、效应量、bootstrap置信区间、临界差异图），并进行了鲁棒性检查（移除主导数据集、数据集水平检验）。
  - **潜在不足**：深度模型可能未被充分优化（并非架构搜索），但作者明确将其列为局限，并解释为设计选择。另外，数据集范围偏向中小通道数；多会话数据集仅5个，但每个受试者一个观测值使得样本量足够（N=88）。总体而言，实验设计在受控性和统计严谨性上非常充分。

## 6. 主要结论与发现

- **中心结论**：在不同会话间，一个具有无监督测试时重居中的最小切空间几何管道（Geometry-Aware）在平均排名上表现最佳，并显著优于所有经典黎曼基线和深度序列模型，具有大的效应量（d=1.06-1.50，所有p_FDR<1.1x10^-12）。在会话内，Geometry-Aware与无重居中的对应方法TS+SVM统计上无法区分（d=-0.00，p=0.54）。
- **机制揭示**：这种跨/会话内双重分离强烈表明重居中是操作机制，而非模型容量。因为如果只靠通用解码能力，则应在两种协议下都领先；但Geometry-Aware仅在存在会话间漂移时才有优势，正好符合漂移校正机制的特征。
- **深度模型表现**：所有深度序列模型（Mamba变体）在所有协议下表现均差于所有经典黎曼方法；SPDNet表现较好（击败MDM），但从未在相同特征上击败简单切空间管道。表明在单波段协方差解码上，高容量序列模型缺乏可利用的结构且易过拟合，而黎曼几何的归纳偏置恰好适合该问题。
- **挑战主流**：结论表明，在该问题规模和表示下，架构复杂性是不合理的；最简单的几何校正（重居中）才是关键。

## 7. 优点

- **干净的控制实验设计**：固定特征表示，仅改变解码器，消除了深度模型常有的特征工程优势。
- **机制可检验性**：通过会话内/跨会话协议下同一管道（有/无重居中）的差异，直接证明了重居中的因果作用，而非仅报告平均准确率。
- **统计严谨性**：使用了完整的非参数统计套件（Friedman、Wilcoxon+FDR+Holm、Cohen's d、bootstrap CI、临界差异图），并进行了鲁棒性检查，结论可靠。
- **公平对比深度模型**：使用相同输入、相同训练预算、相同种子，且作者主动报告自己架构的失败，体现了科学诚实性。
- **明确揭示局限性**：作者主动指出了公平性、机制探测、特征表示、数据集范围等局限，并提出了具体下一步。
- **实践意义**：为跨会话脑机接口提供了极其简单高效的基线方案，对实际部署有直接价值。

## 8. 不足与局限

- **深度模型比较的公平性**：深度模型仅使用了固定、合理的训练预算（20 epoch，余弦退火），未进行架构或超参数搜索。虽然作者有意测试“开箱即用”的复杂性，但可能低估了深度模型在更充分优化下的潜力。另外，深度模型没有报告每模型的训练准确率，无法完全排除优化失败。
- **缺乏直接机制探测**：重居中作为操作机制是通过行为分离推断的，但未直接测量几何漂移的校正程度（如重居中前后会话均值间的黎曼距离变化及其与增益的相关性）。
- **特征表示保守**：仅使用单一时频带（8-32 Hz）和单个协方差矩阵。更丰富的特征（多频带、CSD等）可能改变数值结果，并可能为深度模型提供更多可学习结构。
- **数据集范围有限**：8个数据集虽涵盖不同通道数，但仅5个支持跨会话，且偏向中小通道数。未包含高密度（例如256通道）或更多会话的数据集。三类问题仅使用前三类，简化了多类问题。
- **无直接复现性细节**：未提供GPU型号和算力使用细节，不利于他人完全复现深度模型训练部分。
- **可能的应用限制**：结果基于运动想象和协方差特征，不一定适用于其他EEG范式（如P300、SSVEP）或不同特征表示（如时域波形）。

---

（完）
