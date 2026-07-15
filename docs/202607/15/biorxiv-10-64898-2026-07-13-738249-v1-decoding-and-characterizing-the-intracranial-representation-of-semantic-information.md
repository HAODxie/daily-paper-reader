---
title: Decoding and Characterizing the Intracranial Representation of Semantic Information
title_zh: 解码与表征语义信息的颅内表示
authors: "Smith, C., Inchyna, S., Barrentine, B., Nelson, M. J."
date: 2026-07-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.13.738249v1.full.pdf"
tags: ["query:neuro-mental"]
score: 8.0
evidence: 从颅内EEG解码语义信息用于脑机接口
tldr: "脑机接口（BCI）在解码运动和发音信号方面表现优异，但能否从人类皮层活动中解码高层语义信息尚不清楚。本研究使用立体脑电图（sEEG）记录癫痫患者执行语义任务时的神经活动，提取高伽马功率作为特征进行机器学习分类。结果表明，15个语义类别的平均分类准确率达29.8%（随机6.7%），证明单次试验即可提取概念类别信息。该工作为发展基于概念信息的语言BCI提供了新方向，并深化了对语言网络分布式表征的理解。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738249-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1235, \"height\": 1127, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738249-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1027, \"height\": 1011, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738249-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1139, \"height\": 1114, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-13-738249-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1534, \"height\": 1586, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-13-738249-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1336, \"height\": 1100, \"label\": \"Table\"}]"
motivation: 探索从人类皮层活动中解码语义信息的可能性，以推动基于概念而非纯发音信号的BCI发展。
method: 使用sEEG记录患者语义任务时的神经活动，提取高伽马功率特征，通过监督学习分类评估语义解码性能。
result: "15个语义类别的平均分类准确率达29.8%，显著高于随机水平（6.7%），单次试验可解码语义类别。"
conclusion: 高伽马活动编码可提取的语义类别信息，语义解码可作为未来语言BCI的补充方向，并促进对概念知识的神经表征理解。
---

## 摘要
脑机接口通过解码与语音产生相关的运动和发音信号取得了显著性能。然而，关于更高级别的语义表征能否从人类皮层活动中解码，我们所知甚少。展示语义解码将推进我们对语言组织的理解，以及依赖概念而非纯粹发音信息的脑机接口的发展。我们记录了因临床癫痫监测而接受立体脑电图（sEEG）的患者在完成需要语义处理的语言任务时的颅内神经活动。从局部场电位中提取高伽马功率，并用于生成试验级特征以进行监督机器学习分类。通过交叉验证评估分类性能。语义类别信息的解码显著高于随机水平，15个语义类别的平均分类准确率达到29.8%（随机水平为6.7%）。这些发现表明，高伽马活动包含关于概念类别成员的信息，可以在单个试验中提取。这些结果提供了证据，表明语义信息可以从颅内群体记录中获取，并支持语义解码作为未来语言脑机接口的补充方向的可行性。除了神经假体应用外，这项工作有助于理解概念知识如何在分布式人类语言网络中表征。

## Abstract
Brain-computer interfaces (BCIs) have achieved impressive performance by decoding motor and articulatory signals associated with speech production. However, considerably less is known about whether higher-level semantic representations can be decoded from human cortical activity. Demonstrating semantic decoding would advance both our understanding of language organization and the development of BCIs that rely on conceptual rather than purely articulatory information. We recorded intracranial neural activity from patients undergoing stereotactic electroencephalography (sEEG) for clinical epilepsy monitoring while they performed language tasks requiring semantic processing. High-gamma power was extracted from local field potentials and used to generate trial-level features for supervised machine-learning classification. Classification performance was evaluated using cross-validation. Semantic category information was decoded significantly above chance, with mean classification accuracy reaching 29.8% across 15 semantic categories (chance = 6.7%). These findings demonstrate that high-gamma activity contains information about conceptual category membership that can be extracted on individual trials. These results provide evidence that semantic information is accessible from intracranial population recordings and support the feasibility of semantic decoding as a complementary direction for future language BCIs. Beyond neuroprosthetic applications, this work contributes to understanding how conceptual knowledge is represented in the distributed human language network.