---
title: "Detecting Sleep Deprivation from Running Biomechanics Using Machine Learning Classification: A Comparison Between Wearable and Laboratory Motion Capture"
title_zh: 使用机器学习分类从跑步生物力学检测睡眠剥夺：可穿戴与实验室运动捕捉的比较
authors: "Seynaeve, M., Hendrickx, K., Vanwanseele, B., de Beukelaar, T."
date: 2026-07-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.14.738397v1.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 使用机器学习从跑步生物力学检测睡眠剥夺
tldr: "睡眠剥夺会损害跑步表现并增加受伤风险，但实验室发现的生物力学变化能否被可穿戴设备检测尚不清楚。本研究对21名跑者进行正常睡眠与完全睡眠剥夺的交叉实验，同时使用全身运动捕捉和躯干可穿戴传感器采集步态数据，并采用五种机器学习分类器分析。结果表明，内受试者分类准确率可穿戴达85%（逻辑回归）、运动捕捉为83%（随机森林），而外受试者分类均接近随机水平（约50%），说明个体差异掩盖了睡眠剥夺信号。研究强调，个体化基线参考监测对检测睡眠剥夺相关步态变化至关重要，且单躯干可穿戴传感器能提供实用的现实世界监测方案。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738397-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1782, \"height\": 453, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738397-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1734, \"height\": 769, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-14-738397-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1660, \"height\": 632, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-14-738397-v1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1725, \"height\": 637, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-14-738397-v1/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1565, \"height\": 830, \"label\": \"Table\"}]"
motivation: 探究可穿戴技术能否检测睡眠剥夺引起的跑步生物力学变化，并比较其与实验室运动捕捉系统的效果。
method: 21名跑者在正常睡眠和完全睡眠剥夺后跑步，同时采集全身运动捕捉和躯干可穿戴传感器数据，用五种机器学习模型进行内受试者与外受试者分类。
result: "内受试者分类可穿戴85%、运动捕捉83%准确率；外受试者分类失败（~50%），表明需个体基线参考。"
conclusion: 个体化基线监测是检测睡眠剥夺步态变化的关键，单躯干可穿戴传感器可实用替代实验室系统。
---

## 摘要
睡眠剥夺与耐力表现受损以及跑步相关损伤风险增加有关。先前的研究已发现，在实验室条件下，一夜睡眠剥夺后跑步生物力学发生变化。然而，这些生物力学变化是否能通过可穿戴技术检测尚不清楚。21名休闲活跃跑步者在随机交叉设计中，在正常睡眠和完全睡眠剥夺条件下完成了次最大跑步机跑步。同时使用全身运动捕捉系统和躯干安装的可穿戴传感器提取生物力学特征。在两种分类任务中评估了五种机器学习分类器：使用同一受试者配对记录的个体内任务，以及无个体基线数据的个体间任务。对于两种测量系统，个体内分类始终超过随机水平，可穿戴传感器（逻辑回归）的最佳准确率为85%，运动捕捉系统（随机森林）为83%。这些发现表明，睡眠剥夺在跑步过程中产生系统性和个体一致的生物力学特征。相比之下，几乎所有模型和系统的个体间分类均失败，准确率接近随机水平（约50%），表明在缺乏个性化基线数据的情况下，个体间变异掩盖了睡眠剥夺信号。两种系统均汇聚于时间组织、负荷相关变量和步幅间变异性作为最具区分性的特征域。与预期相反，实验室运动捕捉系统并未优于可穿戴传感器。总之，这些发现表明，个性化、基于基线的监测对于检测跑步步态中与睡眠剥夺相关的变化至关重要，并提示当存在配对记录时，单个躯干安装的可穿戴传感器可能为实际监测提供实用解决方案。

## Abstract
Sleep deprivation is associated with impaired endurance performance and an increased risk of running-related injury. Previous research has identified alterations in running biomechanics following a single night of sleep deprivation under laboratory conditions. However, whether these biomechanical changes can be detected using wearable technology remains unknown. Twenty-one recreationally active runners completed submaximal treadmill running under both normal sleep and total sleep deprivation conditions in a randomized crossover design. Biomechanical features were extracted simultaneously using a full-body motion capture system and a trunk-mounted wearable sensor. Five machine learning classifiers were evaluated in two classification tasks: a within-subject task using paired recordings from the same individual, and a between-subject task performed without individual baseline data. Within-subject classification consistently exceeded chance level for both measurement systems, with best accuracies of 85% for the wearable sensor (Logistic Regression) and 83% for the motion capture system (Random Forest). These findings indicate that sleep deprivation produces a systematic and individually consistent biomechanical signature during running. In contrast, between-subject classification failed across nearly all models and systems, with accuracies remaining close to chance level (~50%), demonstrating that inter-individual variability obscures the sleep-deprivation signal in the absence of personalized baseline data. Both systems converged on temporal organization, loading-related variables, and stride-to-stride variability as the most discriminative feature domains. Contrary to expectations, the laboratory motion capture system did not outperform the wearable sensor. Together, these findings demonstrate that individualized, baseline-referenced monitoring is essential for detecting sleep-deprivation-related changes in running gait, and suggest that a single trunk-mounted wearable sensor may provide a practical solution for real-world monitoring when paired recordings are available.

---

## 论文详细总结（自动生成）

好的，以下是对该论文的详细中文总结。

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：睡眠剥夺会损害跑步表现并增加受伤风险。虽然已有实验室研究证实一夜睡眠剥夺会改变跑步生物力学，但尚未明确这些变化能否被更便捷、成本更低的 **可穿戴设备** 有效检测出来。本研究旨在探究此问题，并比较可穿戴传感器与实验室高精度运动捕捉系统在检测这类变化上的性能差异。
- **整体含义**：如果可穿戴设备能够可靠地检测睡眠剥夺引起的步态变化，将有助于教练、运动员和医疗从业者在日常训练中监测疲劳状态、评估受伤风险，从而制定更科学的训练和恢复计划。

### 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：利用 **机器学习分类器**，从跑步生物力学数据中识别睡眠剥夺状态。研究对比了两种分类策略：
    1.  **个体内分类 (Within-subject)**：使用同一受试者在正常睡眠（CON）和睡眠剥夺（SDEP）条件下的配对数据。通过计算两次数据的差值向量（CON - SDEP 和 SDEP - CON），消除了个体间差异，旨在检测睡眠剥夺引起的**个体内部**的、**方向性**的步态变化。
    2.  **个体间分类 (Between-subject)**：不使用配对数据，直接将所有受试者的单次测量数据（CON或SDEP）混合，要求模型学习一个跨个体的、普遍适用的模式来区分两种状态。
- **关键技术细节**：
    1.  **数据采集**：受试者分别在正常睡眠和完全睡眠剥夺后，在固定速度的跑步机上进行次最大强度跑步。
    2.  **特征提取**：
        - **实验室系统 (Vicon)**：从全身运动捕捉数据中提取了 **83个** 生物力学特征，涵盖时空、运动学、动力学和关节功率等参数。
        - **可穿戴系统 (Runeasi)**：从单个躯干（腰部）佩戴的惯性传感器中提取了 **36个** 特征，包括步频、触地时间、冲击幅值、动态稳定性等指标的平均值、标准差和左右不对称性。
    3.  **机器学习流程**：
        - **模型**：评估了5种分类器：逻辑回归 (Logistic Regression)、决策树 (Decision Tree)、随机森林 (Random Forest)、K近邻 (k-NN) 和极限梯度提升 (XGBoost)。
        - **数据处理**：在每一折交叉验证中，严格遵循“在训练集上拟合”的原则，依次进行**标准化**、基于 **方差分析 (ANOVA)** 的特征选择，最后训练分类器。
        - **验证**：采用 **嵌套交叉验证** 框架，外层10折用于评估泛化性能，内层网格搜索用于优化超参数（包括保留的特征数量k）。使用基于受试者分组的交叉验证（GroupKFold），确保同一受试者的数据不会同时出现在训练集和测试集中。

### 3. 实验设计：数据集、基准与对比方法

- **数据集**：21名健康、热爱跑步的年轻人（21名进入最终分析，1名因数据缺失被排除）。数据在受控的实验室条件下采集。
- **场景**：受试者在四个递增速度的跑步间隔中进行测试（3个8分钟次最大间隔 + 1个力竭间隔）。
- **基准 (Benchmark)**：以 **50%的随机水平 (chance level)** 作为分类性能的基准。
- **对比方法**：
    1.  **测量系统对比**：实验室 **Vicon** 运动捕捉系统 vs. 可穿戴 **Runeasi** 传感器。
    2.  **分类任务对比**：**个体内分类** vs. **个体间分类**。
    3.  **模型对比**：5种不同的机器学习分类器（LR, DT, RF, k-NN, XGBoost）在两种系统和两种任务下的表现。

### 4. 资源与算力

- **文中未明确说明**：论文没有提及训练模型所使用的具体硬件资源，如GPU型号、数量或训练时长。考虑到其特征维度和数据量（21名受试者 × 多种速度条件），这些分类任务的计算负荷相对较低，可能在普通的CPU上即可完成。

### 5. 实验数量与充分性

- **实验数量**：研究进行了全面的对比实验，总共产生了 **4个主要分类管线**（2种测量系统 × 2种分类任务），每个管线均使用5种模型和嵌套交叉验证进行评估。
- **充分性**：
    - **优点**：实验设计考虑周到，对比了不同类型的分类任务（个体内 vs. 个体间）和技术路线（实验室 vs. 可穿戴），并使用多种模型进行验证，增强了结论的可靠性。嵌套交叉验证和基于受试者的分组确保了评估的客观性和公平性。
    - **不足**：
        1.  **样本量较小**：仅21名受试者，可能导致模型性能（尤其是更为复杂的模型如随机森林）的交叉验证折叠之间波动较大（标准差高），影响统计稳定性。
        2.  **未进行特征稳定性分析**：未评估不同折叠或亚组之间所选特征集的一致性，特征重要性结果仅为描述性，缺乏统计检验。

### 6. 论文的主要结论与发现

1.  **可检测性**：睡眠剥夺确实会在个体层面产生系统性的、可被检测的步态生物力学信号。**个体内分类**在所有模型和两种测量系统下均**显著超过随机水平**（可穿戴系统最高 **85%**，实验室系统最高 **83%**）。
2.  **个体基线至关重要**：**个体间分类**完全失败，大多数模型准确率徘徊在 **50%** 的随机水平。这表明，在缺乏个人基线数据的情况下，个体间的巨大步态差异完全掩盖了由睡眠剥夺引起的微小变化。**个性化、基于个体基线的监测是必要的**。
3.  **可穿戴不逊于实验室系统**：**出乎预期**的是，复杂的实验室运动捕捉系统并未优于一个简单的躯干可穿戴传感器。两者在个体内分类任务中表现相当，表明单点可穿戴传感器在检测此类变化时是实验室系统的有效且实用的替代方案。
4.  **关键生物力学特征**：两种系统在其最有效的特征上表现出**一致性**。区分睡眠剥夺状态的最重要特征是**时间组织**（如步频、触地时间）、**负荷相关变量**（如冲击幅值、最大负荷率）以及**步幅间变异性**（如特征的标准差）。这表明睡眠剥夺主要影响跑步的节奏控制、冲击缓冲和动作的一致性。

### 7. 优点：方法或实验设计上的亮点

- **临床与实际意义强**：聚焦于睡眠剥夺这一影响广泛但研究不足的疲劳来源，结论对运动员日常疲劳管理和损伤预防具有直接指导意义。
- **明确的方法论贡献**：清晰地展示了**个体内配对分析**在捕捉细微生物力学变化上的必要性，为后续相关研究提供了重要的方法论指导。
- **公平的对比**：在完全相同的实验条件下，同时测量和对比了实验室系统和可穿戴传感器，使得性能差异的归因更加可靠。
- **严谨的验证框架**：采用嵌套交叉验证和基于受试者的分组，有效防止了数据泄露和结果过拟合，保证了结论的客观性。

### 8. 不足与局限：包括实验覆盖、偏差风险、应用限制

- **外部效度有限**：
    - **极端条件**：实验采用“完全睡眠剥夺”这一极端情况，不如“部分睡眠剥夺”或“慢性睡眠不足”常见，后者的影响可能更微妙。
    - **实验环境**：所有测试均在**跑步机**上进行，且速度固定，可能无法完全代表真实路跑中的自然步态和速度调节。
    - **样本同质性**：受试者为年轻、健康的休闲跑者，结论能否推广到精英运动员、老年跑者或受伤人群尚不明确。
- **方法学局限**：
    - **样本量小**：导致交叉验证性能波动大，结果稳健性受质疑。
    - **算法透明度**：可穿戴系统（Runeasi）使用**专有算法**处理原始数据，部分指标的计算方式不透明，限制了跨平台的可重复性和机理推断。
    - **特征重要性**：基于全数据集计算，属于描述性而非推断性结论，且不同模型的重要性度量（如系数、基尼系数）存在差异，不应视为生理敏感性的直接指示。
- **潜在利益冲突**：作者之一为可穿戴设备公司 Runeasi 的联合创始人。尽管文中声明数据分析在工作入职前完成，但其参与可能引入偏差。

（完）
