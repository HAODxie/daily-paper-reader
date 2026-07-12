---
title: Optimizing MR-based gaze-decoding for eyes-closed eye-tracking in fMRI
title_zh: 优化基于MR的注视解码用于fMRI中的闭眼眼动追踪
authors: "Kling, S. M., Lascombes, U., Nau, M., Masson, G. S., Szinte, M."
date: 2026-07-11
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.07.736972v1.full.pdf"
tags: ["query:neuro-mental"]
score: 8.0
evidence: 用于fMRI眼动解码的深度学习框架
tldr: 在fMRI研究中，闭眼时相机眼动追踪不可用，限制了认知研究。本文通过DeepMReye深度学习框架从MR信号解码凝视，利用睁眼校准数据微调模型，并进一步结合闭眼注视数据提升性能。结果表明，微调显著改善解码精度，模型成功泛化到闭眼时段。该工作实现了闭眼期间可靠的凝视监测，促进了fMRI中眼动追踪的有效整合，有助于深化对人类认知的理解。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736972-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1752, \"height\": 752, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736972-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1719, \"height\": 699, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-07-736972-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1737, \"height\": 734, \"label\": \"Figure\"}]"
motivation: 解决闭眼时相机眼动追踪缺失的问题，实现基于MR信号的可靠凝视解码。
method: 使用DeepMReye模型，通过睁眼视动校准数据微调，并引入闭眼注视数据进一步优化。
result: 微调显著提升解码性能，模型成功泛化到闭眼时段。
conclusion: 实现了闭眼期间可靠的凝视监测，促进fMRI眼动追踪整合与认知研究。
---

## 摘要
眼动为人类认知提供了宝贵的见解，并且是众多功能性磁共振成像（fMRI）研究中的关键变量。然而，当眼睛闭合时，基于摄像头的眼动追踪不可用，这使得对闭眼状态的研究具有挑战性。在此，我们通过基于MR的注视解码（使用DeepMReye）来弥补这一空白，DeepMReye是一种深度学习框架，可从眼睛的MR信号中无摄像头地重建注视行为。我们首先证明，使用睁眼时获取的视觉运动校准数据对DeepMReye进行微调可以显著改善注视解码，并且这种微调不需要同时获取基于摄像头的数据。接下来，我们评估了通过结合参与者在睁眼和闭眼状态下注视已知位置时获取的数据是否可以进一步提高模型性能。值得注意的是，虽然DeepMReye最初仅使用睁眼数据进行训练，但该网络成功推广到闭眼时段，并且通过对闭眼数据进行微调，性能显著提升。这些发现表明，在闭眼期间进行可靠的注视监测是可行的，从而能够在fMRI研究中更有效地整合眼动追踪，进而增进我们对人类认知的理解。

## Abstract
Eye movements provide valuable insights into human cognition and are a critical variable in numerous functional magnetic resonance imaging (fMRI) studies. Yet, when the eyes are closed, camera-based eye-tracking is unavailable, making studies of eyes-closed states challenging. Here, we address this gap through MR-based gaze decoding with DeepMReye, a deep learning framework for camera-free reconstruction of gaze behavior from the MR-signal of the eyes. We first show that fine-tuning DeepMReye using visuomotor calibration data acquired when the eyes were open significantly improves gaze decoding, and that this fine-tuning does not require simultaneous camera-based data. We next assessed whether model performance could be further improved by incorporating data acquired while participants gazed at known positions with both eyes open and closed. Notably, while DeepMReye was originally trained exclusively on eyes-open data, the network successfully generalized eyes-closed periods, with performance improving significantly through fine-tuning on the eyes-closed data. These findings demonstrate that reliable gaze monitoring during eyes-closed periods is feasible, enabling a more effective integration of eye-tracking in fMRI research and, consequently, advancing our understanding of human cognition.

---

## 论文详细总结（自动生成）

# 论文详细中文总结：优化基于MR的注视解码用于fMRI中的闭眼眼动追踪

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：功能性磁共振成像（fMRI）研究中，眼动追踪对于控制注意力、验证任务依从性和提高数据可解释性至关重要。然而，传统的基于摄像头的眼动追踪系统在MRI环境中面临成本高、设置受限、信号中断等问题，最关键的是，它要求参与者的眼睛始终睁开，因此无法用于闭眼状态（如睡眠、闭眼静息态、心理意象等）的研究。这极大地限制了fMRI对多种认知状态的研究范围。
- **研究动机**：最近出现的利用眼球MR信号直接解码凝视的深度学习方法（如DeepMReye）提供了一种无摄像头的替代方案，但该模型主要针对睁眼条件验证，在闭眼条件下的性能证据有限。眼动动力学在睁眼与闭眼之间存在显著差异（例如Bell现象、扫视频率降低等），因此需要专门研究如何优化该模型以适用于闭眼场景。
- **整体含义**：本研究旨在克服这一空白，通过微调DeepMReye模型，使其能够可靠地解码闭眼状态下的凝视行为，从而将眼动追踪的应用范围从睁眼扩展到闭眼，为睡眠神经成像、闭眼静息态研究、视觉意象任务等开辟新可能，并为回顾性分析大量缺少眼动数据的大型fMRI数据集提供基础。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：利用参与者短时间的视动校准数据（睁眼时进行经典的引导注视、引导平滑追踪、自由观看任务）对DeepMReye模型进行微调，以适配本地实验装置（更大的显示屏幕）。进一步，开发一种新型的听觉引导眼动范式，使参与者能够在闭眼或无视视觉输入条件下执行结构化的眼动（追踪三角形路径），从而生成闭眼条件下的训练数据，并用这些数据对模型进行微调。
- **关键技术细节**：
  - **DeepMReye网络结构**：卷积神经网络，输入为眼球区域（从BOLD图像中提取的眼部掩膜体素），输出为2D凝视位置（x, y坐标），使用两个损失函数：欧几里得误差（EE）和预测误差（PE）之间的差异。
  - **微调策略**：在预训练模型基础上，使用新数据集（参与者特定的BOLD信号和对应凝视标签）重新训练。训练参数：学习率2e-6，批次大小15个参与者，每轮步数5000，轮数1，验证步数1，学习率衰减0.03。采用五折交叉验证（80%训练，20%测试）。
  - **标签生成**：对于睁眼条件，从摄像头眼动追踪数据中提取10个凝视位置/TR作为训练标签（通过质量控制和下采样）；对于闭眼条件，标签设为NaN（训练时不提供凝视位置）。也尝试使用已知目标位置作为训练标签（无需摄像头数据）。
  - **缩放模型对照**：为了区分微调效果是否仅仅来自输出缩放，构建了“Scaled DeepMReye”，即对预训练模型的输出拟合线性回归模型进行缩放。

## 3. 实验设计

- **数据集**：17名参与者（排除2名后剩余15名），在3T西门子Prisma扫描仪上采集数据。使用2mm各向同性分辨率、TR=1.2s的EPI序列，全脑60层轴向切片。同时记录基于摄像头的眼动追踪数据（Eyelink 1000，13点校准）。
- **任务设计**：
  - **视动校准任务**：（睁眼）包括引导注视（50 trials，1.2s/trial，覆盖18 dva方形内25个位置）、引导平滑追踪（54 trials，1.2s/trial，振幅3/5/7 dva，角度随机）、自由观看（10 trials，3.6s/trial，自然图像）。共3个功能运行，每运行约3分钟。
  - **视觉/眼状态任务**：包括4个条件，每个条件中参与者根据听觉音调序列追踪三角形路径（8个三角形序列）：①视力+睁眼；②视力+眨眼（在目标点期间眨眼）；③无视力+睁眼；④无视力+闭眼。共3个功能运行，每运行约6分钟。
- **基准（benchmark）**：以摄像头眼动追踪数据为参考（睁眼时），评估解码的欧几里得误差和皮尔逊相关系数。对于闭眼条件，通过训练逻辑回归分类器（基于解码的凝视轨迹）识别三角形朝向的准确率来间接评估。
- **对比方法**：
  - **DeepMReye**：原始预训练模型（来自Frey et al. 2021）。
  - **DeepMReye & visuomotor calibration**：在视动校准任务数据上微调的模型。
  - **DeepMReye & visual/eyes state**：在视觉/眼状态任务数据上微调的模型。
  - **Scaled DeepMReye**：对预训练模型输出进行线性缩放。
  - **目标位置标签 vs 眼动追踪标签**：比较使用已知目标位置作为训练标签与使用实际眼动数据作为标签的效果。

## 4. 资源与算力

- 文中**未明确说明**训练DeepMReye所使用的具体GPU型号、数量或训练时长。仅提供了微调的参数（学习率2e-6，批次大小15，步数5000等），以及使用五折交叉验证。未提及原始预训练模型的训练资源。

## 5. 实验数量与充分性

- **实验组数**：
  - 视动校准任务：对比4种模型（DeepMReye, DeepMReye & visuomotor calibration, Scaled DeepMReye, 以及使用目标位置标签训练的模型）在3个任务部分（引导注视、引导追踪、自由观看）上的性能，各报告了相关系数和欧几里得误差。
  - 视觉/眼状态任务：对比3种模型（DeepMReye, DeepMReye & visuomotor calibration, DeepMReye & visual/eyes state）在4个条件（视力+睁眼、视力+眨眼、无视力+睁眼、无视力+闭眼）上，采用两种评估方式（时间有序的坐标和时间打乱的坐标）的分类准确率。
  - 眼睑状态解码：对比3种模型在眨眼条件下的眼睑状态分类准确率和相关性。
  - 所有统计检验使用非参数置换检验（10,000次随机排列，单侧检验）。
- **充分性评价**：
  - **实验设计充分**：涵盖了睁眼/闭眼多条件，对比了不同微调策略和缩放控制，并使用了交叉验证。样本量15，对于深度学习微调而言偏小，但考虑到参与者内交叉验证，统计检验仍然有效。
  - **客观性**：使用基于摄像头的眼动数据作为睁眼条件的真实值，并在闭眼条件下通过分类任务间接评估，避免了循环论证。但闭眼条件下缺乏直接真实值，分类准确率主要反映空间形状信息，不足以精确评估单个注视位置的准确性。
  - **消融实验**：通过缩放模型对比、目标位置标签对比、以及不同微调数据源对比，较好地隔离了各个因素的影响。

## 6. 论文的主要结论与发现

1. **微调显著提升睁眼条件下的解码性能**：在引导注视、引导追踪和自由观看部分，微调模型（DeepMReye & visuomotor calibration）相比预训练模型，相关系数显著提高，欧几里得误差显著降低（自由观看部分误差无显著差异）。线性缩放模型表现不如微调模型，表明微调的增益不仅仅是输出缩放。
2. **微调无需摄像头眼动数据**：使用已知目标位置作为训练标签进行微调，性能与使用实际眼动数据标签相当（仅引导注视部分略有下降），证明无需昂贵眼动设备即可进行模型适配。
3. **闭眼条件下的解码可行**：即使在无视觉输入且闭眼时，通过听觉引导的三角形追踪任务，解码的凝视轨迹可用于分类三角形方向。时间打乱坐标后，微调模型显著提升了分类准确率（从50%提升至约57%），而睁眼微调模型提升有限。
4. **眼睑状态可被解码**：在眨眼条件下，微调模型（包括仅用睁眼数据微调的模型）即可达到约79%的分类准确率，区分睁眼与闭眼。额外的闭眼数据微调并未带来显著提升。
5. **模型泛化能力**：DeepMReye原始仅用睁眼数据训练，但成功泛化到闭眼数据；通过包含闭眼数据微调，性能进一步提升。

## 7. 优点

- **创新性**：首次系统评估并优化DeepMReye在闭眼条件下的解码能力，开发了新颖的听觉引导闭眼眼动范式，为解决fMRI中闭眼眼动追踪这一长期空白提供了实用方案。
- **实用性**：证明了微调可以在没有摄像头眼动数据的条件下进行（使用已知目标位置），并公开了模型权重，降低了技术门槛，便于其他实验室应用。
- **实验设计严谨**：通过多种对比模型（缩放模型、不同微调数据源）和两种评估方式（时间有序/打乱）来分离时序信息和空间信息，增强了结论的可靠性。
- **跨领域潜力**：将眼动追踪扩展到睡眠、静息态、临床人群等此前难以研究的场景，具有重要的理论和方法学价值。

## 8. 不足与局限

- **闭眼条件的真实值缺失**：闭眼时无法获得地面真实凝视位置，只能通过分类准确率间接评估，而分类准确率仅反映形状辨别能力，无法评估单个注视位置的精度或轨迹保真度。这是该领域固有的挑战，但论文对此讨论充分。
- **闭眼眼动本身的变异性**：无视觉反馈下，眼动本身更不稳定、更不精确（Bell现象、扫视频率降低、空间误差累积），导致解码性能的天花板可能并非来自模型，而是来自信号本身。论文指出这一点，但未量化。
- **样本量较小**：15名参与者，且部分参与者为作者（非完全盲）。虽然统计检验使用非参数方法，但结果的可推广性可能受限。
- **眼睑状态解码的时间分辨率限制**：DeepMReye输出基于TR（1.2s），无法检测单个快速眨眼事件，只能区分持续的开闭眼时段，不适合需要高时间分辨率的眨眼检测应用。
- **听觉引导范式的可行性限制**：该范式要求参与者可靠地执行结构化眼动序列，在部分临床人群（如意识障碍患者、幼儿）中可能难以实施。论文提到了这一点。
- **自由观看条件下的性能有限**：自由观看部分的解码误差改善不显著（欧几里得误差无显著差异），表明该方法在自然场景中的实用性仍有待提高。论文指出需要更大的自由观看数据集重新训练或开发无监督方法。

（完）
