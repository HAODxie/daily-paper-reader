---
title: Machine learning on magnetoencephalography data yields generalizable low-dimensional neural fingerprints that distinguish individuals across task conditions
title_zh: 基于脑磁图数据的机器学习产生可泛化的低维神经指纹，能够在任务条件下区分个体
authors: "Karhula, J., Ojanperä, A., Yılmaz, E., Merz, S., Kaski, S., Salmelin, R."
date: 2026-07-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.26.734424v1.full.pdf"
tags: ["query:neuro-mental"]
score: 6.0
evidence: 基于MEG数据的机器学习低维神经指纹
tldr: 个体大脑功能差异可由神经指纹捕获，但全连接组高维性增加计算负担。本研究采用lnBRRR从MEG数据中学习低维潜在空间，在N=30-35时达到最优测试精度，且任务与静息态指纹性能相当并跨条件泛化。结果展示了lnBRRR作为神经数据分析工具的潜力，表明个体差异在功率谱中本质稳定。
source: biorxiv
selection_source: fresh_fetch
motivation: 全连接组高维性限制机器学习应用，需低维替代保留个体特征。
method: 使用lnBRRR从MEG功能连接和功率谱密度中学习低维潜在空间。
result: N=30-35达最优性能，任务指纹与静息态相当，且跨任务条件泛化。
conclusion: lnBRRR有效提取稳定神经指纹，个体差异不受任务影响。
---

## 摘要
个体大脑在结构和功能上具有独特性。功能差异由神经指纹捕捉，这些指纹反映了行为和认知的个体差异以及与神经退行性疾病相关的群体水平变化。迄今为止，大多数研究聚焦于包含全功能连接组的指纹。然而，连接组的高维度可能增加计算负担并阻碍机器学习方法在潜在应用中的性能。因此，一种能够保留全连接组个体特征的低维替代方案将是有益的。本研究采用潜噪声贝叶斯降秩回归（lnBRRR）来学习低维潜在空间，以捕捉源自MEG记录的功能连接和功率谱密度数据中的个体特征。通过较小的训练集规模（N=20-44）以及主成分分析和线性判别分析作为对比，评估了lnBRRR的性能。还使用任务数据评估了模型性能，并通过余弦相似度比较了不同任务条件下的解，以确定个体特征是否因不同认知过程而改变。LnBRRR在N=20时已能捕捉到可泛化的个体模式，但需要N=30-35才能达到最佳测试准确率并防止过拟合。该模型与替代模型相比取得了可比的性能。从任务数据中得出的潜在指纹与静息态潜在指纹性能相当，并且lnBRRR的解被证明可以跨条件泛化。此外，发现功率谱密度数据的模型解在不同任务条件下高度相似，但旋转方向不同，这表明无论任务条件如何，模型都能捕捉到相似的个体特征模式。总体而言，当前结果突显了lnBRRR作为神经影像数据分析潜在工具的潜力，并表明功率谱密度中的个体差异在很大程度上是内在的，不受不同认知过程的影响。

## Abstract
Individual brains are unique in structure and function. Functional differences are captured by neural fingerprints, which reflect individual differences in behavior and cognition as well as group-level changes related to neurodegenerative diseases. Most research efforts so far have focused on fingerprints com-prising full functional connectomes. However, the high dimensionality of the connectomes can increase computational load and impede performance of machine learning methods in potential applications. A low-dimensional alternative that retains individual features of the full connectomes would thus be beneficial. The present study employed latent-noise Bayesian Reduced Rank Regression (lnBRRR) to learn low-dimensional latent spaces that capture individual features in functional connectivity and power spectral density data derived from MEG recordings. LnBRRR performance was assessed with low training set sizes (N=20-44), and against principal component analysis and linear discriminant analysis. Model performance was also assessed with task data, and the solutions were compared across task conditions with cosine similarity to establish whether individual features are altered by different cognitive processes. LnBRRR captured generalizable individual patterns already at N=20 but N=30-35 was needed to reach optimal test accuracies and to prevent potential overfitting. The model also achieved comparable performance to the alternative models. Latent fingerprints derived from task data attained comparable performance to resting-state latent fingerprints, and lnBRRR solutions were shown to generalize across conditions. Additionally, the model solutions for power spectral density data were discovered to be notably similar, yet differently rotated, over task conditions, suggesting that similar patterns of individual features were captured by the model regardless of the task condition. Altogether, the present results highlight lnBRRR as a potential tool for neuroimaging data analysis and demonstrate that individual differences in power spectral density are largely intrinsic and unaffected by varying cognitive processes.