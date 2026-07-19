---
title: "Thematic Shifts in Early-High-Impact Cancer Genomics and Diagnostics Research: A Bibliometric and Semantic Analysis"
title_zh: 早期高影响力癌症基因组学与诊断研究的主题转变：文献计量学与语义分析
authors: "Su, Z., Li, T."
date: 2026-07-18
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.04.736459v2.full.pdf"
tags: ["query:neuro-mental"]
score: 7.0
evidence: 大语言模型用于主题过滤
tldr: 癌症基因组学与诊断学领域发展迅速。本研究利用基于OpenAlex引文数据和大型语言模型（LLM）的文献计量框架，分析了两个连续年度队列中高影响力论文的主题变化。结果显示，最受引用的论文是大型基因组基础设施资源，而非单疾病机制研究。主题层面，克隆进化、单细胞和空间组学技术、空间转录组学、免疫细胞浸润、拷贝数变异等频率显著上升，而液体活检和ctDNA相关主题出现最大幅度下降。这表明早期引用影响力正转向整合性、空间分辨和异质性感知的研究，LLM增强的引文排序为精准肿瘤学主题演化提供了可复现视角。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-04-736459-v2/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1180, \"height\": 1105, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-04-736459-v2/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1240, \"height\": 1245, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-04-736459-v2/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1245, \"height\": 611, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-04-736459-v2/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1253, \"height\": 758, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-04-736459-v2/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1248, \"height\": 615, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-04-736459-v2/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1251, \"height\": 759, \"label\": \"Figure\"}]"
motivation: 识别癌症基因组学领域早期高引主题，以指导实验室投入和临床转化。
method: "利用精确阈值扩展算法对10,000余篇论文按18个月引用排名，结合LLM主题过滤和概念提取，对比两个年度队列的规范化主题频率。"
result: 高引论文以大型基因组资源为主；主题变化中克隆进化、单细胞/空间组学上升，液体活检下降显著。
conclusion: 早期引用影响力正转向整合、空间分辨和异质性感知研究，LLM方法可有效监测主题演变。
---

## 摘要
癌症基因组学与诊断是一个快速发展的领域，识别哪些主题能获得早期引用凸显性，可为实验室投资、临床转化和研究策略提供信息。我们开发了一个文献计量框架，用于识别和表征连续两个年度队列中该领域最具影响力的近期出版物。通过使用数学精确的阈值扩展算法，我们根据发表后18个月的引用计数，对每个队列中超过10,000篇OpenAlex索引的研究文章进行排序。基于大语言模型（LLM）的主题相关性过滤，每个队列产生了50篇实质性的主题相关论文（共100篇）。基于LLM的概念提取和两阶段、嵌入引导的标准化流程产生了1,090个规范概念，组织成77个父主题，从而实现了跨队列论文级概念流行度的结构化比较。两个队列中被引最多的论文是大规模基因组基础设施资源，而非单一疾病的机制研究。在连续队列之间，克隆进化与肿瘤内异质性、单细胞与空间组学技术、空间转录组学、免疫细胞浸润和拷贝数变异的标准化频率增加最多，而液体活检和ctDNA相关主题的下降最大。这些发现表明，癌症基因组学中的早期引用影响力正在转向整合性、空间分辨和异质性感知的研究，并证明LLM增强的引用排名为监测精准肿瘤学的主题演变提供了可复制、语义丰富的视角。用于探索结果的可视化界面位于https://pri.pepkio.com/。

## Abstract
Cancer genomics and diagnostics is a rapidly evolving field in which identifying which topics attract early citation prominence can inform laboratory investment, clinical translation, and research strategy. We developed a bibliometric framework to identify and characterize the most influential recent publications in this domain across two consecutive annual cohorts. Using a mathematically exact threshold-expansion algorithm, we ranked over 10,000 OpenAlex-indexed research articles per cohort by 18-month post-publication citation count. Large language model (LLM)-based topical relevance filtering yielded 50 substantively on-topic papers per cohort (100 total). LLM-based concept extraction and a two-stage, embedding-guided normalization pipeline produced 1,090 canonical concepts organized into 77 parent themes, enabling structured cross-cohort comparison of paper-level concept prevalence. The most cited papers in both cohorts were large-scale genomic infrastructure resources rather than single-disease mechanistic studies. Between consecutive cohorts, normalized frequencies increased most for clonal evolution and intratumoral heterogeneity, single-cell and spatial omics technologies, spatial transcriptomics, immune cell infiltration, and copy number variation, while liquid biopsy and ctDNA-related themes showed the largest declines. These findings indicate that early citation impact in cancer genomics is shifting toward integrative, spatially resolved, and heterogeneity-aware research, and demonstrate that LLM-augmented citation ranking provides a replicable, semantically enriched lens for monitoring thematic evolution in precision oncology. A web interface for exploring the results is available at https://pri.pepkio.com/.