---
title: Preventing Data Leakage in Neural Decoding
title_zh: 防止神经解码中的数据泄露
authors: "Wong, R., McCullough, M. H., Lu, T., Zhu, S. I., Goodhill, G. J."
date: 2026-06-29
pdf: "https://www.biorxiv.org/content/10.64898/2026.01.26.701583v2.full.pdf"
tags: ["query:neuro-mental"]
score: 6.0
evidence: 解决神经解码中的数据泄漏问题，对神经科学中的深度学习至关重要
tldr: 神经解码中数据泄露常因预处理（如降维）和随机k折交叉验证引入，导致性能估计偏离真实值。研究发现泄露有时反而降低性能，且自相关时间序列中交叉验证会高估性能。通过理论分析揭示机制，并提出具体建议，有助于获得可靠的生物学结论。
source: biorxiv
selection_source: fresh_fetch
motivation: 避免常见预处理步骤无意中导致数据泄露，从而产生有偏的解码性能估计和无效的生物学结论。
method: 理论分析并实验验证降维等预处理及自相关时间序列交叉验证中的泄露现象及其对性能的影响。
result: 泄露可降低或高估解码性能，特别是在自相关时间序列中随机交叉验证会夸大结果。
conclusion: 提供了避免数据泄露的详细建议，确保神经解码研究的可靠性。
---

## 摘要
神经解码是一种广泛使用的机器学习技术，用于研究行为、感知和认知如何在神经活动中表征。然而，若不谨慎应用，可能会发生数据泄露，即测试集的信息污染训练集，导致对解码性能的估计产生偏差，并可能使生物学结论失效。在此，我们展示了在神经解码研究中，常见的监督和无监督预处理步骤（包括降维）可能会引入数据泄露。我们揭示，在某些情况下，与无偏估计相比，数据泄露反而会降低解码性能，并提供了理论分析解释其发生机制。我们还表明，对于自相关的神经时间序列，随机k折交叉验证可能会大幅高估解码性能。基于这些发现，我们提供了避免神经解码中数据泄露的详细建议。

## Abstract
Neural decoding is a widely-used machine learning technique for investigating how behavior, perception and cognition are represented in neural activity. However without careful application data leakage can occur, where information from the test set contaminates the training set, leading to biased estimates of decoding performance and potentially invalidating biological conclusions. Here we show that leakage can be introduced in neural decoding studies by common supervised and unsupervised preprocessing steps, including dimensionality reduction. We reveal that in some cases leakage can paradoxically decrease decoding performance relative to unbiased estimates, and we provide theoretical analyses explaining how this occurs. We also show that, for autocorrelated neural time series, randomized k-fold cross-validation can dramatically overstate decoding performance. Based on these findings, we provide detailed recommendations for avoiding data leakage in neural decoding.