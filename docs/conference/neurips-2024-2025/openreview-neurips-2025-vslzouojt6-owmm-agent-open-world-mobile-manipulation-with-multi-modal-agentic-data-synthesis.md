---
title: "OWMM-Agent: Open World Mobile Manipulation With Multi-modal Agentic Data Synthesis"
title_zh: OWMM-Agent：基于多模态智能数据合成的开放世界移动操作
authors: "Junting Chen, Haotian Liang, Lingxiao Du, Weiyun Wang, Mengkang Hu, Yao Mu, Wenhai Wang, Jifeng Dai, Ping Luo, Wenqi Shao, Lin Shao"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=vSLzoUoJt6"
tags: ["query:ur"]
score: 7.0
evidence: 用于机器人操作的多模态智能数据合成
tldr: 开放世界移动操作面临开放指令和环境泛化挑战，以及系统集成的复杂性。本文提出多模态智能体架构，维护多视角场景帧和智能体状态进行决策，并通过函数调用控制机器人。针对领域迁移导致的幻觉问题，提出多模态数据合成方法以增强智能体性能。实验表明该方法在多种开放世界任务中表现优异。该工作为机器人数据集构建和智能体决策提供了创新方案。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-vslzouojt6/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1243, \"height\": 687, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vslzouojt6/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1364, \"height\": 804, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vslzouojt6/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1280, \"height\": 589, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vslzouojt6/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1405, \"height\": 418, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vslzouojt6/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 829, \"height\": 522, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vslzouojt6/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1399, \"height\": 368, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vslzouojt6/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1411, \"height\": 1655, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vslzouojt6/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1433, \"height\": 2047, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1455, \"height\": 885, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1426, \"height\": 369, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1459, \"height\": 413, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1405, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1455, \"height\": 797, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1535, \"height\": 392, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1463, \"height\": 377, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1508, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 906, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vslzouojt6/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 907, \"height\": 210, \"label\": \"Table\"}]"
motivation: 开放世界移动操作需要应对开放指令和环境的泛化，以及高低层控制的系统集成困难。
method: 提出多模态智能体架构，融合多视角场景理解与函数调用，并利用数据合成缓解领域迁移幻觉。
result: 在多个开放世界任务中验证了方法的有效性，提升了泛化能力。
conclusion: 该工作通过智能体架构和数据合成推进了开放世界移动操作的发展。
---

## Abstract
The rapid progress of navigation, manipulation, and vision models has made mobile manipulators capable in many specialized tasks. 
However, the open-world mobile manipulation (OWMM) task remains a challenge due to the need for generalization to open-ended instructions and environments, as well as the systematic complexity to integrate high-level decision making with low-level robot control based on both global scene understanding and current agent state. To address this complexity, we propose a novel multi-modal agent architecture that maintains multi-view scene frames and agent states for decision-making and controls the robot by function calling.
A second challenge is the hallucination from domain shift. To enhance the agent performance, we further introduce an agentic data synthesis pipeline for the OWMM task to adapt the VLM model to our task domain with instruction fine-tuning. We highlight our fine-tuned OWMM-VLM as the first dedicated foundation model for mobile manipulators with global scene understanding, robot state tracking, and multi-modal action generation in a unified model. Through experiments, we demonstrate that our model achieves SOTA performance compared to other foundation models including GPT-4o and strong zero-shot generalization in real world.
The project page is at https://hhyhrhy.github.io/owmm-agent-project.

---

## 论文详细总结（自动生成）

# OWMM-Agent：基于多模态智能数据合成的开放世界移动操作——论文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **研究动机**：开放世界移动操作（OWMM）要求机器人能理解开放的自然语言指令，在未见过、非结构化的环境中完成任务。现有方法（如基于语义地图或3D语义场的检索）受限于嵌入模型的表达能力，难以处理复杂组合指令，且需要耗时的3D重建。同时，直接将预训练VLM应用于机器人存在领域迁移导致的幻觉问题：罕见的地面任务（如检测可行区域）、状态跟踪、先验知识缺失等。
- **整体含义**：这项工作旨在构建一个统一的VLM智能体架构，使其具备全局场景理解、状态跟踪和端到端动作生成能力，从而实现真正的开放世界移动操作。

## 2. 方法论：核心思想、关键技术细节
- **核心思想**：不依赖详细的3D几何表示，利用VLM强大的视觉-语言基础能力，将OWMM任务建模为多轮、多图像、多模态推理问题。VLM端到端生成思维链、跟踪智能体状态和带有坐标的多模态动作，智能体通过函数调用调用路径规划器和运动规划器执行动作。
- **关键技术细节**：
  - **OWMM-Agent框架**：维护长期环境记忆（预映射阶段获取的带位姿的场景图像）和瞬态机器人状态记忆（文本摘要）。VLM（OWMM-VLM）接收任务指令、多视图图像、当前自我中心图像和历史记录，输出四种高层的多模态动作：搜索场景帧、导航到点、拾取、放置。每个动作包含坐标（边界框中心）和语义信息。
  - **OWMM-VLM模型**：基于InternVL-2.5微调，包含ViT（冻结）、2层投影MLP和LLM（可训练）。输入包括任务指令、多场景帧（8个+1个自我中心帧），输出结构化JSON：包含思维链推理（任务理解、感知、决策、摘要）和动作信息。
  - **智能数据合成流水线**：利用Habitat仿真环境，通过PDDL任务规划生成符号任务序列，机器人执行记录轨迹，关键帧筛选（导航可见性、操作可达性），最后用GPT-4o mini改写注释以增强语言多样性。生成的训练数据包括57.2万条注释（拾取64.7K、放置68.9K、导航59.6K、场景搜索378.8K）。

## 3. 实验设计
- **数据集/场景**：训练使用HSSD中的143个场景，157个操作对象（YCB Objects + Google Scanned Objects），1471个容器。训练/测试场景比例113:30，对象比例137:20（测试集对象完全未见）。生成共21,046个有效情节，约572K注释。
- **Benchmark**：基于HomeRobot框架改造，使用Fetch机器人（模拟器和真实）。评估指标：单步评估（自我中心决策准确率、图像检索准确率、三个子任务的附带评分），情节评估（完整任务成功率、子任务成功率、死循环计数），真实世界评估（动作正确性、附带准确性、可达性）。
- **对比方法**：
  - 通用VLM：GPT-4o、InternVL2.5（8B）
  - 模块化智能体：GPT-4o + PIVOT、GPT-4o + RoboPoint
  - 消融变体：无思维链、输出坐标而非边界框、束搜索等。
- **实验设置**：单步评估测试约4K样本，情节评估测试308个情节，真实世界评估10个样本。

## 4. 资源与算力
- **训练资源**：
  - OWMM-VLM-8B：在8块NVIDIA A100 GPU上训练约7小时（1 epoch）。
  - OWMM-VLM-38B：在24块NVIDIA A100 GPU上训练约18小时（1 epoch）。
- **推理资源**：8B模型单步推理约4.84秒（8+1帧），占用18.43 GB显存（单A100-40G）；38B模型在4×A100-40G上推理约4.39秒（8+1帧），显存约98.22 GB。
- **注意**：论文未提及训练整个数据集的总GPU小时数（仅给出单次训练时长）。

## 5. 实验数量与充分性
- **实验数量**：
  - 单步评估：覆盖5个指标，对比4种基线方法+2种模块化方法。
  - 情节评估：5个关键指标（全任务、子任务、死循环），严格和宽松两种阈值。
  - 真实世界评估：10个样本，对比2种基线。
  - 消融实验：6组（推理格式、束搜索、思维链、数据规模、数据多样性）。
  - 数据扩展实验：5个数据规模（0k~152k），2组多样性对比（场景/对象缺失）。
  - 失效模式分析：100个失败情节，手动分类。
  - 推理效率分析：8帧、16帧等多帧配置。
- **充分性与公平性**：实验设计较为系统，涵盖了基本能力评估和真实部署测试。对比方法包括当前最强的通用VLM（GPT-4o）和专用机器人模型（PIVOT、RoboPoint），且对基线做了适应性调整（如单图像任务重定义）。但真实世界实验样本较少（10个），且需要人工确认，存在一定偏差风险。

## 6. 主要结论与发现
- **性能优势**：OWMM-VLM-38B在单步评估中全面超越所有基线（总体准确率97.85%，图像检索87.54%）；情节评估中全任务成功率达21.9%（严格阈值）/51.52%（宽松阈值），远超GPT-4o+PIVOT（0.33%~1.68%）和GPT-4o+RoboPoint（0.33%~3.03%），且无死循环故障。
- **零样本泛化**：仅在仿真数据上微调的模型在真实Fetch机器人上取得90%单步成功率，体现强跨域泛化能力。
- **数据关键性**：数据规模对性能提升呈对数增长，但场景/对象多样性影响较小（5%波动内），说明核心瓶颈在于数据量而非多样性。
- **设计必要性**：边界框输出优于坐标点；思维链推理对状态跟踪和决策至关重要；束搜索可小幅提升准确性但增加延迟。

## 7. 优点
- **统一架构**：将全局场景理解、状态跟踪、动作生成整合到单一VLM中，无需多个模型协调，降低系统复杂度。
- **思路创新**：利用2D图像代替3D重建进行全局推理，在机器人接近目标时才使用深度信息，平衡了效率与精度。
- **自动化数据合成**：PDDL规划+仿真执行+GPT-4o改写的流水线大幅降低人工标注成本，能产出高质量、结构化的思维链注释。
- **系统性实验**：覆盖单步、情节、真实场景，包含消融、数据律、失效分析，论证充分。
- **可解释性**：生成的思维链包含任务推理、感知、决策和摘要，便于调试和故障诊断。

## 8. 不足与局限
- **依赖预映射**：仍然需要预映射阶段（建图+相机位姿图），限制了在完全未知环境下的自主性。
- **操作能力受限**：主要支持吸盘式抓取，无法处理复杂末端执行器（如灵巧手）的精细操作。
- **跨本体泛化问题**：模型学习了特定机器人（Fetch）的运动学先验（如最大臂展），直接迁移到其他机器人会导致失败。
- **真实实验样本少**：仅10个真实场景测试，统计显著性不足；且因安全原因需要人工确认，并非完全自主运行。
- **评估偏差**：情节成功率较低（21.9%严格），主要瓶颈在于操作阶段（拾取/放置成功率仅38.56%），说明对该子任务的支持仍有较大提升空间。
- **推理时延**：38B模型约4秒/步，难以满足高频控制需求，未来需结合压缩或量化优化。

（完）
