---
title: "Dynamic Test-Time Compute Scaling in Control Policy: Difficulty-Aware Stochastic Interpolant Policy"
title_zh: 控制策略中的动态测试时计算缩放：难度感知的随机插值策略
authors: "Inkook Chun, Seungjae Lee, Michael Samuel Albergo, Saining Xie, Eric Vanden-Eijnden"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=oDoPiR8wZJ"
tags: ["query:ur"]
score: 6.0
evidence: 自适应推理计算以提升边缘部署效率
tldr: 扩散策略在机器人控制中性能优异，但固定推理预算导致低效或欠佳。本文提出DA-SIP，通过难度分类器动态调整积分步数，在每步控制中自适应分配计算资源，提升了长时域操作任务的效率，对边缘部署有潜在价值。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-odopir8wzj/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1435, \"height\": 381, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-odopir8wzj/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1449, \"height\": 470, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-odopir8wzj/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1391, \"height\": 816, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1326, \"height\": 278, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1483, \"height\": 420, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 379, \"height\": 317, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 399, \"height\": 369, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 569, \"height\": 351, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1431, \"height\": 433, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1310, \"height\": 396, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1188, \"height\": 395, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1144, \"height\": 346, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1361, \"height\": 455, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1270, \"height\": 420, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1441, \"height\": 298, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1415, \"height\": 803, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1438, \"height\": 255, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1415, \"height\": 570, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1370, \"height\": 705, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1351, \"height\": 531, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1432, \"height\": 895, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1117, \"height\": 391, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 804, \"height\": 312, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1013, \"height\": 354, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1441, \"height\": 391, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 556, \"height\": 276, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-odopir8wzj/table-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 588, \"height\": 275, \"label\": \"Table\"}]"
motivation: 现有扩散策略使用固定推理预算，无法根据任务复杂度灵活调整，导致资源浪费。
method: 引入难度感知的随机插值策略，通过RGB-D观测分类器动态选择积分步数。
result: 在仿真操纵任务中，DA-SIP在保持性能的同时显著减少计算量。
conclusion: 自适应计算缩放能够提升机器人控制策略的效率。
---

## Abstract
Diffusion- and flow-based policies deliver state-of-the-art performance on long-horizon robotic manipulation and imitation-learning tasks. However, these controllers employ a fixed inference budget at every control step, regardless of task complexity, leading to computational inefficiency for simple subtasks while potentially underperforming on challenging ones. To address these issues, we introduce Difficulty-Aware Stochastic Interpolant Policy (DA-SIP), a framework that enables robotic controllers to adaptively adjust their integration horizon in real-time based on task difficulty. Our approach employs a difficulty classifier that analyzes RGB-D observations to dynamically select the step budget, the optimal solver variant, and ODE/SDE integration at each control cycle. DA-SIP builds upon the stochastic interpolant formulation to provide a unified framework that unlocks diverse training and inference configurations for diffusion- and flow-based policies. Through comprehensive benchmarks across diverse manipulation tasks, DA-SIP achieves 2.6-4.4× reduction in total computation time while maintaining task-success rates comparable to fixed maximum-computation baselines. By implementing adaptive computation within this framework, DA-SIP transforms generative robot controllers into efficient, task-aware systems that intelligently allocate inference resources where they provide the greatest benefit.

---

## 论文详细总结（自动生成）

# 论文总结：Dynamic Test-Time Compute Scaling in Control Policy (DA-SIP)

## 1. 核心问题与整体含义
- **研究动机**：现有的扩散模型和流匹配策略在机器人模仿学习中取得了最优性能，但它们采用**固定的推理预算**（固定的步数、求解器、ODE/SDE模式）执行每个控制周期。这导致简单子任务（如空载移动）浪费计算资源，而困难子任务（如亚毫米级放置）可能因预算不足而性能下降。
- **整体含义**：受大语言模型中“自适应思考步数”的启发，本文提出在机器人控制策略中也实现**难度感知的自适应计算**，在推理时动态分配计算资源，从而在保持任务成功率的同时大幅降低总计算开销。

## 2. 方法论：核心思想、关键技术细节
- **核心思想**：利用随机插值（Stochastic Interpolant, SI）框架统一扩散策略和流策略，并附加一个**难度分类器**，在每个控制周期根据当前RGB-D观测预测难度级别，然后动态选择推理配置三元组（步数、求解器类型、ODE/SDE模式）。
- **关键技术细节**：
  - **随机插值框架**：定义插值过程 \( I_t = \alpha_t x^* + \sigma_t \epsilon \)，学习速度场 \( v(x,t,o) = \mathbb{E}[\dot{I}_t | I_t=x, o] \) 或得分函数 \( s(x,t,o) \)。通过损失函数 \( L_v = \mathbb{E}[|\hat{v}(I_t,t,o) - \dot{I}_t|^2] \) 训练网络。支持多种插值方式（Linear、VP、GVP），且训练后可在ODE与SDE之间切换。
  - **难度分类器**：三种实现：
    1. **轻量CNN**（ResNet-18）：在300张标注图像上训练，推理约20ms。
    2. **少样本VLM**：使用Qwen-VL等模型，提示1-3张示例图像，无需训练，推理500-1000ms。
    3. **微调VLM**：对Qwen2.5-VL进行LoRA微调（8-12轮），推理约300-400ms。
  - **自适应分配**：难度级别d∈{1,2,3}映射到三元组：
    - 简单（d=1）：5步，Euler，ODE
    - 中等（d=2）：10步，Heun，ODE
    - 困难（d=3）：20步，RK4，SDE
    - 更细粒度版本（6类）见表3，包括初始、接近、抓取、随机尝试、连续推、结束等状态及其对应配置。
- **算法流程**：训练阶段选择插值和预测目标（velocity/score）训练统一策略网络；部署阶段：观察→难度分类器→选择配置→执行SI逆过程生成动作。

## 3. 实验设计
- **数据集/场景**：
  - **仿真环境**：RoboMimic（Can、Lift、Square、Tool Hang）、Block Push（Fetch）、Push-T、Kitchen、Multimodal Ant，涵盖简单到复杂的操纵与运动任务。
  - **难度标注**：从8名标注员收集约20,000个状态，分为6类（I、N、G、S、C、E），通过多数投票确定最终标签。
- **基准方法**：
  - 固定最大计算（最大步数、最优求解器）
  - 固定最小计算（1步、Euler、ODE）
  - 不同分类器（CNN、Few-shot VLM、Fine-tuned VLM）
  - 标准Diffusion Policy（DDPM、DDIM）作为策略基线。
- **对比指标**：任务成功率、计算时间（秒）、计算缩减倍数。

## 4. 资源与算力
- **训练资源**：策略网络在**NVIDIA L40S GPU**上训练（Table 1脚注），每个配置训练5,000 epoch，3个随机种子，每50 epoch保存检查点。**未明确说明使用的GPU数量及总训练时长**。
- **VLM微调**：使用8-bit量化、LoRA（rank 16/8），在单GPU上微调12 epoch（附录A.4）。
- **推理资源**：轻量CNN约20ms，VLM类约300-1000ms（表17）。

## 5. 实验数量与充分性
- **实验数量**：非常充分。
  - 在8个任务上评估，每个任务测试多种配置（步数从1到100、求解器Euler/Heun/RK4、ODE/SDE模式）。
  - 分类器消融：对比CNN、Few-shot VLM、微调VLM，并测试不同数据量（表16）、不同噪声水平（表19）、不同示例数（表18）。
  - 策略基线对比：与标准Diffusion Policy（DDPM/DDIM）在多个步数下比较（附录B）。
  - 真实机器人数据初步验证（push T的MSE，表20）。
- **客观性与公平性**：实验设计严格，每组配置采用3训练种子×3推理种子=9次运行，报告最后10个检查点的平均成功率（每检查点50 episode）。基线方法在相同设置下复现。**总体客观公平，但所有主要实验均在仿真中进行，真实机器人部署仅有MSE指标而无实际 rollout**。

## 6. 主要结论与发现
1. **自适应计算效率高**：DA-SIP在6个任务上实现平均2.6-4.4×计算缩减，成功率损失平均仅1.3%~4.7%（CNN分类器损失最小）。
2. **不同任务需要不同最优配置**：简单任务（Lift、Can）1步即达100%；精确任务（Push-T、Block Push）需要Heun+SDE+多步；探索性任务（Tool Hang）在中等步数（50）最优，过多步数反而下降。
3. **轻量CNN是最佳分类器**：准确率最高（约80-95%）、推理延迟最低，且对噪声鲁棒（σ=0.3时仅降3%）。
4. **微调VLM平衡性能与灵活性**：虽准确率低于CNN，但无需从零训练，且能在少样本基础上显著提升。
5. **统一SI框架的优越性**：支持训练后切换求解器、步数、模式，无需重新训练。

## 7. 优点
- **创新性**：将自适应计算从NLP引入机器人生成策略，且基于统一的理论框架（SI），非启发式。
- **综合性**：同时调整步数、求解器和ODE/SDE三种维度，提供了完整的设计空间探索。
- **实用性**：轻量CNN分类器计算开销极低（20ms），适合实时控制；微调VLM分离注灵活性。
- **稳健性**：分类器对噪声和部分数据具备鲁棒性（附录D.4、D.1）。
- **评估充分**：涵盖多种复杂度任务，大量消融实验和基线对比。

## 8. 不足与局限
- **仿真为主**：所有主要成功率实验均在仿真环境，真实机器人部署仅测试了action MSE（附录D.5），缺少实际闭环rollout验证，存在sim-to-real gap风险。
- **人工标注依赖**：难度分类需要人工标注大量状态（~20,000），标注成本较高，且类别定义依赖专家经验。
- **VLM分类器准确率较低**：即使微调后，平均准确率仅约50-60%（表2），对策略端到端性能可能引入偏差。
- **未考虑安全约束**：论文提到未来可与安全监控结合，但当前框架未处理接触丰富任务的危险情况。
- **算力报告不完整**：未明确训练总时长、GPU数量、能耗等，影响可重复性和成本评估。
- **仅用单一网络架构**（U-Net transformer），未验证对其他骨干（如Diffusion Policy的CNN）的通用性。

（完）
