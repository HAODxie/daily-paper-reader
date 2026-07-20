---
title: "Large-Scale Assessment of Language, Speech, and Movement in Autism and ADHD with AI"
title_zh: 基于AI的自闭症与多动症语言、言语及运动的大规模评估
authors: "Silvan, A., Parra, L. C., Franco, A. R., Di Martino, A., Milham, M., Madsen, J."
date: 2026-07-16
pdf: "https://www.biorxiv.org/content/10.1101/2025.10.20.682864v3.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 自闭症、ADHD、心理健康、AI行为分析
tldr: ADHD与ASD常共病且行为重叠，传统诊断依赖主观观察。本研究创新性地利用AI对2529名5-22岁儿童的临床访谈进行自动音视频分析，提取多模态行为特征。通过多变量模型发现，语言困难主要由年龄、认知或共病ASD解释，而非ADHD；多动冲动型ADHD特异表现为运动增加；ASD则展现独特高音调、嘶哑声音及叙事异常。研究证实数字评估能有效分离两病症域特异性行为特征，为大规模客观诊断提供新方法。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-20-682864-v3/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1857, \"height\": 1591, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-20-682864-v3/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1876, \"height\": 998, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-20-682864-v3/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1861, \"height\": 1807, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-20-682864-v3/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1875, \"height\": 521, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-20-682864-v3/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1872, \"height\": 518, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-1101-2025-10-20-682864-v3/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1865, \"height\": 746, \"label\": \"Table\"}]"
motivation: 现有ADHD与ASD诊断依赖主观评估，难以分离共病重叠特征，亟需客观量化工具。
method: 对2529名青少年临床访谈的音视频进行AI自动化分析，提取语言、声音、运动多模态特征并建立多变量模型。
result: 语言困难取决于年龄、认知或共病ASD；多动冲动型ADHD有运动增加；ASD呈现高音调嘶哑声音和叙事异常。
conclusion: 基于临床访谈的数字行为测量可分离ASD与ADHD的域特异性症状，具备大规模推广潜力。
---

## 摘要
注意缺陷/多动障碍（ADHD）和自闭症谱系障碍（ASD）常同时发生，且具有重叠特征。本研究探讨在临床医生与儿童访谈过程中，自动化行为分析能否识别出两种障碍的独特客观特征。通过对广泛社区样本中2529名青少年（5-22岁）的音视频记录进行分析，多变量模型揭示，常归因于ADHD的语言困难主要由年龄、认知能力或共病ASD解释。运动活动增加特异地标志了多动-冲动型ADHD，而非ASD或注意缺陷型ADHD。ASD的独特特征表现为分歧的叙事产生和特异反应，以及尽管语言结构完整，但具有独特的声音特征：更高的音调和发声困难。虽然这些数字行为测量与大多数诊断类别和年龄相关，但联合分析能有效分离ASD与ADHD的影响。这些发现表明，基于记录临床访谈的可扩展数字评估能够将重叠的ASD和ADHD诊断分解为特定领域的行为特征。

## Abstract
Attention-Deficit/Hyperactivity Disorder (ADHD) and Autism Spectrum Disorder (ASD) frequently co-occur with overlapping traits. We investigated whether automated behavioral analysis during a clinician-child interview can identify distinct, objective features of the two conditions. Analyzing audio-video recordings of 2,529 youths (ages 5-22) in a broad community sample, multivariate models revealed that language difficulties often attributed to ADHD are primarily explained by age, cognitive ability, or co-occurring ASD. Increased motor activity specifically marked hyperactive-impulsive ADHD, but not ASD or inattentive ADHD. ASD was uniquely characterized by divergent narrative production and idiosyncratic responses, alongside a distinct vocal profile of higher pitch and dysphonia, despite structurally intact language. While these digital behavioral measures correlate with most diagnostic categories and age, the joint analysis effectively separates the effects of ASD from ADHD. These findings show that scalable digital assessment from recorded clinical interviews can disentangle overlapping ASD and ADHD diagnoses into domain-specific behavioral signatures.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义（研究动机和背景）
- **核心问题**：注意缺陷/多动障碍（ADHD）和自闭症谱系障碍（ASD）常共病存在，且表现重叠。传统诊断依赖主观评估（家长/教师报告、实验室任务），缺乏生态效度，难以大规模客观量化，且无法分离两种病症的独特行为标记。
- **整体含义**：研究旨在利用AI技术自动化分析临床访谈中的音视频数据，提取多模态行为特征（语言、言语韵律、运动），通过多变量模型分离ADHD和ASD的独特贡献，验证数字评估能否将重叠的诊断分解为域特异性行为特征，为客观、可扩展的诊断工具提供基础。

## 2. 方法论
- **核心思想**：对半结构化临床访谈（观看动画片后续提问）的音视频进行全自动AI处理，提取客观行为指标，然后使用多变量线性回归模型分离不同诊断（ASD、ADHD-IN、ADHD-HI）的独特效应，同时控制年龄、性别、智商等混淆因素。
- **关键技术细节**：
  - **转录与说话人分离**：使用WhisperX（large-v2）进行语音转文字；利用Google Gemini LLM基于上下文分离访谈者和儿童语音（优于传统声学方法，DER从16.35%降至3.16%）。
  - **语言特征**：使用Openwillis工具包提取词汇多样性、语速、连贯性等结构语言指标；使用Google Gecko文本嵌入模型计算回答语义与年龄匹配的典型发育儿童回答的余弦相似度，得到“答案典型性”分数。
  - **言语韵律特征**：提取基频、音量、声强二级（dysphonia）、气息声等声学指标。
  - **运动特征**：使用Google Mediapipe Holistic提取面部、头部、躯干关键点，计算帧间欧氏位移，取平均值。
  - **统计模型**：多元线性回归 `Metric ~ Age + IQ + Sex + ADHD_Inatt + ADHD_Hyper + ASD` ，使用双平方稳健拟合。效应量：连续变量用Cohen's f，二值变量用Cohen's d。
- **算法流程（文字说明）**：输入音频、视频 → WhisperX转录 → LLM说话人分离 → 提取结构化语言特征 → Gecko嵌入计算语义典型性 → 提取声学特征 → Mediapipe提取关键点及位移 → 针对每个行为指标拟合多元回归 → 输出各诊断的独特效应量。

## 3. 实验设计
- **数据集**：Healthy Brain Network (HBN) 社区样本，包含2529名5-22岁青少年，其中ADHD 1627人、ASD 306人（80%伴ADHD）、典型发育211人、其他诊断631人。所有被试观看动画短片《The Present》后接受标准化半结构化访谈（23个问题），同步录制高清视频和音频。
- **基准与对比方法**：
  - 无直接外部benchmark，主要内部对比：单变量相关 vs.多变量回归（揭示混淆因素）。
  - 敏感性分析：添加交互项（ASD×ADHD）；改用互斥分类组（ADHD-only、ASD-only、ADHD+ASD）；控制焦虑共病；限制年龄范围；控制临床语言能力（CELF）；排除非目标诊断等。
- **未与其他AI诊断系统或传统诊断工具进行直接对比**（如ADOS分类结果），但提供了与临床量表（SWAN、ASSQ）的相关性分析（图S5、S6）。

## 4. 资源与算力
- 论文**未明确说明**所使用的具体GPU型号、数量、训练时长或总计算资源。
- 仅提及：WhisperX和Mediapipe在本地安全机器上执行；LLM（Gemini）通过云端API调用；所有处理均在本地完成，未上传原始音视频到外部服务器。

## 5. 实验数量与充分性
- 共分析**三个领域**（语言、韵律、运动）的约**22个独立指标**（9个语言/韵律特征、5个语义域聚合指标、8个运动区域指标），每个指标均拟合单独的多变量回归模型。
- 进行了**多项敏感性分析**：交互项模型（未发现显著交互）、互斥分类组分析（支持加法模型）、排除其他诊断组、限制年龄至5-14岁、控制语言能力、控制焦虑等。
- **充分性评估**：实验覆盖广泛，控制多个混淆，且验证了主要结果的稳健性。但样本为**横截面**，不能验证纵向发展轨迹；ASD组以轻度至中度、高共病ADHD（80%）为主，限制外推。整体上，实验设计相当充分，但缺乏与金标准诊断（ADOS）的严格对比，亦未与其他AI诊断方法在同一数据集上对比，公平性中等。

## 6. 主要结论与发现
- **结构语言**：主要由年龄和IQ驱动，ADHD无独特负面效应（仅语速略快于非多动者）。先前认为ADHD相关的语言困难实为共病ASD或发育因素所致。
- **叙事与语义**：ASD独有叙事异常、答案典型性低、主题理解异于常人（如未理解男孩和小狗都有缺失肢体的相似性）。ADHD未见独立效应。
- **言语韵律**：ASD独有更高基频、更大基频变异、更高响度、明显更重的嘶哑（dysphonia）和气息声。ADHD-HI仅与基频变异和响度弱相关。
- **运动行为**：仅ADHD-HI（多动冲动型）与全面运动增加显著相关（头、躯干、面部）。ASD和ADHD-IN无此效应。年龄效应普遍存在（随龄减少）。
- **共病效应可加**：ASD和ADHD对行为的影响近似可加，未发现显著交互作用。

## 7. 优点
- **大规模生态样本**：2529人，真实临床访谈环境，提高生态效度。
- **多模态自动分析**：融合语言、言语韵律、运动行为三模态，全面刻画。
- **先进AI技术**：使用最先进的转录（WhisperX）、上下文感知说话人分离（LLM）、语义嵌入（Gecko）、计算机视觉（Mediapipe），并公开代码。
- **严格统计控制**：多变量模型明确分离年龄、IQ、性别、共病效应，避免过去单一变量分析中的混淆。
- **方法透明**：详细描述每个特征的提取方法和模型公式，可复现。
- **伦理合规**：所有处理在本地执行，保护参与者隐私。

## 8. 不足与局限
- **横截面设计**：无法验证纵向发展轨迹或变化机制。
- **样本局限**：ASD仅含言语、轻度至中度（Level 1），且80%伴ADHD，结论不能推广至重度、非言语或无ADHD共病的ASD人群。
- **运动分析粗粒度**：仅测量整体位移，未能识别特定重复/刻板运动（ASD核心症状之一），可能漏诊ASD运动特征。
- **缺乏金标准诊断验证**：未使用ADOS/ADI-R观察分数作为连续特征，仅依靠社区临床共识，可能引入标签噪声。
- **未与其他自动化工具对比**：未在同一数据集上比较不同AI诊断方法（如基于脑成像、眼动追踪等）的性能。
- **计算资源不透明**：未报告GPU型号、训练时间、成本，影响可复现性。
- **种族/文化偏差**：样本以白人居多（42.86%），可能影响语言模型的普适性。
- **语言处理局限**：未能捕捉对话中的实时互动、隐性韵律或复杂语用（如讽刺、幽默）。

（完）
