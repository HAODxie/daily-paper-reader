---
title: "VFB-MCP: Natural-Language Access to Drosophila Neuroscience Grounded by an Expert-Curated Ontology-Led Knowledgebase"
title_zh: VFB-MCP：基于专家策划的本体驱动知识库的果蝇神经科学自然语言访问
authors: "McLachlan, A. D., Court, R., Pilgrim, C., Longden, K., Brown, N. H. D., Osumi-Sutherland, D., Jefferis, G. S. X. E., Armstrong, D. J."
date: 2026-07-14
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.16.732577v2.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 大语言模型用于神经科学数据库自然语言访问
tldr: "生物数据库访问依赖专业查询技能，阻碍了经验丰富的科学家和新手整合复杂数据。本研究开发VFB-MCP系统，通过模型上下文协议将果蝇专家知识库暴露给大语言模型，实现自然语言访问。在30个神经科学任务上，VFB-MCP-equipped大语言模型以25/30的正确率远超裸大语言模型（2/30）和网络辅助大语言模型（14/30），尤其在量化任务上优势显著（89% vs 11%）。工作表明，基于本体知识图谱的MCP可有效提升大语言模型在神经科学和连接组学数据上的回答质量，促进复杂集成数据的可访问性和可靠分析。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-06-16-732577-v2/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1671, \"height\": 987, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-06-16-732577-v2/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1578, \"height\": 1401, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-06-16-732577-v2/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1612, \"height\": 952, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-06-16-732577-v2/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1616, \"height\": 1044, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-06-16-732577-v2/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1650, \"height\": 550, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-06-16-732577-v2/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1637, \"height\": 397, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-06-16-732577-v2/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1637, \"height\": 397, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-06-16-732577-v2/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1647, \"height\": 975, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-06-16-732577-v2/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1646, \"height\": 505, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-06-16-732577-v2/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1650, \"height\": 836, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-06-16-732577-v2/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1648, \"height\": 649, \"label\": \"Table\"}]"
motivation: 降低非专业用户访问生物数据库的门槛，提升大语言模型在神经科学等专业领域数据查询的准确性和可量化性。
method: 通过模型上下文协议将专家维护的本体知识图谱（Virtual Fly Brain）暴露给大语言模型，实现自然语言驱动的精准访问。
result: 在30个神经科学任务中，VFB-MCP-equipped大语言模型正确回答25个，显著优于裸大语言模型（2个）和网络辅助模型（14个）。
conclusion: 基于本体知识图谱的MCP是提升大语言模型在连接组学等专业领域回答质量的有效方法，能促进复杂集成数据的可访问性。
---

## 摘要
生物数据库存储着经过策划的知识，研究人员传统上通过网络界面或API访问这些知识。要超越随意浏览，需要领域特定的知识和专业知识来构建探索这些数据所需的查询。这给试图整合广泛信息源的有经验用户以及进入正在经历范式转变（如连接组学）的科学领域的新用户都设置了障碍。降低这些障碍的一个潜在有效方法是，通过模型上下文协议（MCP）将数据库暴露给大型语言模型（LLM），从而促进对数据库的自然语言访问。我们在Virtual Fly Brain（VFB，一个专家策划的、基于本体的果蝇神经科学知识库）上实现了这一点，提供了所需的精确性，使最近整合的连接组和分子数据变得可访问。在30项神经科学任务上，与裸LLM和网络搜索辅助LLM进行基准测试，配备VFB-MCP的LLM在25/30的任务中产生了精确、可验证且适当量化的答案，而网络搜索辅助LLM为14/30，裸LLM为2/30。在需要数据量化的任务中，MCP的优势最大（89%对11%的网络搜索）。这项工作确立了将MCP叠加在基于本体的知识图谱之上，作为提高LLM在神经科学和连接组学数据上响应质量的有效方法，促进了可访问性，并加速了对复杂集成数据集的可靠分析。

## Abstract
Biological databases store curated knowledge that researchers traditionally access through web interfaces or APIs. To move beyond casual browsing requires domain-specific knowledge and expertise to frame the queries necessary to explore this data. This generates barriers to both experienced users trying to integrate wide-ranging sources of information and for new users entering scientific fields undergoing paradigm shifts such as connectomics. A potentially powerful method to lower these barriers is to facilitate natural-language access to these databases by exposing them to large language models (LLMs) via the Model Context Protocol (MCP). Here we implement this for Virtual Fly Brain (VFB), an expert-curated and ontology-backed knowledgebase of Drosophila neuroscience, providing the precision needed to make recently integrated connectome and molecular data accessible. Benchmarked on 30 neuroscience tasks against a bare LLM and a web-search-assisted LLM, the VFB-MCP-equipped LLM produces precise, verifiable and appropriately quantified answers on 25/30 tasks vs 14/30 for web and 2/30 for bare. The MCP advantage is largest for tasks where data quantification is required (89% vs 11% web). This work establishes MCP layered over ontology-backed knowledge graphs as an effective method to improve LLM response quality for neuroscience and connectomics data, promoting accessibility and accelerating the reliable analysis of complex integrated datasets.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：生物数据库（如Virtual Fly Brain）存储了专家策划的结构化知识，但传统访问方式（Web界面、API、REST接口）需要用户具备领域专长和编程能力，形成了显著的**可访问性鸿沟**。特别是对于连接组学等新兴领域，新的研究者难以高效地查询、整合和推理复杂数据集。
- **整体含义**：本研究提出通过模型上下文协议（Model Context Protocol, MCP）将大型语言模型（LLM）与专家策划的本体知识图谱相结合，实现**自然语言驱动的精准数据库访问**。这种“智能体RAG”范式允许LLM在运行时自主调用数据库工具，进行多跳检索和推理，从而显著降低非专业用户使用专业数据库的门槛，加速科学发现。

---

### 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：利用MCP标准接口，将LLM转化为**自主代理**，使其能够根据用户问题自行决定需要哪些上下文，通过调用预设工具查询数据库，并利用本体驱动的运行时内省（introspection）逐步细化查询。
- **关键技术细节**：
  - **三层架构**：
    - 形式化本体层（Drosophila Anatomy Ontology, DAO）：定义实体类型、关系约束，提供语义骨架。
    - 图数据库层（Neo4j）：存储策划知识，支持高效的路径遍历和关系查询。
    - 最小化MCP工具层：仅暴露三个通用工具。
  - **三个核心MCP工具**：
    - `search_terms`：基于Solr的全文本搜索，可按约100种实体类型过滤，返回VFB ID。
    - `get_term_info`：获取实体的规范记录，其中包含**Queries数组**，列出该实体可用的所有查询类型（运行时内省的关键）。
    - `run_query`：执行(id, query_type)对的查询，支持批量操作；查询类型包括`NeuronInputsTo`、`SubclassesOf`、`ExpressionOverlapsHere`、`clusterExpression`等。
  - **工作流**：搜索→内省→执行（search → introspect → execute）。LLM首先调用`search_terms`识别实体ID，然后调用`get_term_info`获取可用的查询类型，再调用`run_query`获取结构化结果。整个过程中，LLM基于前面调用的返回结果自主决定下一步操作，实现多跳检索。
  - **部署**：TypeScript实现的MCP服务器，部署为无状态HTTP端点，兼容Claude Desktop、Claude Code、VS Code等多种客户端。

---

### 3. 实验设计：数据集/场景、Benchmark、对比方法

- **数据集/场景**：Virtual Fly Brain（VFB）知识库，它是一个专家策划的、基于本体的果蝇神经科学知识库，整合了连接组数据、单细胞转录组数据、转基因驱动子库等。
- **Benchmark**：作者设计了一套**30项果蝇神经科学任务**，分为四类：
  - **类别1（简单知识，8项）**：已知事实，如蘑菇体主要分区。
  - **类别2（整合/调查，5项）**：开放性研究问题，需要定性综合。
  - **类别3（多跳，8项）**：2-3步链式操作，如神经递质输入映射到神经元类别。
  - **类别4（图遍历/量化，9项）**：连接推理、层次导航、跨模态查询，需要精确ID和量化计数。
- **对比方法**：使用同一个前沿LLM（Claude Opus 4.7）在三种条件下测试：
  - **裸LLM（Bare）**：仅依靠训练数据，无外部工具。
  - **LLM + 网页搜索（Web）**：赋予网页搜索和抓取工具，但网页内容经过独立LLM摘要后返回（两阶段）。
  - **LLM + VFB-MCP（MCP）**：赋予三个VFB-MCP工具。
- **评分标准**：由领域专家基于VFB当前数据库状态作为主要真实标准，对每个答案进行4分制评分（-1: 捏造, 0: 错误且不捏造, 1: 大致正确但缺细节, 2: 精确正确且可量化），并记录部分捏造（PF）和文献-数据不一致（LD）标志。

---

### 4. 资源与算力

- 论文中**没有明确说明使用的GPU型号、数量或训练时长**。实验是在Claude Opus 4.7（Anthropic的专有模型）上进行的，作者通过Claude Code CLI以非交互模式运行，设置了**每张提示最大预算3美元**和**600秒超时**。
- 作者报告了一次完整30任务扫描的成本：裸LLM约1.36美元（~14分钟），MCP约16.30美元（~61分钟），网页搜索约11.80美元（~43分钟）。MCP条件成本约为裸的12倍，网页的1.4倍。
- 此外，作者提到正在开发基于本地模型（Llama 3.3 70B Instruct）的VFB-chat，托管在Edinburgh ELM上，以降低成本。

---

### 5. 实验数量与充分性

- **实验数量**：在30项任务上，每个条件只进行了一次重复（1 rep per task）。作者承认**未捕捉LLM响应的概率性波动**。
- **充分性与公平性**：
  - 任务设计覆盖了从简单检索到复杂量化的四种代表性类别，但作者也承认**并未穷尽所有可能的神经科学查询**。
  - 比较条件设置合理：使用同一LLM，不同工具集，关键区别在于裸LLM无外部知识，网页搜索依赖文本摘要，MCP依赖结构化查询。
  - 评分者未设盲（scorer not blinded），因为答案中的引用来源（MCP vs 网页 vs 无引用）本质上无法隐藏。
  - 实验展示了显著的统计差异（Friedman检验p=1.4e-8，成对Wilcoxon检验均显著），但单次重复降低了结果的可靠性。
- **总体评价**：实验设计覆盖了关键维度，有力地证明了MCP的优势，但单次重复和未设盲是明显的局限性。

---

### 6. 论文的主要结论与发现

- **主要结论**：基于MCP的本体知识图谱访问方法可以大幅提升LLM在果蝇神经科学和连接组学数据上的回答质量。具体地：
  - MCP条件在30项任务中获得了**25个精确正确（score=2）**，而网页搜索为14个，裸LLM为2个。
  - 在**量化任务（类别4）**上，MCP优势最大：89%精确率（8/9），网页仅11%（1/9），裸LLM为0%。
  - 在多跳任务（类别3）上，MCP也显著优于网页（75% vs 25%）。
  - **整体差异高度显著**：Friedman χ²=36.10, p=1.4e-8；成对比较均显著。
- **其他发现**：
  - 完全没有出现完全捏造的答案（score=-1），但**部分捏造（PF）**在所有条件下发生率相似（约20-27%），但失败模式不同：MCP的PF主要来源于在正确MCP骨架上的训练数据填充或本体类混淆，而网页的PF涉及更多实体绑定错误和文献误读。
  - 实体绑定是结构化工具访问相对于文本检索的核心优势：MCP通过ID锁定实体，避免了网页搜索中常见的“真实论文但绑定了错误实体”的错误。

---

### 7. 优点

- **方法创新**：提出了一种基于MCP的智能体RAG范式，利用本体驱动的运行时内省，使LLM能够自主发现可用的查询类型，无需预先编码特定领域的工具。三个通用工具覆盖了广泛检索需求。
- **实际效用**：极大地降低了非专家研究者访问复杂连接组学数据的技术门槛，使得自然语言即可获得精确、可验证的量化结果。
- **实验设计**：对比网页搜索和裸LLM两种常见替代方案，系统评估了不同工具设置的效果，并详细分析了失败模式。
- **可复现性**：提供了完整的代码、数据、评分记录和统计分析方法，部署了公开的MCP服务器。
- **安全性**：MCP工具为只读操作，无写入路径，不增加安全风险。

---

### 8. 不足与局限

- **实验局限性**：
  - 仅测试了**一个模型（Claude Opus 4.7）**，可能不适用于其他LLM。
  - **单次重复**，未考虑LLM输出的随机性，结果可能不稳定。
  - **未设盲**的评分可能引入主观偏差。
  - 任务电池虽然覆盖代表类别，但**未穷尽所有查询类型**；且对于网页搜索，结果高度依赖于是否有文献包含所需数据（对于研究较少的神经元，网页搜索条件几乎无效）。
- **方法局限性**：
  - MCP条件中部分捏造仍会发生，尤其是当LLM在正确数据库输出上叠加上训练数据中的错误细节时。作者建议未来可补充PubMed MCP服务器来缓解。
  - 大规模查询可能导致MCP返回超大数据包（>1MB），需要客户端能够处理溢出，增加了实现复杂性。
  - **成本较高**：MCP条件成本约为裸LLM的12倍（约16.3美元/30任务），对于资源有限的研究者可能难以承受。
- **其他**：
  - 作者提到未使用验证代理来交叉检查回答中的引用，因为会增加显著的时间和成本，且验证代理本身也可能有同样的问题。
  - 系统目前仅适用于果蝇神经科学领域，迁移到其他物种或领域需要构建相应的本体和MCP服务器。

（完）
