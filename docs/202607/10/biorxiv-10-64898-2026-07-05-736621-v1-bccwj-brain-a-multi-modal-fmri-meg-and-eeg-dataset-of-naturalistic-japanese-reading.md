---
title: "BCCWJ-Brain: A Multi-Modal fMRI, MEG, and EEG Dataset of Naturalistic Japanese Reading"
title_zh: BCCWJ-Brain：自然日语阅读的多模态fMRI、MEG和EEG数据集
authors: "Sugimoto, Y., Asahara, M., Jeong, H., Kanno, A., Koizumi, M., Oseki, Y."
date: 2026-07-09
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.05.736621v1.full.pdf"
tags: ["query:neuro-mental"]
score: 8.0
evidence: 为大型语言模型提供多模态神经影像基准数据集
tldr: 自然阅读的神经机制研究需要多模态神经影像数据，但现有资源有限。BCCWJ-Brain数据集包含fMRI、MEG和EEG三种模态，记录了112名日语母语者阅读报纸文章时的脑活动，采用快速序列视觉呈现范式。该数据集提供了同一自然刺激下的互补神经数据，可作为大型语言模型等计算模型的认知基准，并已在OpenNeuro平台公开。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1818, \"height\": 1312, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1643, \"height\": 360, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1606, \"height\": 539, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1575, \"height\": 833, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1575, \"height\": 834, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1632, \"height\": 1332, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1635, \"height\": 229, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1614, \"height\": 1753, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1639, \"height\": 249, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-05-736621-v1/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1630, \"height\": 346, \"label\": \"Table\"}]"
motivation: 构建多模态、自然刺激的神经影像数据集，以支持阅读的认知神经科学研究和计算模型评估。
method: 采集112名被试（36人fMRI、35人MEG、41人EEG）在快速序列视觉呈现下阅读20篇日语报纸文章时的脑活动数据。
result: 成功获取三种模态的神经数据，数据质量良好，可用于分析自然阅读过程中的大脑动态。
conclusion: 该数据集为自然语言处理和神经科学提供了宝贵的多模态资源，有助于理解自然阅读的神经机制。
---

## 摘要
我们推出了BCCWJ-Brain数据集，这是一个多模态神经影像资源，包含功能性磁共振成像（fMRI）、脑磁图（MEG）和脑电图（EEG）数据，数据来自母语为日语的被试阅读《现代日本书面语平衡语料库》（BCCWJ）中的报纸文章。神经数据采集自112名被试（36名fMRI、35名MEG和41名EEG），他们以快速序列视觉呈现（RSVP）范式阅读了二十篇报纸文章。通过在相同的自然阅读刺激下提供三种互补的神经影像模态，该数据集为大型语言模型等计算模型提供了认知基准。该数据集在OpenNeuro平台上公开可用，为神经科学、自然语言处理及相关研究领域提供了宝贵资源。

## Abstract
We present the BCCWJ-Brain dataset, a multi-modal neuroimaging resource comprising functional magnetic resonance imaging (fMRI), magnetoencephalography (MEG), and electroencephalography (EEG) data recorded from native Japanese speakers reading newspaper articles from the Balanced Corpus of Contemporary Written Japanese (BCCWJ). Neural data were collected from 112 participants (36 fMRI, 35 MEG, and 41 EEG) as they read twenty newspaper articles presented in a Rapid Serial Visual Presentation (RSVP) paradigm. By providing three complementary neuroimaging modalities collected under identical naturalistic reading stimuli, this dataset provides a cognitive benchmark for computational models such as large language models. The dataset is publicly available on the OpenNeuro platform, offering a valuable resource for neuroscience, natural language processing, and related research fields.