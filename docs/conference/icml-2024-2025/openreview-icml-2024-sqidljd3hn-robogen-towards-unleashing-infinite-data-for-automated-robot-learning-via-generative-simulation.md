---
title: "RoboGen: Towards Unleashing Infinite Data for Automated Robot Learning via Generative Simulation"
title_zh: RoboGen：通过生成仿真实现自动化机器人学习的无限数据生成
authors: "Yufei Wang, Zhou Xian, Feng Chen, Tsun-Hsuan Wang, Yian Wang, Katerina Fragkiadaki, Zackory Erickson, David Held, Chuang Gan"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=SQIDlJd3hN"
tags: ["query:ur"]
score: 7.0
evidence: 通过生成仿真环境自动产生机器人训练数据
tldr: 现有的机器人技能学习方法依赖大量人工数据采集和监督，限制了可扩展性。RoboGen提出了一个自驱动的生成仿真框架，利用生成模型自动产生多样化的任务、场景和训练监督信号。实验表明，该方法能够使机器人在无需人工干预的情况下学习多种技能，显著提升了学习效率和泛化能力。这项工作为机器人数据集的自动构建提供了全新范式。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-sqidljd3hn/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1505, \"height\": 1027, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-sqidljd3hn/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1600, \"height\": 699, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-sqidljd3hn/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1494, \"height\": 753, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-sqidljd3hn/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1410, \"height\": 463, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-sqidljd3hn/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1412, \"height\": 460, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-sqidljd3hn/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1703, \"height\": 424, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-sqidljd3hn/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1770, \"height\": 1868, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-sqidljd3hn/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1543, \"height\": 237, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-sqidljd3hn/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1475, \"height\": 935, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-sqidljd3hn/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1470, \"height\": 2344, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-sqidljd3hn/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1471, \"height\": 2298, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-sqidljd3hn/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1471, \"height\": 2295, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-sqidljd3hn/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1472, \"height\": 1986, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-sqidljd3hn/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1294, \"height\": 281, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-sqidljd3hn/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1482, \"height\": 433, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-sqidljd3hn/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1234, \"height\": 1117, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-sqidljd3hn/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1233, \"height\": 1918, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-sqidljd3hn/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1227, \"height\": 229, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-sqidljd3hn/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1231, \"height\": 296, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-sqidljd3hn/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1232, \"height\": 731, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-sqidljd3hn/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1537, \"height\": 1641, \"label\": \"Table\"}]"
motivation: 减少机器人技能学习中对人工数据采集的依赖，实现自动化数据生成。
method: 采用自驱的“提出-生成-学习”循环，利用基础模型和生成模型自动创建任务、场景及监督信号。
result: 在多种仿真环境中有效学习多样化技能，无需人工标注，展示了强大的可扩展性。
conclusion: RoboGen为自动生成机器人训练数据提供了可扩展的框架，对数据集构建有重要启示。
---

## Abstract
We present RoboGen, a generative robotic agent that automatically learns diverse robotic skills at scale via generative simulation. RoboGen leverages the latest advancements in foundation and generative models. Instead of directly adapting these models to produce policies or low-level actions, we advocate for a generative scheme, which uses these models to automatically generate diversified tasks, scenes, and training supervisions, thereby scaling up robotic skill learning with minimal human supervision. Our approach equips a robotic agent with a self-guided propose-generate-learn cycle: the agent first proposes interesting tasks and skills to develop, and then generates simulation environments by populating pertinent assets with proper spatial configurations. Afterwards, the agent decomposes the proposed task into sub-tasks, selects the optimal learning approach (reinforcement learning, motion planning, or trajectory optimization), generates required training supervision, and then learns policies to acquire the proposed skill. Our fully generative pipeline can be queried repeatedly, producing an endless stream of skill demonstrations associated with diverse tasks and environments.

---

## 论文详细总结（自动生成）

# RoboGen 论文详细总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：机器人技能学习在仿真环境中虽然成本低、可并行，但构建仿真环境需要大量人工劳动——设计任务、制作相关三维资产、生成合理的场景布局、编写奖励函数等。这些繁琐步骤严重限制了机器人技能学习的可扩展性。
- **整体含义**：作者提出“生成仿真”（Generative Simulation）新范式，利用最新的基础模型（如 GPT-4、Gemini-Pro、Midjourney）自动生成多样化任务、场景和训练监督信号，使机器人能在**最小人工监督**下大规模学习技能。RoboGen 是该范式的首个具体实现，旨在“解放”机器人学习对人工数据的依赖。

## 2. 方法论：核心思想、关键技术细节

### 2.1 核心思想——自驱动“提出-生成-学习”循环

RoboGen 的工作流程分为四个阶段，全部由基础模型驱动：

1. **任务提议（Task Proposal）**  
   - 输入：一个随机采样的铰接物体（如微波炉）或一个示例任务。  
   - 利用 GPT-4 生成与该物体功能/语义相关的任务，包括任务名称、自然语言描述、所需附加物体、相关关节和连杆。  
   - 示例：给定“微波炉”，输出“加热一碗汤”，需添加“碗”和“汤”，涉及门关节和定时旋钮关节。

2. **场景生成（Scene Generation）**  
   - **资产获取**：根据任务需求，从 Objaverse 数据库中检索匹配的三维模型，或用文本生成图像（Midjourney）再转为三维模型（Zero-1-to-3）。  
   - **资产验证**：用 Gemini-Pro VLM 过滤不合适的资产。  
   - **尺寸调整**：用 GPT-4 生成符合真实世界尺寸的物体大小。  
   - **初始配置**：设置铰接物体的关节角度（如门应初始关闭），并确定物体间的空间关系（如“纸张在抽屉内”）。  
   - **碰撞避免**：用 GPT-4 指定初始位置，再通过物理检测修正碰撞。

3. **训练监督生成（Training Supervision Generation）**  
   - **任务分解**：用 GPT-4 将长程任务分解为多个子任务（sub-task）。  
   - **算法选择**：对每个子任务，让 GPT-4 从三种算法中选择最合适的：  
     - 运动规划基元（如抓取、接近、释放）  
     - 强化学习（RL，SAC）  
     - 梯度轨迹优化（用于软体操作）  
   - **奖励函数设计**：若选择 RL，让 GPT-4 编写基于低层状态的奖励函数（提供 API 如 `get_joint_state`, `get_position`）。  
   - **软体操作**：通过文本描述生成目标形状网格，以 Earth Mover 距离作为损失。

4. **技能学习（Skill Learning）**  
   - 在仿真中依次学习每个子任务：先尝试多种初始状态，记录最高奖励的终止状态作为下一子任务的初始态。  
   - 多任务通过顺序组合完成长程操作。

### 2.2 关键设计原则

- 基础模型仅用于生成**语义信息**（任务、场景描述、奖励函数模板），而不直接输出低层动作或策略。  
- 系统模块化，后端模型可替换升级（如 GPT-4 换成更强模型）。  
- 同时支持资产检索与资产生成，未来可完全生成。

## 3. 实验设计：数据集、基准与对比方法

### 3.1 使用场景/数据集

- **操作任务**：基于 PartNetMobility（铰接物体）和 Objaverse（刚性物体）构建场景。  
- **软体操作**：用 Midjourney + Zero-1-to-3 生成目标形状网格。  
- **运动任务**：四足机器人环境。

### 3.2 基准对比

对比了五个手工创建的机器人学数据集/基准：

- RLBench (James et al., 2020)  
- ManiSkill2 (Gu et al., 2023)  
- Meta-World (Yu et al., 2020)  
- Behavior-100 (Srivastava et al., 2022)  
- GenSim (Wang et al., 2023a) [并发工作，利用 LLM 生成表盘刚性物体操作]

### 3.3 评估指标

- **任务多样性**：  
  - 语义层面：Self-BLEU 分数（越低越多样）、Sentence-BERT 嵌入相似度。  
  - 图像层面：ViT 和 CLIP 嵌入相似度。  
- **场景有效性**：BLIP-2 分数（图像与文本描述匹配度），以及人工评估。  
- **训练监督有效性**：人工检查子任务分解和奖励函数合理性，以及技能学习视频。  
- **技能学习成功率**：在 50 个操作任务、7 个软体任务、12 个运动任务上统计成功比例。

### 3.4 消融实验

- 对象验证（有/无 VLM 验证）  
- 尺寸验证（有/无 GPT-4 调整）  
- 算法选择（仅 RL 对比多算法）

## 4. 资源与算力

- 论文**未明确指定 GPU 型号和数量**。  
- 训练细节：  
  - 每个 RL 子任务训练 1M 环境步；  
  - 使用 8 个线程的 CPU（2.5 GHz），每个任务平均耗时 4-5 小时；  
  - 若使用 32 核（64 线程）CPU，可并行运行 8 个作业。  
- 软体操作使用梯度优化约 300 步。  
- 总体算力需求**中等**，未大规模使用 GPU 集群。

## 5. 实验数量与充分性

- **生成任务数量**：共 155 个操作任务（表2列出），其中 106 个用于多样性比较。  
- **技能学习成功率评估**：  
  - 50 个操作任务（平均成功率 74.5%）；  
  - 7 个软体任务（平均成功率 88.6%）；  
  - 12 个运动任务（平均成功率 83.3%）。  
- **人工评估**：对 155 个任务检查场景和训练监督，发现 19 个失败（13 个场景错误、6 个奖励错误）。  
- **消融实验**：对 7 个任务比较 BLIP-2 分数，对 12 个操作任务比较仅 RL 的成功率。  

**评价**：实验覆盖了多种任务类型和算法，数量充足；对比了多个手工基准和消融版本。**公平性**：与 GenSim 的对比可能略占优势（因为 RoboGen 任务类型更多样）。但缺乏真实世界迁移实验，评估仅基于仿真。

## 6. 主要结论与发现

1. **任务多样性**：RoboGen 生成的 106 个任务在语义和图像多样性上均超过已有手工基准（Self-BLEU 最低，嵌入相似度最低）。  
2. **场景有效性**：对象验证和尺寸验证显著提升场景真实性（BLIP-2 分数更高）。  
3. **训练监督有效性**：自动生成的子任务分解和奖励函数能成功驱动技能学习（图3展示长程任务演示）。  
4. **算法选择重要性**：仅用 RL 时成功率大幅下降（12 个操作任务中大部分失败），证明多算法组合的必要性。  
5. **系统整体**：可连续产生多样化的技能演示，涵盖刚性/铰接操作、软体操作、运动技能（图1）。

## 7. 优点：方法与实验设计的亮点

- **全自动化**：从任务概念到最终策略学习，无需人工干预，可无限查询。  
- **利用基础模型语义能力**：巧妙地将 LLM/VLM 用于生成任务、场景配置和奖励函数，而避开其生成低层动作的短板。  
- **多算法混合**：根据子任务特性自动选择 RL、运动规划、轨迹优化，提高鲁棒性。  
- **场景丰富性**：资产检索与生成结合，且加入语义相关干扰物体，使场景更真实。  
- **评估全面**：从多样性、有效性、成功率多个维度评估，含人工检查。

## 8. 不足与局限

- **缺乏大规模自动化验证**：当前仍需人工检查生成的场景和奖励是否正确（19/155 失败）。未来可借助多模态模型自动反馈。  
- **仿真实域差距（Sim-to-Real）**：所有评估均在 Genesis 仿真中，未迁移到真实机器人。作者指出这仍是独立研究领域。  
- **资产依赖**：部分场景因资产功能不全（如打印机无托盘）或几何不匹配（如订书机与订书钉）而失败。  
- **奖励函数生成错误**：LLM 对铰接物体状态（开/关）的理解可能出错，导致奖励反向。  
- **实验局限性**：  
  - 未与真实机器人或最新 sim-to-real 方法对比；  
  - 软体任务仅 7 个，运动任务仅 12 个，样本量相对较小；  
  - 多样性比较中 RoboGen 任务数（106）与 Behavior-100（100）相近，但其他基准任务数较少（如 Meta-World 50），比较基数不完全一致。  
- **复杂性**：长程任务（如“丢弃厕纸”需 10 个子步骤）的成功率可能更低，文中未单独统计。

（完）
