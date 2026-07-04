---
title: Sample size critically shapes the reliability of EEG case-control findings in psychiatry
title_zh: 样本量对精神病学中EEG病例对照研究结果可靠性的关键影响
authors: "Ebadi, A., Kaderi, S., Rodriguez-Herreros, B., Chabane, N., Allouch, S., Hassan, M."
date: 2026-06-25
pdf: "https://www.biorxiv.org/content/10.1101/2025.11.10.687610v2.full.pdf"
tags: ["query:neuro-mental"]
score: 8.0
evidence: 系统评估样本量如何影响精神病学中EEG病例对照研究的可靠性
tldr: 精神病学中基于脑电图的病例-对照研究结果高度不一致，小样本被认为是不确定性的主要来源但缺乏量化。本研究利用包含2874名5-18岁参与者（含多动症、自闭症、焦虑症、学习障碍及健康对照）的大型多中心静息态EEG数据集，提取频谱、时域和复杂度特征，通过大量随机子采样在不同样本量下反复进行病例-对照比较。结果发现小样本效应量不稳定且夸大，大样本则产生一致的微弱但稳健效应；统计功效随样本量急剧上升，假阳性率保持稳定。研究揭示了样本量对EEG研究结果的关键影响，挑战了传统病例-对照方法在生物标志物发现中的效用。
source: biorxiv
selection_source: carryover_cache
motivation: 精神病学EEG研究结果高度不一致，需系统量化样本量对病例-对照比较可靠性的影响。
method: 利用2874名5-18岁受试者多中心静息态EEG数据集，提取多种特征并进行不同样本量下随机子采样重复比较。
result: 小样本效应量不稳定且夸大，大样本产生一致微弱但稳健效应；统计功效随样本量急剧上升，假阳性率稳定。
conclusion: 样本量是塑造EEG研究结果的核心因素，传统小样本病例-对照方法在生物标志物发现中可靠性不足。
---

## 摘要
精神病学中的脑电图（EEG）研究产生了高度不一致的结果，尤其是在病例对照设计中。小样本量通常被认为是导致这种变异性的因素，但其对EEG组间比较可靠性的影响尚未在大范围内进行系统量化。在此，我们利用一个包含2,874名5-18岁参与者的多中心静息态EEG数据集来填补这一关键空白，其中包括注意力缺陷/多动障碍、自闭症谱系障碍、焦虑症、学习障碍患者以及健康对照。我们提取了一套全面的频谱、时间及复杂性EEG特征，并通过大量随机子采样，在多种样本量下进行了反复的病例对照比较。小样本的结果不稳定，效应量被夸大且在不同迭代间高度变异。相比之下，较大样本产生了一致且可重复的结果，收敛于虽小但稳健的效应。统计功效随样本量急剧增加，而假阳性率保持相对稳定。这些结果证明了样本量在塑造EEG研究结果中的核心作用，并对传统病例对照方法在精神病学生物标志物发现中的实用性提出了挑战。

## Abstract
Electroencephalography (EEG) studies in psychiatry have produced highly inconsistent findings, particularly in case-control designs. Small sample sizes are widely assumed to contribute to this variability, yet their impact on the reliability of EEG group comparisons has not been systematically quantified at scale. Here, we address this key gap using a large multisite resting-state EEG dataset comprising 2,874 participants aged 5-18 years, including individuals with attention-deficit/hyperactivity disorder, autism spectrum disorder, anxiety, learning disorders, and healthy controls. We extracted a comprehensive set of spectral, temporal, and complexity EEG features and performed repeated case-control comparisons across a wide range of sample sizes using extensive random subsampling. Results from small samples were unstable, with inflated and highly variable effect sizes across iterations. By contrast, larger samples produced consistent and reproducible findings, converging on uniformly small but robust effects. Statistical power rose steeply with sample size, whereas false positive rates remained relatively stable. These results demonstrate the central role of sample size in shaping EEG study outcomes and challenge the utility of conventional case-control approaches for biomarker discovery in psychiatry.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：精神病学中基于脑电图（EEG）的病例-对照研究结果高度不一致，小样本被认为是导致这种变异性的主要原因，但缺乏系统量化。本研究旨在精确量化样本量如何影响EEG组间比较的可靠性。
- **背景**：典型EEG生物标志物研究每组仅招募约30名参与者，统计功效严重不足，导致效应量不稳定、可重复性差。此前类似工作多集中于fMRI/MRI领域（Marek et al., 2022），而EEG领域缺少大规模量化评估。
- **研究含义**：如果小样本带来的不稳定性被证实，将直接挑战传统小样本病例-对照设计在生物标志物发现中的有效性，并为未来研究设计和样本量规划提供关键定量依据。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：通过在大规模多中心EEG数据集中反复随机子采样，系统模拟不同样本量（n=10~550）下的病例-对照比较，评估统计结果的稳定性、效应量大小及空间模式的可重复性。
- **关键技术细节**：
  - **数据预处理**：将原始128通道数据降采样至19通道（标准10-20系统），带通滤波1-45 Hz，降采样至200 Hz，坏导检测与插值（pyprep），共平均重参考，ICA去除眼动伪影（IClabel），分割为10秒非重叠epoch，使用Autoreject拒绝伪迹epoch。最后对每个被试做z变换（减均值除标准差）。
  - **特征提取**：共提取103个EEG特征，涵盖频域（绝对/相对功率、频带功率比、α峰频率、非周期成分参数）、时域（振幅均值、标准差、偏度、峰度、包络统计量）、复杂度（近似熵、样本熵、谱熵、Hjorth参数、Hurst指数、分形维数、DFA、Lempel-Ziv复杂度）以及Catch22时间序列特征。每个特征在19个通道上分别计算，并计算通道均值，最终得到2060个特征-通道对。
  - **特征协调**：使用neuroCombat消除多中心效应，保留年龄、性别、诊断组效应。
  - **反复子采样框架**：从健康对照和患者组中各随机抽取等量被试（初始n=10，步长10递增至最大可用样本量），进行ANCOVA（年龄、性别为协变量），每次迭代记录p值和效应量（偏η²）。每种样本量重复1000次迭代。
  - **可靠性指标**：显著性百分比（p<0.05的迭代比例）、样本量阈值（95%迭代显著的最小n）、Jaccard相似度（与全样本空间模式的匹配）、归一化熵（空间模式多样性）、统计功效、假阳性率、假阴性率、效应量膨胀比（子样本效应量/全样本效应量）。

## 3. 实验设计：使用的数据集、基准、对比方法

- **数据集**：整合5个独立研究，共2874名5-18岁参与者（558名健康对照，1221名ADHD，554名ASD，305名焦虑症，236名学习障碍）。具体来源：HBN、MIPDB、ABCCT、femaleASD、LausanneASD。受试者中41%存在共病，诊断按首位诊断保留。
- **基准**：以全样本（最大可用样本量）分析结果为参考“真值”，比较不同子样本量下的结果相对于全样本的偏差。
- **对比方法**：
  - 不同样本量之间相互对比（n=10到最大）。
  - 不同诊断组之间对比（ADHD、ASD、焦虑、学习障碍）。
  - 不同EEG特征类型之间对比（频谱、时域、复杂度）。
  - 控制分析：共病性影响（单诊断ADHD vs 共病ADHD）、epoch长度影响（2/4/6/8秒 vs 10秒）。

## 4. 资源与算力

- **文中未明确说明使用的GPU型号、数量或训练时长**。只提到使用了Python包（MNE、pingouin、neuroCombat等）进行信号处理和统计分析。考虑到计算量（2060特征×19通道×多种样本量×1000迭代×4诊断组），需要一定计算资源，但论文未提供细节。

## 5. 实验数量与充分性

- **实验数量**：非常充分。包括：
  - 4个诊断组分别与健康对照比较。
  - 样本量从10到最大（约550）共约50个不同样本量水平，每个水平1000次随机子采样。
  - 2060个特征-通道对进行分析。
  - 5个可靠性指标（显著性百分比、阈值、Jaccard相似度、熵、效应量膨胀）。
  - 2个控制分析（共病性、epoch长度）。
- **充分性评价**：实验设计系统、全面，覆盖了多个诊断类别、多种特征类型、多种空间尺度和多种统计指标。控制分析检验了主要混杂因素（共病性、epoch长度），增加结论稳健性。由于使用真实大规模数据集而非模拟，结果更具现实意义。实验客观、公平：所有比较使用相同预处理、特征提取和统计方法，子采样过程随机重复减少偶然性。

## 6. 论文的主要结论与发现

1. **小样本导致结果不稳定**：在n=30（典型研究规模）时，相同比较在不同子样本间方向可变、效应量波动剧烈，空间模式（显著通道集）与全样本几乎无重叠（Jaccard相似度接近0）。
2. **统计功效随样本量急剧上升**：n=30时平均功效仅~10%，假阳性率约4.86%；样本增大后功效迅速提高，假阳性率仅轻微增加。
3. **效应量显著膨胀**：在n=30时，98.6%的显著特征效应量比全样本大5倍以上；随样本增大，效应量收敛于极小值（偏η²全部<0.06）。
4. **样本量阈值远高于常规**：达到95%显著性一致所需样本量，ADHD和ASD中位数约480人，焦虑约256人，学习障碍约218人，远超典型EEG研究。
5. **诊断特异性弱**：大多数显著特征跨诊断共享（32.8%），而非疾病特有，提示EEG改变主要为跨诊断性质。
6. **共病性和epoch长度影响有限**：共病性仅引起微小效应量变化；不同epoch长度虽改变特征分布，但对组间比较结果影响很小（平均5.6%特征改变显著性，且效应量仍极小）。

## 7. 优点：方法或实验设计上的亮点

- **大规模真实数据**：利用2874名参与者的多中心数据集，为评估样本量影响提供了足够统计能力和外部效度。
- **系统性量化框架**：提出包含多种统计推断误差和空间稳定性指标的重复子采样流程，全面刻画小样本问题。
- **多模态特征覆盖**：提取103个特征涵盖频谱、时域、复杂度等多个维度，避免单一特征偏倚，反映方法学普遍性。
- **控制混杂因素**：使用neuroCombat协调多中心效应，控制年龄性别协变量，并专门检验共病性和epoch长度。
- **结论直接挑战范式**：明确指出现有病例-对照设计在生物标志物发现中的根本局限，推动转向维度化、亚型分析等新范式。

## 8. 不足与局限：包括实验覆盖、偏差风险、应用限制

- **样本量上限有限**：最大样本约~550人，对于某些细微效应可能仍不足。论文指出与大型fMRI研究相比规模较小。
- **年龄范围局限**：参与者仅5-18岁，结果可能不适用于成人或老年人群。
- **诊断类别不均衡**：ADHD组最大（1221），学习障碍最小（236），可能影响组间比较的统计功效。
- **共病性问题简化**：仅保留首位诊断，未深入分析共病组合模式对结果的影响。
- **仅使用静息态EO条件**：未涵盖任务态或闭眼条件，可能遗漏某些生物标志物。
- **未考虑个体内变异性**：未评估同一被试不同时段或不同epoch变异性对结果的影响。
- **方法学假设限制**：子采样假设全样本结果为“真值”，但全样本本身可能仍存在未消除的混杂（如药物、共病、数据质量差异）。
- **临床转化建议有限**：论文虽指出病例-对照方法的局限，但未提供具体可靠的替代方案（如亚型分析、规范性建模）的实证比较。
- **未报告算力需求**：缺少计算资源细节，不利于其他研究复现或估计成本。

（完）
