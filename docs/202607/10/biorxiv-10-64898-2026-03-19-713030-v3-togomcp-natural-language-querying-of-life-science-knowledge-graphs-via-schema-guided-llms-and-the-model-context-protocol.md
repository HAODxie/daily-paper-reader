---
title: "TogoMCP: Natural Language Querying of Life-Science Knowledge Graphs via Schema-Guided LLMs and the Model Context Protocol"
title_zh: TogoMCP：基于模式引导的LLM与模型上下文协议实现生命科学知识图谱的自然语言查询
authors: "Kinjo, A. R., Yamamoto, Y., Bustamante-Larriet, S., Labra-Gayo, J. E., Fujisawa, T."
date: 2026-07-06
pdf: "https://www.biorxiv.org/content/10.64898/2026.03.19.713030v3.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 基于LLM的生命科学知识图谱自然语言查询系统
tldr: "生命科学知识图谱查询需要精通SPARQL和数据库模式，阻碍了大多数研究者。TogoMCP通过模型上下文协议(MCP)将大语言模型重构为协议驱动的推理引擎，利用MIE文件动态提供模式上下文，并采用两阶段工作流先进行实体解析再生成SPARQL。在50个生物问题上，相比无辅助基线取得大幅提升(Cohen's d=1.82)，准确率超80%。关键贡献在于发现简洁动态的模式上下文比复杂编排逻辑对平均性能更有效，而程序指导可互补地降低结果方差。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-03-19-713030-v3/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1752, \"height\": 1488, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-03-19-713030-v3/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 790, \"height\": 516, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-03-19-713030-v3/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 781, \"height\": 257, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-03-19-713030-v3/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 773, \"height\": 255, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-03-19-713030-v3/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 885, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-03-19-713030-v3/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1158, \"height\": 253, \"label\": \"Table\"}]"
motivation: 现有LLM将自然语言转为SPARQL时缺乏模式上下文，常编造不存在的谓词，导致查询失败。
method: TogoMCP利用MIE文件动态提供数据库模式上下文，通过两阶段流程先调用REST API解析实体，再生成模式引导的SPARQL。
result: "在50个生物问题上，相比无辅助基线提升显著(Cohen's d=1.82)，准确率超80%，MIE文件贡献最大均值提升(+0.50)。"
conclusion: 简洁动态的模式上下文比复杂编排对平均性能更关键，程序指导可互补地降低结果方差。
---

## 摘要
查询DBCLS维护的RDF Portal知识图谱——该图汇聚了约60个生命科学数据库——需要精通SPARQL和特定于数据库的RDF模式，这使得大多数研究人员难以利用这一资源。大型语言模型原则上可以将自然语言问题转化为可执行的SPARQL，但缺乏模式级上下文时，它们常常虚构不存在的谓词，或未能将实体名称解析为特定于数据库的标识符。我们提出了TogoMCP，该系统将LLM重新定位为协议驱动的推理引擎，通过模型上下文协议（MCP）编排专用工具。其设计有两个关键机制：（i）MIE（元数据-互操作性-交换）文件，一个简洁的YAML文档，在查询时动态为LLM提供每个目标数据库的结构和语义上下文；（ii）一个两阶段工作流，将外部REST API的实体解析与模式引导的SPARQL生成相分离。在一个涵盖五种类型、23个数据库的50个生物学基础问题的基准测试中，TogoMCP相比无辅助基线取得了大幅提升（Cohen's d = 1.82，Wilcoxon p < 0.001），对于具有精确可验证答案的问题类型，胜率超过80%。消融研究表明，所有组件配置均带来显著改进，其中MIE模式文件在平均每题得分上的边际贡献最大（相对于无MIE条件，Δ = +0.50，双尾Wilcoxon p = 0.067；90% bootstrap CI [+0.04, +0.94]排除零）；一条加载相关MIE文件的单行指令即可恢复到完整程序化协议的相同平均改进，而协议还额外降低了风险（损失率1.6%对4.8%，Fisher p = 0.036）。这些结果表明了一个通用设计原则：对于平均得分性能而言，简洁、动态传递的模式上下文比复杂的编排逻辑更有价值，而程序化引导在缩小方差方面发挥补充作用。

数据库URL：https://togomcp.rdfportal.org/

## Abstract
Querying the RDF Portal knowledge graph maintained by DBCLS--which aggregates approximately 60 life-science databases--requires proficiency in both SPARQL and database-specific RDF schemas, placing this resource beyond the reach of most researchers. Large Language Models (LLMs) can, in principle, translate natural-language questions into executable SPARQL, but without schema-level context, they frequently fabricate non-existent predicates or fail to resolve entity names to database-specific identifiers. We present TogoMCP, a system that recasts the LLM as a protocol-driven inference engine orchestrating specialized tools via the Model Context Protocol (MCP). Two mechanisms are essential to its design: (i) the MIE (Metadata-Interoperability-Exchange) file, a concise YAML document that dynamically supplies the LLM with each target databases structural and semantic context at query time; and (ii) a two-stage workflow separating entity resolution via external REST APIs from schema-guided SPARQL generation. On a benchmark of 50 biologically grounded questions spanning five types and 23 databases, TogoMCP achieved a large improvement over an unaided baseline (Cohens d = 1.82, Wilcoxon p < 0.001), with win rates exceeding 80% for question types with precise, verifiable answers. An ablation study shows that all component configurations deliver significant improvements, with MIE schema files providing the largest marginal contribution on mean per-question score ({Delta} = +0.50 relative to a no-MIE condition, two-sided Wilcoxon p = 0.067; 90% bootstrap CI [+0.04, +0.94] excludes zero); a one-line instruction to load the relevant MIE file recovers the same mean improvement as a full procedural protocol, while the protocol additionally reduces downside risk (loss rate 1.6% vs. 4.8%, Fisher p = 0.036). These results suggest a general design principle: concise, dynamically delivered schema context is more valuable than complex orchestration logic for mean-score performance, while procedural guidance plays a complementary role in narrowing variance.

Database URL: https://togomcp.rdfportal.org/

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：生命科学领域存在大量异构的RDF知识图谱（如RDF Portal聚合了约60个数据库），但直接查询需要精通SPARQL语言和各数据库特有的RDF模式，对于大多数研究人员门槛过高。大语言模型（LLM）虽有将自然语言翻译为SPARQL的潜力，但缺乏模式上下文时经常虚构不存在的谓词或无法正确解析实体名称。
- **整体含义**：本文旨在构建一个低门槛、高可靠的自然语言接口，使生物学家无需掌握SPARQL和数据库模式就能查询跨数据库的知识图谱，从而释放这些数据资源的研究价值。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：将LLM作为协议驱动的推理引擎，通过模型上下文协议（MCP）编排专用外部工具，并利用精心设计的MIE（Metadata-Interoperability-Exchange）文件动态提供数据库模式上下文。
- **关键技术细节**：
  - **MIE文件**：一种YAML格式的文档，包含数据库元数据、实体类形状表达式（ShEx）、示例SPARQL查询、反模式/常见错误等11个必需部分。每个数据库对应一个MIE文件，在查询时由`get MIE file`工具按需传递给LLM。
  - **两阶段混合工作流**：
    1. **实体解析阶段**：优先调用专用的REST API（如UniProt、ChEMBL、NCBI E-utilities等）进行快速、结构化的实体名称到标识符的解析。
    2. **SPARQL生成阶段**：在获取确切标识符后，参考MIE文件构建并执行SPARQL查询，聚焦于图遍历而非文本匹配。
  - **TogoMCP Usage Guide**：一个经验性的执行协议，以工具形式注入LLM，规定了问题类型分类、工具选择优先级、SPARQL调用预算、防御性查询策略等。
  - **系统实现**：基于FastMCP库，包含SPARQL层和Web API层，支持28个RDF数据库，8个SPARQL端点。额外集成了外部MCP服务器（PubMed、OLS4、PubDictionaries）。

## 3. 实验设计：数据集/场景、基准测试、对比方法

- **基准测试**：人工构建50个生物学基础问题，涵盖5种类型（是非题、事实题、列举题、总结题、选择题），每种10题。问题涉及至少2个数据库（60%）、至少3个数据库（20%），覆盖当时所有23个数据库。每个问题有确切的答案字段（ground truth）和理想答案段落。
- **对比方法**：
  - **基线**：无工具的Claude Sonnet 4.5（`claude-sonnet-4-5-20250929`）。
  - **TogoMCP全系统**：相同的LLM加上MCP工具、MIE文件和Usage Guide。
  - **消融条件**（共4个实验条件）：With Guide（全系统）、MIE-Instr（无Usage Guide但有一条指令要求使用`find databases`和`get MIE file`）、No-Instr（无Guide也无指令）、No MIE（移除`get MIE file`工具）。
- **评估指标**：由LLM Judge（Claude Opus 4.7）对Recall、Precision、Non-redundancy、Readability四个维度各1-5分，总分4-20。每个问题-答案对独立评估5次取平均。此外在20个问题子集上进行了三位领域专家的人工盲评对比。

## 4. 资源与算力

- **算力信息**：论文未明确说明使用的GPU型号、数量或训练时长。实验中使用的是Anthropic的闭源API（Claude Sonnet 4.5和Opus 4.7），因此计算资源由API提供方管理，作者未报告具体硬件配置或训练过程。注意：MIE文件的创建是半自动的，需要少量人工验证，但无需训练新模型。

## 5. 实验数量与充分性

- **实验数量**：
  - 主实验：50个问题×2个条件（基线+TogoMCP）×5次评估 = 250个评估对。
  - 消融实验：4个条件（With Guide, MIE-Instr, No-Instr, No MIE）各50个问题×5次 = 1000个评估对。
  - 人工验证：20个问题子集由3位独立专家盲评。
- **充分性与公平性**：
  - 实验设计系统：问题类型均衡、数据库覆盖全面、问题答案经过SPARQL执行和算术验证；避免了能从预训练或文献直接回答的问题；每个问题要求实体解析而非直接给出标识符。
  - 统计方法严谨：使用了Cohen's d、Wilcoxon符号秩检验、Fisher精确检验、Levene方差检验、Bootstrap置信区间等。
  - 消融实验设计合理，分离了MIE文件和Usage Guide的贡献。
  - 存在一定局限：问题数量50题相对有限；仅使用了Claude模型家族；未在更多大模型上交叉验证。

## 6. 论文的主要结论与发现

- **整体性能**：TogoMCP比无工具基线大幅提升（总分Δ = +3.45，Cohen's d = 1.82，p < 0.001），胜率94.4%，基线从未达到满分，TogoMCP在42.8%的评估中得满分（20分）。改进主要集中在Recall（+2.23）和Precision（+1.04）。
- **问题类型差异**：是非题提升最大（Δ=+4.22，胜率100%），总结题提升最小（Δ=+2.44，胜率90%）。
- **消融研究关键发现**：
  - 所有消融条件均显著优于基线。
  - **MIE文件是平均性能的主要贡献者**：移除MIE文件后，每题平均改进减少0.50分（90% bootstrap CI排除零）。即使没有MIE，通过迭代SPARQL探索也能部分补偿，但对非标准RDF结构数据库失效。
  - **一条使用MIE的指令**（MIE-Instr）就能恢复完整Usage Guide的相同平均改进（Δ = +3.46 vs +3.45，无显著差异）。
  - **Usage Guide的额外价值在于降低方差和风险**：损失率从4.8%（MIE-Instr）降至1.6%（With Guide），Fisher p=0.036；问题间标准差也更小。
  - **一般性结论**：对平均性能，简洁动态的模式上下文比复杂编排逻辑更关键；程序化协议在管理最坏情况上发挥互补作用。

## 7. 优点

- **创新性**：提出MIE文件作为标准化、数据库可移植的上下文单元，并实证表明其是高性能的关键，而非复杂协议。
- **工程实用性**：工具设计包含防幻觉机制（工具描述作为协议契约、参数名同义处理、错误带内恢复指导等），提高了LLM工具调用的鲁棒性。
- **两阶段分离**：将实体解析与SPARQL生成解耦，降低了LLM在SPARQL内进行文本匹配的难度。
- **全面评估**：包括多类型问题、多次评估、消融实验、人工验证，统计严谨。
- **公开可用**：源代码和服务器公开，便于复现和扩展。

## 8. 不足与局限

- **评估覆盖有限**：50个问题仅为可能查询空间的一小部分；新增的5个数据库未被纳入初始基准。
- **仅使用Claude模型**：未测试其他模型家族（如GPT-4、Llama等），通用性待验证。
- **LLM Judge偏差**：主评估依赖LLM Judge（Claude Opus 4.7），虽有人工验证但仅20个问题子集，且在非冗余性和可读性维度上LLM Judge与人工评分有一定分歧（相关系数低）。
- **人工验证的局限性**：三位专家间一致性中等（ICC(2,1)=0.675），认知负荷大，可能影响评分准确性。
- **MIE文件质量依赖人工**：每新增一个数据库需要2-4小时专家努力，扩展性有限；随着数据库模式更新，MIE文件可能过时，自动化检测尚未实现。
- **跨端点查询的脆弱性**：通过顺序多查询和TogoID桥接不同端点，存在标识符遗漏导致下游计数错误的风险，且没有自动错误检查。
- **未测试模糊实体解析场景**：基准问题设计为单一正确解析路径，避免了歧义案例，实际应用中可能遇到更复杂情况。
- **成本和延迟**：平均每查询耗时137秒、花费0.38美元，虽然对高精度查询可接受，但在低成本场景下可能不切实际。

（完）
