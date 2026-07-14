---
title: Tokenizing single-cell transcriptomes as a native language for large language models
title_zh: 将单细胞转录组标记为大型语言模型的母语
authors: "Xiao, C., Ding, Y., Bian, H., Chen, Y., Wei, L., Zhang, X."
date: 2026-07-11
pdf: "https://www.biorxiv.org/content/10.1101/2025.10.22.684047v2.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 使用大语言模型通过标记化处理单细胞转录组
tldr: 大语言模型(LLM)主要处理离散文本，难以直接处理连续高维的单细胞转录组数据。本文提出CellTok方法，将单细胞转录组转化为紧凑的细胞token序列，并融入预训练LLM词表，使LLM能像处理自然语言一样处理细胞数据。实验表明，该模型能识别单个细胞、解释细胞群体、推断疾病相关状态、预测细胞通讯、模拟发育轨迹和生成细胞状态。通过上下文提示可进一步提升性能，表明CellTok有效桥接了分子模态与语言模型，为细胞与生物知识的统一建模提供了新范式。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-22-684047-v2/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1509, \"height\": 1404, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-22-684047-v2/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1503, \"height\": 891, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-22-684047-v2/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1500, \"height\": 717, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-22-684047-v2/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1174, \"height\": 730, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2025-10-22-684047-v2/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1499, \"height\": 565, \"label\": \"Figure\"}]"
motivation: 单细胞转录组是连续高维分子谱，难以被现有LLM作为离散语言单元处理，需要新方法将其转化为LLM可理解的模态。
method: 提出CellTok，通过量化编码将转录组转换为紧凑的细胞token序列，并作为新词嵌入到预训练LLM词汇表中。
result: LLM能完成细胞识别、群体解释、疾病状态推断、细胞通讯预测、发育轨迹模拟及状态生成，且生物上下文提示可提升性能。
conclusion: 单细胞转录组可转化为LLM的原生语言，建立细胞、群体和生物知识在共享token空间中的统一接口。
---

## 摘要
大型语言模型（LLMs）能够处理表示为共享序列空间中的标记的各种形式的信息。然而，单细胞转录组对于LLMs而言仍然是一种陌生的模态，因为它们是连续的高维分子谱，而非离散的语言单元。在此，我们提出CellTok，一种标记化的单细胞语言建模方法，它将转录组谱转换为紧凑的细胞标记序列，并将其纳入预训练LLM的词汇表中。通过将细胞表示为原生标记，CellTok使得细胞测量、文本指令、生物学背景以及多细胞群体能够在同一自回归建模框架内被联合处理。在多项任务中，CellTok使LLMs能够识别单个细胞、解释同质和异质细胞群体、推断疾病相关的细胞状态、预测细胞间通讯、模拟发育轨迹以及生成细胞状态。此外，基于提示的实验表明，提供适当的生物学背景可以提高性能，表明CellTok能够利用LLM的知识和上下文推理来支持细胞数据解释。这些结果表明，单细胞转录组可以从一种陌生的分子模态转变为LLMs的母语，从而在共享的标记空间中建立统一接口，用于建模细胞、群体和生物学知识。

## Abstract
Large language models (LLMs) can process diverse forms of information once they are represented as tokens in a shared sequence space. However, single-cell transcriptomes remain a foreign modality to LLMs because they are continuous, high-dimensional molecular profiles rather than discrete linguistic units. Here, we propose CellTok, a tokenized single-cell language modeling approach that converts transcriptomic profiles into compact cellular token sequences and incorporates them into the vocabulary of a pretrained LLM. By representing cells as native tokens, CellTok enables cellular measurements, textual instructions, biological context, and multi-cell populations to be jointly processed within the same autoregressive modeling framework. Across diverse tasks, CellTok enable LLMs to recognize individual cells, interpret homogeneous and heterogeneous cell populations, infer disease-associated cellular states, predict cell-cell communication, model developmental trajectories, and generate cellular states. Moreover, prompt-based experiments show that providing appropriate biological context improves performance, indicating that CellTok can leverage LLM knowledge and contextual reasoning to support cellular data interpretation. These results demonstrate that single-cell transcriptomes can be transformed from a foreign molecular modality into a native language for LLMs, establishing a unified interface for modeling cells, populations, and biological knowledge in a shared token space.

---

## 论文详细总结（自动生成）

# 详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：单细胞转录组数据是连续、高维的分子谱，而大型语言模型（LLM）本质处理离散的文本标记（token）。这种模态上的根本差异使得LLM无法直接“阅读”或“编写”细胞状态，细胞生物学数据与语言学知识之间缺乏统一的接口。
- **整体含义**：尽管已有大型细胞模型（LCM）能编码细胞状态，但它们仍然是细胞自身的表示，无法与文本指令、群体上下文或生物学知识在同一空间内联合建模。论文提出将单细胞转录组转化为LLM可消费的“细胞token”，使LLM能像处理母语一样处理细胞数据，从而建立细胞、群体和生物知识的统一序列建模框架。

## 2. 论文提出的方法论

- **核心思想**：通过向量量化自编码器（VQ-VAE）将每个细胞的基因表达谱压缩为一段离散的token序列，然后将这些token作为新词加入预训练LLM（Qwen 2.5 7B）的词表中。采用**早期融合**设计，使细胞token与文本token在同一自回归框架中共同建模，既可以作为输入、上下文，也可以作为预测输出。
- **关键技术细节**：
  - **细胞分词器**：编码器将对数归一化的表达量（5,000个高变基因）映射到连续潜在空间，然后分割为32个片段，每个片段用欧氏距离匹配最近的码本向量（共256个码本，每个维度8）。量化后的表示经解码器重建为表达谱。
  - **与LLM整合**：码本向量作为新token加入LLM词表，使用LoRA（低秩适配）微调LLM的注意力层、前馈层、嵌入层和输出投影层，仅更新约2%的参数。
  - **双预训练任务**：①**细胞理解任务**——输入细胞token，生成文本描述；②**细胞生成任务**——输入文本描述，生成细胞token，再经解码器产生表达谱。两者联合优化，实现细胞与语言的相互翻译。
  - **训练数据**：68百万高质量单细胞谱（来自CELLxGENE，覆盖285种组织、660种细胞类型），文本描述由GPT-4o生成。预训练时混合1:1的通用文本以保持语言能力。

## 3. 实验设计

- **数据集与场景**：
  - **个体细胞注释**：三个留出数据集（小肠、脑、外周血），对比LCM（Geneformer, scGPT, scFoundation）、LLM方法（CellWhisperer, Cell2Sentence）以及大型通用LLM（GPT-4o, GPT-o1, DeepSeek-R1等）在零样本/微调下的表现。
  - **个体细胞生成**：相同留出数据集，对比Cell2Sentence和scDiffusion。
  - **群体注释**：肺数据集（健康与COVID-19供者）。①**同质群体**：Leiden聚类后每个群体单一细胞类型，大小10-100细胞；②**异质群体**：混合两种细胞类型（如CD4+与CD8+ T细胞），需直接解析。对比方法：scGPT, scFoundation, Geneformer, Cell2Sentence, CellWhisperer（零样本）。
  - **疾病状态推断**：肺数据集，健康 vs COVID-19，不提供细胞类型标签，只给出群体中每个细胞的状态（正常/COVID-19）。做了语义中性化消融（用“状态A”“状态B”代替正常/COVID-19）。
  - **细胞通讯预测**：
    - **非空间**：肺数据集中供者间推断配体-受体通路，使用CellChat生成监督信号。对比随机基线、仅基于细胞类型标签的多选基线，并做通路名称语义消融（“通路1”等）。
    - **空间**：人结直肠癌Visium HD数据（CellNEST流程），区分通讯与不通讯的相邻细胞对。仅用转录组输入，无坐标。对比基于细胞类型对频率的随机猜测基线。还做了仅异质对的训练。
  - **发育轨迹推理**：脑类器官数据集（iPSC/ESC来源，4天至2个月）。设**大跨度**（d4,12,21,31,61）和**小跨度**（d4,7,11,12,16）。评价准确率、Kendall τ、Spearman ρ。做OOD（未见天替代部分观察天）。
  - **轨迹条件生成**：同一脑类器官数据集，设四种生成模式（局部插值、密集插值、中程插值、外推），共19个任务。评价生成细胞与真实细胞在目标天的相似性，并做OOD目标天实验。
- **基准方法**：包括scGPT、Geneformer、scFoundation、Cell2Sentence、CellWhisperer、通用LLM（GPT-4o等）以及专门生成模型scDiffusion。
- **消融实验**：语义中性标签（疾病状态、通路名称）、多任务联合训练（CellTok-mix）、LLM骨干规模比较（Qwen 0.5B/3B, LLaMA 3 8B）、码本参数消融（片段数、码本大小等）。

## 4. 资源与算力

- 论文**未明确说明**训练CellTok-base或各下游任务所使用的GPU型号、数量、训练时长、总计算量等具体信息。仅提及使用了Qwen 2.5 7B作为主干，LoRA微调约2%的参数，以及预训练数据量为68M单细胞谱。关于训练成本和硬件信息缺失。

## 5. 实验数量与充分性

- **实验数量丰富**：涵盖7大类任务（个体注释、个体生成、群体注释、疾病状态、细胞通讯、轨迹推理、轨迹生成），每类内部有多种设置（不同数据集、不同群体大小、不同跨度等）。还包括多个消融实验（语义中性、多任务联合、骨干尺度、码本参数）。
- **充分性评估**：
  - 在个体细胞注释和生成上对比了几乎所有主流方法，且结果具有竞争力。
  - 群体任务中设计了同质/异质、有/无细胞类型标签、有/无语义标签等对比，控制变量全面。
  - 通讯任务同时考虑了非空间和空间两种形式，且做了语义消融和配对频率基线。
  - 轨迹推理和生成设置了OOD泛化测试。
  - 整体上实验设计较充分、逻辑清晰，对比公平（微调设置统一，零样本方法另行说明）。
  - 但某些任务（如空间通讯）仅使用一个数据集，且监督信号来源于计算工具（CellChat, CellNEST），可能引入偏差。此外，未测试跨组织或跨物种的泛化能力。

## 6. 论文的主要结论与发现

- 单细胞转录组可以通过**离散化+早期融合**转化为LLM的原生token，实现细胞数据的“读取、推理、生成”一体化。
- CellTok在个体水平上达到或超过了现有专门模型（如scGPT, scFoundation）及通用LLM的性能，尤其在异质群体直接注释和疾病状态推断中显著超越所有基线。
- **语义信息的重要性**：用中性标签替代生物学标签后性能下降，表明CellTok能利用语言级的生物学知识辅助细胞分析。
- 细胞token支持联合建模多细胞上下文，使LLM能直接预测群体属性、通讯事件和时序关系，而无需逐细胞聚合。
- **多任务联合训练**（CellTok-mix）在部分任务上可带来正面迁移（如疾病状态识别），说明统一的token接口可促进知识共享。
- 轨迹生成可泛化到未见的目标时间点，表明模型学到了连续的发育相关的转录变化。

## 7. 优点

- **新颖性**：首次将单细胞转录组表示为LLM可原生消费的离散token，并实现双向翻译与共建模，填补了模态鸿沟。
- **统一接口**：早期融合设计使细胞token与文本token在同一个自回归框架内互动，可自然支持多种任务（分类、生成、关系预测、时序推理），无需任务特定架构。
- **可解释性**：语义消融实验揭示了标签知识对性能的贡献，体现了语言模型先验知识的利用，比纯数字嵌入更透明。
- **高效性**：LoRA微调仅更新2%参数，适合资源受限场景。
- **鲁棒性**：跨不同LLM骨干（Qwen, LLaMA）和规模均表现缩放一致性。
- **实验设计周密**：包含多种控制变量、OOD泛化测试和公平对比，结果可信度高。

## 8. 不足与局限

- **信息损失**：离散化可能压缩或丢弃连续表达中的精细定量信息，特定标记基因的表达差异可能被量化噪声遮蔽。论文未详细评估保留了多少定量信息。
- **训练与推理成本未报告**：未说明GPU资源、训练时间等，不利于复现和成本评估。
- **数据集与任务覆盖有限**：疾病状态和通讯任务仅基于一个肺数据集，空间通讯仅一个CRC Visium HD样本；轨迹数据仅来自脑类器官，可能缺乏跨组织/跨物种泛化验证。
- **监督信号的依赖**：细胞通讯的真值由CellChat和CellNEST等计算工具生成，可能引入系统性偏差；模型实际上学的是“工具预测”，而非绝对生物学真实。
- **微调局限性**：除CellTok-mix外，多数任务单独微调，未充分展示零样本或少样本能力。CellTok-base在无微调下对群体的直接推理能力未评测。
- **仅支持转录组**：未能整合染色质可及性、蛋白质组等多模态数据，限制了更广的应用。
- **tokenizer设计未充分优化**：预定义5,000个HVG、固定码本大小等可能不适用于所有场景，更灵活的基因选择或基于LCM的初始化可进一步提升。
- **缺乏与大型通用LLM在复杂推理上的对比**：如GPT-4在疾病机制解释、通路功能推理等方面与CellTok的效果比较未被探索。

（完）
