---
title: Unsupervised Representation Learning Reveals Individualized Neurophysiological Profiles
title_zh: 无监督表示学习揭示个体化神经生理特征
authors: "Lapatrie, M., da Silva Castanheira, J., Aydin, I., Baillet, S."
date: 2026-06-26
pdf: "https://www.biorxiv.org/content/10.64898/2026.02.10.705127v2.full.pdf"
tags: ["query:neuro-mental"]
score: 7.0
evidence: 使用无监督表示学习从脑磁图数据提取个性化神经生理特征
tldr: "个体脑活动存在稳定神经特征，但监督方法难以区分生物学因素与任务策略。本文提出与被试无关的自编码器，仅用重建目标从短时静息态MEG中学习潜在表征，无需标签即可区分个体。同次记录120秒准确率93.3%，最低14秒仍有效；跨次泛化49.5%高于随机，年龄预测r²=0.318。该方法为可解释的神经特征建模提供了新范式。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有神经特征提取依赖标签或有监督目标，难以区分稳定生物学信号与任务相关策略。
method: 采用与被试无关的自编码器，仅以重建为训练目标，从短时静息态MEG片段中学习潜在空间表征。
result: "同次记录120秒区分准确率93.3%，短至14秒有效；跨次准确率49.5%；年龄预测r²=0.318。"
conclusion: 无监督表示学习可生成可解释的个体神经特征，实现可扩展且无需标签的神经画像方法。
---

## 摘要
人类大脑活动包含稳定且个体特有的特征，这些特征可持续数月到数年，形成神经生理特征。大多数基于模型的特征化方法使用参与者标签或有监督目标，这使得难以确定成功的区分是反映了稳定的生物学特性还是可被利用的特异性。我们引入了一种参与者无关的自编码器框架，该框架以重建作为唯一训练目标，从短暂的静息态脑磁图（MEG）片段中提取特征。在没有参与者标签的情况下，从学习到的潜在空间中产生了具有区分力的特征。在会话内，自编码器特征在120秒时达到93.3%的准确率，当源重建中隐藏了参与者特定解剖结构时，即使仅使用14秒的记录，也超过了功能连接、频谱和对比基线。不同记录会话间的区分高于随机水平（预训练自编码器的会话间准确率为49.5%）。这些特征在预测年龄方面也比基线更准确（r²=0.318），并且解码器能够在频谱和连接空间中进行基于扰动的敏感性分析。这确立了参与者无关的表示学习作为一种可扩展且可解释的特征化方法。

## Abstract
Human brain activity contains stable, individual-specific features that persist over months to years, forming neurophysiological profiles. Most model-based profiling approaches use participant labels or supervised objectives, making it difficult to determine whether successful differentiation reflects stable biology or exploitable idiosyncrasies. We introduce a participant-agnostic autoencoder framework that derives profiles from brief resting-state magnetoencephalography (MEG) segments using reconstruction as sole training objective. Discriminative profiles emerged from the learned latent space without participant labels. Within-session, autoencoder profiles reached 93.3% accuracy at 120 s, exceeding functional-connectivity, spectral, and contrastive baselines with recordings as short as 14 s when participant-specific anatomy was withheld from source reconstruction. Differentiation generalized above chance across recording sessions (between-session accuracy 49.5% for the pretrained autoencoder). Profiles also predicted age more accurately than baselines (r2=0.318), and the decoder enabled perturbation-based sensitivity analyses in spectral and connectivity spaces. This establishes participant-agnostic representation learning as a scalable and interpretable profiling.