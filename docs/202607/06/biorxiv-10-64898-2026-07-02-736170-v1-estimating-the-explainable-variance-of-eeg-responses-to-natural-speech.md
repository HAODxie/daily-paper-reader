---
title: Estimating the Explainable Variance of EEG Responses to Natural Speech
title_zh: 估计脑电图对自然语音反应的可解释方差
authors: "Dou, J., Lalor, E."
date: 2026-07-03
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.02.736170v1.full.pdf"
tags: ["query:neuro-mental"]
score: 6.0
evidence: 脑电响应建模用于自然语言处理
tldr: 衡量脑电图对自然语音响应的模型好坏缺乏标准。本研究利用19名受试者听同一有声书的脑电图数据，通过跨主体线性模型估计总可解释方差。基于常用声学和语言特征的模型可预测大部分方差，但非全部，揭示现有特征集虽有效但仍有提升空间。
source: biorxiv
selection_source: fresh_fetch
motivation: 缺乏评估脑电图模型对自然语音响应解释力的基准，需量化可解释方差上限。
method: 用19名受试者听有声书的脑电图数据，以其他受试者降维后信号预测目标响应，外推估计总可解释方差。
result: 基于声学与语言特征的线性模型预测了大部分估计的总可解释方差，但未完全覆盖。
conclusion: 跨主体模型提供参考，表明现有特征集接近但未完全捕获所有可解释方差。
---

## 摘要
近年来，在理解人类大脑如何解析和处理自然语音方面取得了重大进展。这些进展大多基于建模大脑活动与语音的不同声学和语言学特征之间的关系。通过基于这些特征拟合和测试模型，可以检验关于大脑将语音声音转化为理解所使用的计算和表征类型的假设。尽管这项工作大部分集中在使用功能神经成像或颅内记录的电生理信号来建模BOLD活动，但该方法也被证明对MEG和EEG有用。事实上，无创EEG在转化研究和应用方面对研究语音处理具有某些优势。过去十多年的研究表明，基于众多声学、语言和副语言语音特征可以成功地对EEG进行建模。然而，一个重要的未解问题悬而未决：即什么才是EEG对自然语音反应的良好模型？或者换句话说，在自然语音聆听过程中记录的EEG中有多少方差可以解释为源自该语音输入？本研究旨在解决这个问题。我们假设一个人对自然语音的EEG反应的最佳模型是其他人在听同一段语音时的EEG反应集合。基于这一假设，我们使用19名健康成年英语母语者的EEG构建了跨被试模型，他们都听了同一本有声书。每个被试的模型涉及使用来自不同数量其他被试的（降维）EEG数据来预测该被试的EEG数据，然后外推以估计目标个体对语音反应的总可解释方差。接着，我们表明，基于几个常用声学和语言语音特征的线性模型（时间响应函数）可以预测大部分（但并非全部）估计的总可解释方差在跨被试的EEG反应中。

## Abstract
Substantial progress has been made in recent years on understanding how the human brain parses and processes natural speech. Much of this progress has been based on modeling how brain activity relates to the different acoustic and linguistic features of speech. By fitting and testing models based on those features, one can test hypotheses about the kinds of computations and representations the brain uses to convert speech sounds into understanding. While much of this work has focused on modeling BOLD activity using functional neuroimaging or intracranially recorded electrophysiological signals, the approach has also proven useful with MEG and EEG. Indeed, noninvasive EEG has certain advantages for studying speech processing in terms of translational research and application. Research over the last decade or so has shown that EEG can be successfully modeled based on numerous acoustic, linguistic, and paralinguistic speech features. However, an important unanswered question hangs over all of this work: namely, what constitutes a good model of EEG responses to natural speech? Or, to put it another way, how much variance in EEG recorded during natural speech listening is explainable as having derived from that speech input? The present study aims to tackle this issue. We do so under the assumption that the best model for a person's EEG response to natural speech is a set of EEG responses from other people listening to the same speech. Using this assumption, we construct inter-subject models using EEG from 19 healthy adult native speakers of English who all listened to the same audiobook. The model for each subject involves predicting their EEG data using (dimensionality-reduced) EEG from different numbers of other subjects and then extrapolating to estimate the total explainable variance in the target individual's response to speech. Following this, we show that linear models (temporal response functions) based on several commonly used acoustic and linguistic speech features can predict most - but importantly not all - of the estimated total explainable variance in EEG responses across subjects.