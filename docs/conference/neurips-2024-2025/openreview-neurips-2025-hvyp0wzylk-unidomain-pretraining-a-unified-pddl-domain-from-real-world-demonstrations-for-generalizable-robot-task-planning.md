---
title: "UniDomain: Pretraining a Unified PDDL Domain from Real-World Demonstrations for Generalizable Robot Task Planning"
title_zh: UniDomain：从真实世界演示预训练统一PDDL领域以实现通用机器人任务规划
authors: "Haoming Ye, Yunxiao Xiao, Cewu Lu, Panpan Cai"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=hVYp0WzyLK"
tags: ["query:ur"]
score: 7.0
evidence: 从12393个操作视频构建统一PDDL领域，直接相关于机器人数据集构建
tldr: 现有机器人任务规划方法依赖手工定义或窄领域，泛化性受限。本文提出UniDomain，从12393个操作视频中提取原子领域，构建包含3137个操作符和2875个谓词的统一PDDL领域。在线规划时，系统为给定任务检索相关原子领域并合成规划域。实验表明该方法显著提升跨任务泛化能力，为机器人任务规划提供了可复用的知识库。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1429, \"height\": 584, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1434, \"height\": 810, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1399, \"height\": 482, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1411, \"height\": 375, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 801, \"height\": 372, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1306, \"height\": 956, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1299, \"height\": 873, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 659, \"height\": 502, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 659, \"height\": 498, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 660, \"height\": 500, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 659, \"height\": 498, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 660, \"height\": 501, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 659, \"height\": 498, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 659, \"height\": 500, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1436, \"height\": 970, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 728, \"height\": 734, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 982, \"height\": 531, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1441, \"height\": 1251, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1451, \"height\": 207, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hvyp0wzylk/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1391, \"height\": 741, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-hvyp0wzylk/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1472, \"height\": 535, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hvyp0wzylk/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1468, \"height\": 902, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hvyp0wzylk/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1474, \"height\": 367, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hvyp0wzylk/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1455, \"height\": 69, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hvyp0wzylk/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1463, \"height\": 144, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hvyp0wzylk/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1470, \"height\": 180, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hvyp0wzylk/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1481, \"height\": 546, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hvyp0wzylk/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1471, \"height\": 251, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hvyp0wzylk/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1454, \"height\": 140, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hvyp0wzylk/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1466, \"height\": 400, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hvyp0wzylk/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1469, \"height\": 279, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hvyp0wzylk/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1449, \"height\": 1742, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hvyp0wzylk/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1449, \"height\": 1777, \"label\": \"Table\"}]"
motivation: 现有方法依赖手工定义或窄领域，难以泛化到新任务场景。
method: 从大量操作视频中自动提取原子PDDL领域，聚合成统一领域，在线检索相关子领域用于规划。
result: 构建了包含3137个操作符的领域，并在多种规划任务上验证了泛化性提升。
conclusion: UniDomain通过数据驱动的方式构建可泛化的规划领域，为机器人任务规划提供了通用知识基。
---

## Abstract
Robotic task planning in real-world environments requires reasoning over implicit constraints from language and vision. While LLMs and VLMs offer strong priors, they struggle with long-horizon structure and symbolic grounding. Existing meth-
ods that combine LLMs with symbolic planning often rely on handcrafted or narrow domains, limiting generalization. We propose UniDomain, a framework that pre-trains a PDDL domain from robot manipulation demonstrations and applies it for online robotic task planning. It extracts atomic domains from 12,393 manipulation videos to form a unified domain with 3137 operators, 2875 predicates, and 16481 causal edges. Given a target class of tasks, it retrieves relevant atomics from the unified domain and systematically fuses them into high-quality meta-domains for zero-shot planning. Experiments on diverse real-world tasks show that UniDomain solves complex, unseen tasks in a zero-shot manner, achieving up to 58% higher task success and 160% improvement in plan optimality over state-of-the-art LLM and LLM-PDDL baselines.

---

## 论文详细总结（自动生成）

# 论文总结：UniDomain: Pretraining a Unified PDDL Domain from Real-World Demonstrations for Generalizable Robot Task Planning

## 1. 核心问题与整体含义（研究动机和背景）
- **问题**：真实世界中的机器人任务规划需要从自然语言指令和视觉观测中推理隐含约束（如操作前提、时序依赖、物理属性）。现有方法中，纯LLM/VLM虽然拥有常识先验，但在长程结构化和符号化推理上表现不佳；而将LLM与符号规划（如PDDL）结合的方案，往往依赖手工设计的窄领域，限制了泛化能力。
- **背景**：PDDL规划需要域定义，手工构建费时费力且难以跨任务复用。近期工作尝试用LLM从语言生成域，但质量有限；或从少量演示学习窄域，但无法支持组合泛化。
- **核心挑战**：如何从大规模真实演示中自动学习一个通用的PDDL域，使其能够零样本泛化到未见过的复杂长时任务。
- **论文整体含义**：提出UniDomain框架，首次从大量（12,393个）真实机器人操作视频中预训练一个统一的PDDL域，并通过检索与融合构建任务特定的元域，实现在线零样本规划。该方法显著提升了跨域泛化能力和规划质量。

## 2. 方法论：核心思想、关键技术细节
- **整体流程**：UniDomain分为三个阶段：
  1. **领域预训练**：从DROID数据集的12,393个演示中提取每个视频的原子PDDL域，并聚合成统一域。
  2. **领域融合**：对给定任务类，检索相关原子域，通过层次化融合构建紧凑、高质量的元域。
  3. **在线规划**：利用元域生成接地PDDL问题，由经典规划器求解得到动作序列。

- **关键技术细节**：
  - **关键帧提取**：基于灰度能量的方法，检测局部极值点，自动识别语义变化处的关键帧。公式：\( E(I_t)=\sum_{i=1}^W\sum_{j=1}^H I_t(i,j)^2 \)，滑动窗口取局部最大/最小值。
  - **封闭循环原子域生成**：对每段演示，VLM从关键帧推断算子、前提和效果，LLM进行整体修正；然后通过可解性检查（用规划器验证K个测试问题）和方案验证（用LLM检查常识合理性）迭代精炼，最多5轮。
  - **统一域**：所有原子域取并集，形成包含3,137个算子（170个语义类别）、2,875个谓词、16,481条因果边的符号知识图谱。
  - **原子域检索**：可通过人工选择或LLM推断相关动作+句子嵌入相似度自动检索。
  - **层次化融合**：将检索到的原子域按二叉树自底向上融合，每步先合并语义等价谓词（基于嵌入余弦相似度和LLM验证），再合并功能等价算子（基于名称相似度和LLM验证）。阈值τ_p=0.3，τ_o=0.3。
  - **在线规划**：使用元域，先组织谓词为四组（对象类别、状态属性、空间关系、功能关系），然后通过VLM生成初始问题提取相关谓词，再筛选相关算子（根据谓词关联），构建紧凑域，生成最终问题，由Fast Downward求解。

## 3. 实验设计：数据集/场景、基准、对比方法
- **数据集与场景**：
  - **领域预训练**：使用DROID数据集，包含12,393个真实操作演示（用于学习原子域）。
  - **评估任务**：4个未见过的任务域（BlockWorld、Desktop、Kitchen、Combination），共100个长时任务。具体包括积木排序/堆叠、抽屉/擦拭/折叠、食物工具操作、以及混合域任务。
- **基准方法**：
  - **LLM/VLM-only规划器**：Code-as-Policies、ReAct、VLM-CoT。
  - **LLM-PDDL混合方法**：ISR-LLM、VLM-PDDL、BoN-iVML。
- **评估指标**：任务成功率（SR）、成功加权路径长度（SPL）、最优率（OR，以K=2,1,0衡量接近最优程度）。同时记录推理时间和LLM调用次数。
- **评估协议**：假设完美低层控制（人类遥操作），采用半自动评估（LLM初评+专家终验），以聚焦高层的符号规划能力。

## 4. 资源与算力
- **计算资源**：
  - 关键帧提取：能量法在单线程CPU（i7-14700HX，32GB RAM）上执行，平均0.6秒/演示；对比的相似度方法（SigLIP-2）使用NVIDIA A800 GPU（80GB VRAM）。
  - 领域学习与规划：主要依赖GPT-4.1 API（温度0.0）调用，无自建训练。未明确给出总GPU训练时长或集群规模。
  - 领域融合：使用预训练语言模型（MPNet）计算嵌入，LLM进行合并验证，计算开销以API调用为主。
- **说明**：论文未详细披露统一域预训练的整体算力消耗（如VLM/LLM推理的总GPU小时数），主要依赖外部API服务。

## 5. 实验数量与充分性
- **实验数量**：
  - 主实验：在100个任务上对比7种方法，报告3个主要指标。
  - 消融实验：3组（域学习、域融合、规划方法），每组包含多个变体。
  - 额外分析：每个任务类的详细结果，失败模式分析（附录F），关键帧提取验证（附录D）。
- **充分性与公平性**：
  - 实验覆盖4个差异明显的任务域，包含组合域，体现跨域泛化。
  - 所有方法使用相同LLM（GPT-4.1）和温度设置，公平比较。
  - 消融实验逐一移除核心组件，证实每个模块的贡献。
  - 统计显著性：报告标准误差。
  - **局限性**：未在真实机器人上完整部署测试（假设完美低层执行），但提供了真实世界演示视频链接作为验证。

## 6. 主要结论与发现
- UniDomain在成功率上比最强基线（ISR-LLM）高出58%，在最优性（K=0）上提升160%，同时LLM调用次数和推理时间更低。
- 预训练的统一域通过融合原子域支持组合泛化，83%的任务生成了可行且最优的计划。
- 消融实验表明：
  - 封闭循环验证（可解性+方案检查）是原子域质量的关键；移除后成功率大幅下降。
  - 层次化融合优于直接合并或直接LLM合并（后者完全失败）。
  - 谓词分组和任务相关过滤显著提升在线规划性能，尤其在复杂组合域。
- 关键帧提取能量法高效（比相似度方法快80倍）且有效（与人工标注一致）。

## 7. 优点
- **创新性**：首次从大规模真实演示中预训练通用PDDL域，类比基础模型的预训练-后训练-推理范式。
- **数据驱动**：利用现有VLA数据，无需人工标注域或专家知识。
- **封闭循环验证**：通过规划器检查和常识验证自动提升域质量，避免人工反馈。
- **层次化融合**：解决原子域间语义不一致问题，构建紧凑有效的元域，支持组合泛化。
- **零样本泛化**：直接部署到未见任务，无需微调或额外演示。
- **效率与性能平衡**：在线规划通过谓词分组和算子过滤减少符号噪声，同时保持高质量规划。

## 8. 不足与局限
- **领域格式限制**：仅支持PDDL 1.0，不支持时序、数值、代价敏感规划，难以处理资源约束。
- **假设完全可观测**：忽略真实世界的遮挡、传感器噪声等问题，未采用概率规划框架（如PPDDL/RDDL）。
- **融合开销**：自动检索的原子域可能冗余，导致融合过程耗时；未来需优化检索与融合效率。
- **低层控制假设**：实验假设完美执行（人类遥操作），未在真实机器人上端到端验证高层的规划实际执行效果（虽有视频示例但非系统评估）。
- **通用域规模**：3k+算子、2.8k+谓词对LLM/VLM的显式建模仍有挑战，检索与融合的准确性可能影响泛化极限。
- **数据集依赖**：基于DROID的厨房/桌面操作，可能不完全覆盖所有机器人任务类型（如导航、装配）。

（完）
