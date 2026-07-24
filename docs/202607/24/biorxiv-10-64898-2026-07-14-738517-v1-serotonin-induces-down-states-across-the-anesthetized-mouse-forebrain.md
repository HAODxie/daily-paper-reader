---
title: Serotonin induces DOWN states across the anesthetized mouse forebrain
title_zh: 血清素在麻醉小鼠前脑中诱导DOWN状态
authors: "Grossmann, R., Meijas, J. F., International Brain Laboratory,, Mainen, Z. F., Meijer, G. T."
date: 2026-07-20
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.14.738517v1.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 血清素在类似睡眠条件下诱发DOWN状态
tldr: 血清素对前脑全局网络状态的影响存在争议，传统电刺激诱导UP状态而光遗传fMRI提示抑制。本研究结合光遗传5-HT刺激与大规模Neuropixel记录，发现选择性5-HT释放一致诱导皮层和纹状体的DOWN状态，而中脑动力学几乎不受影响。多区域计算模型表明，这种转变源于网络同步而非直接来自中缝背核的输入，解决了长期争议。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738517-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1344, \"height\": 1378, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738517-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1756, \"height\": 1765, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738517-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1788, \"height\": 1358, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738517-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1733, \"height\": 1003, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738517-v1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1724, \"height\": 583, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738517-v1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1766, \"height\": 439, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738517-v1/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1759, \"height\": 631, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738517-v1/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1779, \"height\": 548, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-14-738517-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1361, \"height\": 460, \"label\": \"Table\"}]"
motivation: 澄清血清素通过中缝背核投射对前脑全局网络状态（UP/DOWN状态）调控的争议。
method: 结合光遗传5-HT刺激与跨前脑Neuropixel记录，并构建受生物学连接约束的多区域计算模型。
result: 5-HT释放一致诱导皮层和纹状体DOWN状态，中脑动力学几乎不变。
conclusion: 转变源于网络同步而非直接DRN输入。
---

## 摘要
背侧中缝核(DRN)的血清素能神经元广泛投射到前脑，但它们对全局网络状态的影响仍存在争议。血清素被认为参与调节慢波振荡，即所谓的UP和DOWN状态，这些状态在睡眠和轻度麻醉期间出现。虽然光遗传fMRI提示血清素(5-HT)抑制全脑活动，但经典电刺激研究却报告其可诱导皮层UP状态。为解决这一矛盾，我们将光遗传5-HT刺激与轻麻醉小鼠前脑的大规模Neuropixel记录相结合。我们证明选择性5-HT释放一致地在皮层和纹状体中诱导DOWN状态，而对中脑动力学影响甚微。一个受生物可信连接性约束的多区域计算模型表明，在某些区域，状态转变源于网络层面的同步化，而非直接的DRN输入。

## Abstract
Serotonergic neurons in the dorsal raphe nucleus (DRN) project extensively throughout the forebrain, yet their influence on global network states remains controversial. Serotonin is implicated in regulating slow-oscillations, so-called UP and DOWN states, which occur during sleep and light anesthesia. While optogenetic fMRI suggests that serotonin (5-HT) suppresses brain-wide activity, classical electrical stimulation studies report the induction of cortical UP states. To resolve this discrepancy, we combined optogenetic 5-HT stimulation with large-scale Neuropixel recordings across the forebrain of lightly anesthetized mice. We demonstrate that selective 5-HT release consistently induces DOWN states across the cortex and striatum, while leaving midbrain dynamics largely unaffected. A multi-area computational model constrained by biologically plausible connectivity, indicates that in certain regions the transitions arises from network-level synchronization rather than direct DRN input.

---

## 论文详细总结（自动生成）

# 中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **研究动机**：血清素（5-HT）作为重要的中枢神经调质，其通过背侧中缝核（DRN）广泛投射至前脑，但对全局网络状态（特别是慢波振荡中的 UP/DOWN 状态）的调控方向存在长期争议。电刺激 DRN 研究报告诱导 **UP 状态**，而光遗传 fMRI 研究则提示 **抑制性效应**，导致结论碎片化。
- **整体含义**：本研究旨在弥合分歧，通过同时具备**全脑覆盖**和**高时间分辨率**的方法，阐明血清素在麻醉下对 UP/DOWN 动态的真实作用。结果证明选择性 5-HT 释放**强有力地诱导 DOWN 状态**，并揭示该效应源于**网络同步化**而非单一的 DRN 直接输入，为理解血清素在睡眠和麻醉中的作用提供了统一框架。

## 2. 论文提出的方法论：核心思想、关键技术细节
- **核心思想**：结合**光遗传学选择性激活 DRN 血清素神经元**与**大规模 Neuropixel 探针记录**，实现全前脑（皮层、纹状体、海马、丘脑、杏仁核、中脑等）的单细胞级电生理同步记录，克服 fMRI 时间分辨率不足和传统电生理空间覆盖窄的缺陷。
- **关键技术细节**：
  - **动物模型**：SERT-Cre 小鼠注射 ChR2 病毒，五只表达成功，两只作为对照（无 ChR2 表达）。
  - **记录与刺激**：急性 Neuropixel 记录（4天，7个插入位置，覆盖8个脑区）；光刺激为 1 s 脉冲（1/5/10/25 Hz，10 ms 脉宽，5 mW），重复50次，ISI 服从截断指数分布（5-15 s）。
  - **数据分析**：
    - 使用 **ZETA 检验**统计神经元调制显著性。
    - 用 **ROC 曲线下面积（auROC）** 计算调制指数（MI），量化抑制/兴奋方向。
    - 使用 **两状态隐马尔可夫模型（HMM）** 对200 ms 窗口的发放率序列推断 UP/DOWN 状态后验概率。
  - **计算模型**：
    - 构建 **双稳态发放率模型**：每个脑区为包含兴奋（E）、抑制（I）群体和适应机制（A）的局部电路，基于 Jercog et al. 模型。
    - **生物可信连接**：从 Allen 小鼠连接组数据集抽取区域间投射密度，并作为网络耦合强度（参数 G）的权重。
    - **5-HT 刺激模拟**：向各区域 E 群体施加抑制性电流（E-），强度与 DRN 投射密度成正比；时间过程匹配实验的 0.5 s 峰值、3 s 衰减。
    - 比较了四种机制：E-（抑制 E），I+（兴奋 I），E+（兴奋 E），I-（抑制 I）。

## 3. 实验设计
- **数据集/场景**：
  - **动物**：7 只 SERT-Cre 小鼠（5 只表达 ChR2，2 只作为无光遗传效应的对照）。
  - **记录脑区**：前额皮层、视觉皮层、梨状皮层、杏仁核、纹状体、海马、丘脑、中脑。
  - **刺激条件**：四种频率（1/5/10/25 Hz），以及无刺激基线；分析时还按刺激发生在 UP 或 DOWN 状态进行子选择。
- **基准（benchmark）**：未明确设定外部基准，主要进行**内部对比**：不同脑区之间、刺激频率之间、ChR2 表达与否的动物之间、模型参数（G=0 无耦合 vs G=3 强耦合）之间。
- **对比方法**：
  - 实验层面：与之前电刺激研究（Puig et al. 2010）和光遗传 fMRI 研究（Grandjean et al. 2019）的结果进行比较。
  - 模型层面：对比不同 5-HT 作用机制（E-, I+, E+, I-）对 DOWN 状态诱导的差异。

## 4. 资源与算力
- **文中未明确提及 GPU 型号、数量、训练时长等算力信息**。仅提及使用 Python 中的 `ssm` 包进行 HMM 拟合，以及基于 Allen 连接组数据的网络模型仿真。计算需求属于常规科学计算范畴，未强调大规模算力消耗。

## 5. 实验数量与充分性
- **实验数量**：
  - 动物：5 只实验小鼠 + 2 只对照，共 7 只。
  - 记录：每只小鼠 4 天共 7 次 Neuropixel 插入，总计数十个 session。
  - 刺激：每只小鼠每个频率 50 次重复，总体约 200 次刺激（4 频率 × 50）。
  - 统计分析：覆盖 8 个脑区，数千个神经元。
  - 模型：在不同耦合强度（G=0,1,2,3）和四种刺激机制下进行仿真，并进行了留一法（leave-one-out）相关性检验。
- **充分性与客观性**：
  - **优点**：对照实验（无 ChR2 小鼠）排除了光伪影；模型参数与实验数据匹配（如自然 UP-DOWN 频率 0.5-1 Hz）；留一法检验了相关性的稳健性。
  - **不足**：动物数量较少（尤其对照只有 2 只）；仅使用异氟烷麻醉一种条件，缺乏与其他麻醉剂或自然睡眠的横向比较；未进行药理学操纵验证受体亚型作用（仅基于 Allen 表达数据的相关性）。

## 6. 论文的主要结论与发现
- **主要结论**：
  1. 选择性光遗传激活 DRN 血清素神经元在轻麻醉小鼠中**快速、强烈地诱导 DOWN 状态**（抑制神经活动），效应随刺激频率增加而增强。
  2. 该效应广泛存在于皮层、纹状体、丘脑、杏仁核、海马，但**中脑不受影响**。
  3. 5-HT 刺激可**延长正在进行的 DOWN 状态**，并能**从 UP 状态提前触发 DOWN 状态**。
  4. 脑区间 5-HT1f 和 5-HT2a 受体表达密度与抑制程度正相关，而 DRN 投射强度与抑制程度无显著相关性（模型解释：网络耦合掩盖了直接输入的作用）。
  5. **计算模型揭示**：在强网络耦合下，即使缺乏直接 DRN 输入的脑区（如视觉皮层）也能因网络同步化而被诱导 DOWN 状态；而在无耦合网络中，DOWN 状态概率仅由 DRN 输入决定。
- **关键发现**：血清素在麻醉下是**DOWN 状态的促进剂**，其作用通过网络级动态传播，解决了电刺激与光遗传 fMRI 之间的表观矛盾。

## 7. 优点
- **方法创新**：首次在单个实验中同时实现**全前脑大规模单细胞记录**与**选择性血清素激活**，兼顾了空间覆盖和时程精度。
- **模型与实验的闭环验证**：用生物真实连接的计算模型复现并解释实验现象，并成功预测了无直接输入区域（视觉皮层）的 DOWN 状态来源于网络同步，提升了结论的可靠性。
- **严谨的数据质量控制**：使用标准化的 IBL 预处理和 spike sorting 流程，并包含无 ChR2 表达的严格光学对照。
- **开放科学实践**：数据和代码均公开（ONE 平台和 GitHub），可复现性强。

## 8. 不足与局限
- **实验覆盖**：
  - 仅使用一种麻醉剂（异氟烷），其 UP-DOWN 状态与自然慢波睡眠的等同性仍有争论。
  - 动物数量（5 只有效）较小，可能限制统计泛化能力。
  - 未记录 DRN 本身或脑深部结构的活动，无法直接证实 5-HT 释放与神经抑制的因果链。
- **偏差风险**：
  - 模型为开环架构（DRN→靶区单向投射），未考虑靶区对 DRN 的反馈调节。
  - 对杏仁核、海马的“DOWN 状态”解释较谨慎——它们并不自然表现出双稳态，HMM 可能将普通抑制误判为 DOWN 状态。
  - 受体相关性仅基于 Allen Atlas 表达数据，缺乏药理学因果验证；5-HT1f 的作用需进一步确认。
- **应用限制**：结果主要适用于麻醉状态，对清醒动物行为状态下的血清素功能（如意识、觉醒）的直接推断需谨慎。

（完）
