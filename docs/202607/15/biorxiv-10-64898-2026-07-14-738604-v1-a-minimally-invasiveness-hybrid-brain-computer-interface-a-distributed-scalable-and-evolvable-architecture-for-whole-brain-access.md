---
title: "A Minimally Invasiveness Hybrid Brain-Computer Interface: A Distributed, Scalable and Evolvable Architecture for Whole Brain Access"
title_zh: 一种微创混合脑机接口：面向全脑接入的分布式、可扩展和可进化架构
authors: "Li, Z., Liu, N., Wan, L., Liu, M., Wu, C."
date: 2026-07-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.14.738604v1.full.pdf"
tags: ["query:neuro-mental"]
score: 9.0
evidence: 提出一种微创混合脑机接口架构
tldr: 非侵入式脑机接口信号保真度低，侵入式手术创伤大且扩展性差。为突破这一矛盾，提出以颅骨作为分布式接口层的微创混合BCI架构：通过智能微孔开颅在颅骨安全制备微孔（300-800μm），植入皮下微电极接触硬脑膜，配合外部双向可穿戴头戴设备与AI辅助控制系统。大鼠实验证明，该架构显著提升静息态功率谱与感觉诱发电位信噪比，计算模型显示其能增强颅内电场并聚焦于深部脑靶点。该工作为构建分布式、可扩展、可升级的全脑接入神经界面奠定了基础。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738604-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1618, \"height\": 899, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738604-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1628, \"height\": 1476, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738604-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1619, \"height\": 903, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738604-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1599, \"height\": 1036, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738604-v1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1637, \"height\": 1093, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738604-v1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1616, \"height\": 1300, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738604-v1/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1575, \"height\": 2072, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-14-738604-v1/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1600, \"height\": 1418, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-14-738604-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1510, \"height\": 367, \"label\": \"Table\"}]"
motivation: 解决非侵入BCI信号质量差与侵入BCI手术创伤大的矛盾，实现微创且高效的全脑接入。
method: 提出混合BCI架构：微孔开颅、颅骨植入微电极、外部可穿戴头戴设备及AI辅助规划控制。
result: 大鼠实验表明微孔安全可制备，信号功率谱及信噪比提升；计算模型实现深部脑靶点聚焦。
conclusion: 该混合BCI是分布式、可扩展的微创神经界面新范式，有望扩展临床应用。
---

## 摘要
脑机接口面临着一个基本权衡：无创系统的信号保真度和刺激精度与有创系统的手术负担和可扩展性之间的矛盾。无创脑机接口由于颅骨屏障以及头皮和颅骨引入的变异性，信号质量低且刺激精度差。现有的有创脑机接口依赖创伤性手术或穿透脑组织的电极，限制了其空间扩展性、应用和患者接受度。本文介绍了一种微创混合脑机接口架构，该架构将颅骨用作分布式接口层，而非仅将其视为屏障。该混合脑机接口包含四个集成组件：(1) 安全智能的微孔颅骨钻孔术；(2) 皮下植入颅骨微孔中的分布式微电极，远端与硬脑膜接触；(3) 用于耦合、记录、刺激和通道选择的外部双向可穿戴头戴设备；以及(4) AI辅助的规划与控制代理。动物研究表明，直径300-800微米的微孔可以在颅骨任何预定位置安全方便地制备，且不损伤硬脑膜。大鼠体内实验表明，与头皮脑电图相比，使用颅骨植入微电极的混合脑机接口明显增加了静息态频谱功率，并改善了体感和稳态视觉诱发电位的信噪比；计算模型显示，分布式颅骨-硬脑膜微电极可以增加颅内电场强度，并将聚焦的时域干涉场导向预定的深部脑靶点。这些发现将为混合脑机接口在无线集成、安全性评估和临床效益方面的未来研究奠定坚实基础。总之，我们提出混合脑机接口作为一种独特的微创脑机接口范式，具有作为分布式、可扩展和可升级的神经接口的巨大潜力，可扩展微创脑机接口技术的临床应用。

## Abstract
Brain-computer interfaces face a fundamental trade-off between the signal fidelity and stimulation precision of noninvasive systems and the surgical burden and scalability of invasive systems. Non-invasive BCIs suffer from low signal quality and poor stimulation accuracy due to the skull barrier and the variability introduced by the scalp and skull. Existing invasive BCIs rely on traumatic surgical procedures or brain-penetrating electrodes, which limits their spatial extensibility, application, and patient acceptance. Here, we introduce a minimally invasive hybrid BCI architecture that uses the skull as a distributed interface layer rather than treating it solely as a barrier. The hybrid BCI comprises four integrated components: (1) the safe and smart micro-hole craniotomy; (2) distributed microelectrodes subcutaneously implanted in micro-holes in the skull with the distal end in contact with the dura; (3) an external bi-directional wearable headset for coupling, recording, stimulation, and channel selection; and (4) an AI-assisted planning and control agent. Animal studies have shown that micro-holes with a diameter of 300-800 m can be safely and conveniently prepared at any predefined locations across the skull without impairing the dura. In vivo experiments on rats demonstrate that the hybrid BCI with skull-implanted microelectrodes evidently increases resting-state spectral power and improves the signal-to-noise ratio of somatosensory and steady-state visual evoked responses compared to the scalp EEG; the computational modelling shows that distributed skull-dura microelectrodes can increase the intracranial electrical field strength and steer focused temporal-interference fields towards predefined deep brain targets. These findings will lay a solid foundation for future endeavors in wireless integration, safety evaluation and clinical benefits of the hybrid BCI. In summary, we propose the hybrid BCI as a distinct minimally invasive BCI paradigm with the great potential as a distributed, scalable, and upgradable neural interface that can expand the clinical application of minimally invasive BCI techniques.

---

## 论文详细总结（自动生成）

# 论文结构化总结

## 1. 核心问题与整体含义（研究动机与背景）

**核心问题**：脑机接口（BCI）面临根本性权衡——非侵入式系统信号保真度低、刺激精度差（因颅骨屏障、头皮/颅骨变异）；侵入式系统（如硬膜下阵列、皮层内微电极）信号好但手术创伤大、可扩展性差、患者接受度低。现有深部脑刺激（DBS）和人工耳蜗的临床低接受率（1.6%~4.5% 的帕金森患者符合DBS条件，且其中60-70%拒绝手术）凸显了微创与性能平衡的迫切性。

**整体含义**：本文提出一种**微创混合BCI架构**，将颅骨视为分布式接口层而非单纯障碍物，通过颅骨微孔植入微电极与硬脑膜接触，配合外部可穿戴设备，旨在实现“介于非侵入式与侵入式之间的全新设计空间”。

---

## 2. 方法论：核心思想、关键技术细节

### 核心思想
构建四要素集成的混合BCI：
1. **安全智能微孔颅骨钻孔术（S²MHC）**：利用超声振动在不去除材料的前提下，在颅骨上制备直径300-800μm的微孔，微孔末端与硬脑膜接触，近端皮下。
2. **分布式微电极植入**：将定制Pt-Ir微电极植入微孔，远端接触硬脑膜，近端位于头皮-颅骨界面。
3. **外部双向可穿戴头戴设备**：用于信号耦合、记录、刺激和通道选择。
4. **AI辅助规划与控制代理**：用于电极植入规划、信号解码、电场优化及闭环控制。

### 关键技术细节
- **微孔颅骨钻孔术**：采用超声振动辅助，利用颅骨微孔结构的可塑性，通过高频锻造使骨组织侧向挤压，实现无材料去除的微孔成型。轴向力<500 mN（与皮下注射力相当）。通过内部同轴微通道冷却，温度控制在<42℃，术后2周愈合。
- **智能终止检测**：基于多模态信息的突破检测算法，响应时间34.0±16.4 ms，距离误差16.2±17.2 μm，确保不损伤硬脑膜。
- **微电极**：Pt-Ir材质，柱体直径500 μm，近端法兰直径0.7-4.0 mm作为深度限制结构。Ag/AgCl参比电极，低阻抗（<1 kΩ@0-100 Hz），相位角-10°至-30°（弱容性区）。
- **记录模式**：差分记录（E1-E2或C1-C2），参考公共地（GND）。带通滤波0.5-500 Hz，50 Hz陷波，采样率1000 Hz。
- **信号处理**：Welch法计算功率谱密度（PSD），2秒汉明窗，50%重叠。体感诱发电位（SEP）通过60次时域叠加平均。稳态视觉诱发电位（SSVEP）通过FFT提取频率特征。
- **神经调控模拟**：基于COMSOL Multiphysics球形头模型（四层：头皮、颅骨、脑脊液、大脑），采用准静态近似，求解泊松方程 ∇·(σ∇V)=0。时间干涉刺激（TI）通过两对电极的电场矢量合成，解析计算干涉包络最大值。

---

## 3. 实验设计：数据集/场景、基准、对比方法

### 实验场景与数据集
- **微孔制备实验**：兔（新西兰白兔）颅骨样本，SD大鼠活体。
- **神经记录实验**：12只SD大鼠（雄性，250-300g），随机分3组（每组4只），分别在S1/视觉皮层区域植入不同近端尺寸微电极（0.7 mm、1.5 mm、4.0 mm）。
- **基准（对照）**：同一大鼠对侧头皮EEG（C1-C2）作为非侵入式对照。
- **对比方法**：
  - 常规头皮EEG（控制组）。
  - 混合BCI-0.7（近端0.7 mm）、混合BCI-1.5（1.5 mm）、混合BCI-4.0（4.0 mm）。
- **刺激范式**：
  - 体感诱发电位（SEP）：大鼠尾部机械刺激（钝头针0.3 mm，线性致动器2 mm推进，周期5s，共60个周期）。
  - 稳态视觉诱发电位（SSVEP）：白光源闪烁（8、10、12、14 Hz，脉冲宽度900 μs，每个频率5个30s刺激块，间隔10s暗期）。
- **计算模型**：球形人头部模型（直径190 mm），对比传统经颅交流电刺激（tACS）、经颅时间干涉刺激（tTI）、混合BCI、无线混合BCI。

---

## 4. 资源与算力

文中**未明确说明**使用的GPU型号、数量或训练时长。计算部分主要涉及：
- 微孔成型模拟：Abaqus SPH（2D模型）。
- 热传导模拟：Abaqus稳态热传递模型。
- 电刺激模拟：COMSOL Multiphysics（AC/DC模块，有限元法）。
- 信号处理：MATLAB（Welch法、FFT、包络提取）。

未提及深度学习模型训练所需的算力资源。

---

## 5. 实验数量与充分性

| 实验类型 | 动物/样本数 | 重复次数 | 条件 |
|----------|-------------|--------|------|
| 微孔制备力测试 | 兔颅骨样本，n=4 | 未明确单样本重复 | 有/无超声振动对比 |
| 热效应测试 | 兔颅骨样本 | 多距离多点温度测量 | 有/无冷却 |
| 愈合实验 | SD大鼠 | 2、3、5周时间点取样 | 有/无冷却，H&E染色 |
| 终止检测精度 | 体外兔颅骨，n=3 | 每组？ | 预设进给距离误差 |
| 体内微孔安全性 | 兔 | 每组1只？ | 有/无智能控制，伊文思蓝染色 |
| SEP记录 | 12只大鼠（4只/组） | 每只60次刺激叠加 | 3种电极尺寸 vs EEG |
| SSVEP记录 | 12只大鼠（4只/组） | 5个30s刺激块/频率 | 4种频率 × 3种电极尺寸 vs EEG |

**充分性评价**：
- **较好之处**：每个实验条件使用了多个独立动物（n=4），且进行了多次重复（SEP 60次叠加，SSVEP 5个block），数据具有统计意义。
- **不足**：
  - 体外实验样本量较小（终止检测n=3，热测试未报告重复数）。
  - 未进行动物间的交叉验证（如不同电极尺寸在不同大鼠上顺序测试）。
  - 未报告缺失值或动物排除标准。
  - 微孔愈合实验仅展示定性组织学图像，无定量统计分析（如骨密度、愈合率）。
  - SEP和SSVEP的信噪比（SNR）比较仅呈现热图/柱状图，未提供统计检验（如t检验或ANOVA）的p值。
  - 计算模拟采用简化球形模型，未验证异质性颅骨模型下的鲁棒性。

**客观性**：内文未声明利益冲突，但专利由合作公司（Shenzhen BrainXess Technology Co., Ltd.）申请，存在潜在利益关系。部分作者为该公司员工。

---

## 6. 主要结论与发现

1. **微孔颅骨钻孔术可行**：超声振动辅助可在颅骨安全制备300-800μm微孔，轴向力<500 mN，最大温度<42℃，术后2周愈合，智能终止检测可避免硬脑膜损伤。
2. **神经记录性能提升显著**：
   - 混合BCI-1.5的静息态功率比EEG高2.6-5倍（各频段）；混合BCI-4.0高4.1-8.9倍。
   - SEP信噪比：EEG为12-21，混合BCI-1.5提升至18-30，混合BCI-4.0提升至33-47。
   - SSVEP：EEG无法检测到特征峰；混合BCI-0.7即可检测弱峰；混合BCI-1.5和4.0呈现清晰窄带峰，信噪比随频率升高而增大。
3. **神经调控模拟优势**：
   - 混合BCI可提高颅内电场强度，减少电流分流，聚焦性优于经颅时间干涉刺激（tTI）。
   - 无线混合BCI（直接刺激硬脑膜）可进一步缩小半高宽（FWHM），提升深部靶点聚焦能力。
4. **可扩展性**：分布式微电极可按需增量植入，结合外部可升级的头戴设备，实现全脑覆盖与长期可进化。

---

## 7. 优点（方法或实验设计亮点）

- **创新性架构**：提出“颅骨作为接口层”的范式，巧妙平衡了微创与信号质量，填补了非侵入与侵入式之间的空白。
- **超声微孔技术细节成熟**：解决了传统机械/激光钻孔的难点（工具断裂、热损伤、硬脑膜损伤），实现了类似针灸的微孔制备。
- **多模态验证**：同时提供了微孔制备的力学/热学评估、活体神经记录（两种诱发范式）和计算模拟，覆盖了从物理层到功能层的验证。
- **灵活可扩展设计**：微电极尺寸可选（0.7-4.0 mm），植入位置可编程，结合外接设备升级，具有临床转化潜力。
- **对比基准合理**：使用同一动物对侧头皮EEG作为对照，减少了生物差异干扰。
- **计算模拟全面**：比较了tACS、tTI、混合BCI、无线BCI四种策略，并分析了电极位置和电流比率对聚焦性的影响。

---

## 8. 不足与局限

### 实验覆盖不足
- **长期慢性研究缺失**：未报告微电极植入后超过1周的记录稳定性、组织反应（如胶质增生、腐蚀）或信号衰减。
- **无线系统未实现**：文中仅模拟了无线混合BCI，未进行无线遥测验证（功率传输、数据传输、自由活动动物记录）。
- **闭环控制缺失**：AI辅助规划和控制仅概念性描述，未有实际闭环实验。
- **频率范围有限**：记录带宽仅0.5-500 Hz，未涵盖高频（>500 Hz）或场电位；刺激模拟仅限kHz范围。
- **样本量偏小**：每组4只动物，统计效力不足（未提供功效分析），组间比较缺乏显著性检验（p值）。
- **对照条件不完整**：SEP和SSVEP实验的EEG控制组仅使用了0.7 mm植入组大鼠的对侧记录，未使用未植入微电极的完全空白对照组（以排除微电极存在对EEG的影响）。
- **温度测量**：仅测量0.5 mm处温度，模拟预测孔壁达43℃（接近安全阈值），实际温度梯度可能更高，安全性边界不明确。

### 方法局限
- **简化头模型**：球形模型忽略了个体解剖差异（颅骨厚度、曲率、异质性），模拟结果可能高估聚焦性。
- **准静态假设**：忽略频率依赖性导电率（尤其是TI刺激的高频载波），可能影响包络场计算精度。
- **电刺激安全性未评估**：未讨论微电极植入后的电化学安全性（电荷注入极限、组织损伤阈值）。
- **硬脑膜长期接触反应**：微电极远端直接接触硬脑膜，长期压迫可能诱发硬脑膜增生或炎症，未报道长期组织学结果。
- **人工智能部分模糊**：AI代理的具体算法、训练数据、性能指标未披露，仅作为概念提及。

### 应用限制
- **有创性仍存在**：虽然微孔比传统颅骨钻孔创伤小，但仍需皮肤切口、颅骨微孔制备、电极植入，与完全无创相比患者接受度未知。
- **可扩展性代价**：多节点植入需多个微孔，可能累加手术时间与风险（出血、感染）。微孔间距800 μm可密集种植，但硬脑膜上多个接触点可能产生局部应力集中。
- **头戴设备耦合稳定性**：外部头套与皮下微电极的耦合依赖精确对准，日常使用中可能因活动移位。
- **伦理与监管**：作为新型植入式设备，需满足严格生物相容性标准（ISO 10993），MRI兼容性待验证。

### 偏差风险
- **利益冲突**：合作公司为专利申请方，主要发明人同为作者，可能存在报告偏倚。
- **选择性报告**：仅报告了成功实验，未提及失败案例（如微孔制备断裂、植入后动物死亡、信号不良等）。
- **结果呈现**：SNR对比图仅显示范围，未提供均值±标准差或统计检验；部分功率谱图为单条曲线，无法评估动物间变异。

---

（完）
