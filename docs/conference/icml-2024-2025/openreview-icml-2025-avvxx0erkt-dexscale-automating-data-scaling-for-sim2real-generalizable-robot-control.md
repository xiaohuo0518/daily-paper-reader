---
title: "DexScale: Automating Data Scaling for Sim2Real Generalizable Robot Control"
title_zh: DexScale：自动化数据缩放实现Sim2Real可泛化机器人控制
authors: "Guiliang Liu, Yueci Deng, Runyi Zhao, Huayi Zhou, Jian Chen, Jietao Chen, Ruiyan Xu, Yunxin Tai, Kui Jia"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=AVVXX0erKT"
tags: ["query:ur"]
score: 8.0
evidence: 用于扩展机器人训练数据集的数据引擎
tldr: 针对机器人数据采集成本高、仿真数据与现实差距大的问题，提出DexScale数据引擎，自动模拟和缩放机器人操作技能，生成可部署的策略。通过集成仿真与真实数据，验证了该方法在Sim2Real泛化中的有效性，为构建大规模机器人数据集提供了可复用的自动化方案。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 805, \"height\": 450, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1604, \"height\": 593, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 852, \"height\": 294, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1757, \"height\": 624, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 681, \"height\": 504, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 847, \"height\": 1717, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1775, \"height\": 974, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1730, \"height\": 612, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1758, \"height\": 621, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1729, \"height\": 605, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-avvxx0erkt/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1730, \"height\": 610, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-avvxx0erkt/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 835, \"height\": 435, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-avvxx0erkt/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1068, \"height\": 421, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-avvxx0erkt/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1638, \"height\": 239, \"label\": \"Table\"}]"
motivation: 机器人泛化控制需要大规模数据集，但真实数据采集昂贵，仿真数据与现实存在差距。
method: 提出DexScale数据引擎，自动模拟机器人技能并缩放数据，结合仿真与真实环境进行学习。
result: 在多种机器人操作任务上验证了Sim2Real泛化能力的提升。
conclusion: DexScale为自动化构建可泛化机器人数据集提供了高效方法。
---

## Abstract
A critical prerequisite for achieving generalizable robot control is the availability of a large-scale robot training dataset. Due to the expense of collecting realistic robotic data, recent studies explored simulating and recording robot skills in virtual environments. While simulated data can be generated at higher speeds, lower costs, and larger scales, the applicability of such simulated data remains questionable due to the gap between simulated and realistic environments. To advance the Sim2Real generalization, in this study, we present DexScale, a data engine designed to perform automatic skills simulation and scaling for learning deployable robot manipulation policies. Specifically, DexScale ensures the usability of simulated skills by integrating diverse forms of realistic data into the simulated environment, preserving semantic alignment with the target tasks. For each simulated skill in the environment, DexScale facilitates effective Sim2Real data scaling by automating the process of domain randomization and adaptation. Tuned by the scaled dataset, the control policy achieves zero-shot Sim2Real generalization across diverse tasks, multiple robot embodiments, and widely studied policy model architectures, highlighting its importance in advancing Sim2Real embodied intelligence.

---

## 论文详细总结（自动生成）

# 论文中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：机器人控制策略的泛化需要大规模训练数据，但真实数据采集成本高、耗时长；仿真数据虽然可无限生成，但因仿真与现实环境之间的语义不匹配和模拟偏差（Sim2Real gap）导致学到的策略难以直接部署。
- **研究动机**：现有方法（如MimicGen、RoboGen）依赖手工领域随机化或需要真实数据微调，缺乏自动化、可扩展的Sim2Real数据生成引擎。DexScale旨在解决这一矛盾，实现零样本的Sim2Real泛化。
- **整体含义**：构建一个自动化数据引擎，将真实世界观测（如人类视频、场景图像）投影到仿真环境，并通过自动领域随机化和领域适应生成多样化训练数据，使控制策略能在多任务、多机器人平台上零样本部署。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：将真实世界数据（场景和动作轨迹）投影到仿真环境，再利用自动化的领域随机化（DR）和领域适应（DA）生成大规模、多样化的技能数据集，使得模仿学习的策略能够跨领域泛化。
- **关键技术细节**：
  - **异构数据投影**：
    - **场景投影**：从RGB图像中提取物体信息，匹配到3D资产集（如Objaverse-XL）中的“数字表亲”，构建静态环境；支持手动调整。
    - **动作-轨迹投影**：从人类操作视频中检测手部运动，重定向到机器人末端执行器（如夹爪），并联合优化物体与末端执行器的3D位姿，确保物理交互合理性。
  - **环境仿真**：
    - **场景仿真**：基于投影结果，利用大语言模型（如GPT-4）自动配置完整场景（物体布局、背景等）。
    - **动作轨迹仿真**：基于投影的末端位姿，通过逆运动学（IK）和轨迹规划（如RRT-Connect）生成连续动作；若无可投影动作，则利用LLM自动设计奖励函数，结合强化学习获取技能。
  - **Sim2Real数据缩放**：
    - **自动领域随机化（ADR）**：区分**动作不变DR（AI-DR）**（不影响最优动作，如光照）和**语义感知DR（SA-DR）**（需要策略适应，如物体形状），利用大模型对DR特征排序，并通过ADR算法自动更新DR参数分布。
    - **领域适应（DA）**：将观测映射到面向物体的表示（如点云）或姿态-可供性表示，减少背景等无关特征的影响。
  - **部署**：基于缩放后的数据集（D_DR+AR）训练模仿学习策略（如ACT、扩散策略、VLA模型），实现零样本Sim2Real部署。

## 3. 实验设计：数据集、场景、基准与对比方法

- **任务与场景**：四个挑战性任务——物体抓取、纸箱操作（开箱）、双手机器人餐具重排、倒水。
- **机器人平台**：单臂机器人（Rokae SR3、AUBO I5）和双臂机器人（WidowX 250 S）。
- **基准对比**：
  - 在8种Sim2Real间隙（光照、物体纹理、桌面纹理、背景、干扰物、相机位置、相机朝向、视野）下，对比**仅技能数据集**、**技能+DR**、**技能+DA** 和完整**DexScale**。
  - 与**手工DR**（基于经验排名前3的特征）进行对比。
- **策略架构**：Transformer策略（ACT）、扩散策略（Diffusion Policy）、视觉-语言-动作模型（RDT-1B）。
- **消融实验**：分别移除DR和DA组件，比较在仿真（100次）和真实（10次）环境中的成功率。

## 4. 资源与算力

- **明确说明**：
  - 物体抓取：4× NVIDIA A800 GPU，训练36小时。
  - 开箱任务：单张 NVIDIA A100 GPU，训练48小时。
  - 餐具重排：单张 NVIDIA A100 GPU，训练迭代40k次。
- **未说明**：未给出手工DR对比实验的具体算力消耗。

## 5. 实验数量与充分性

- **实验数量**：
  - 泛化性实验：针对10种领域间隙（8种静态+2种动态），每种间隙在仿真中100次试验、真实中10次试验，共约1000+次仿真试验和100次真实试验。
  - 可扩展性实验：覆盖4种任务×3种策略架构×3种机器人平台。
  - 消融实验：对比3种数据配置（仅技能、+DR、+DA）与完整DexScale。
- **充分性与客观性**：
  - 实验设计较全面，覆盖了典型间隙、多种任务和机器人本体。
  - 手工DR对比实验仅测试了3种特征，且每次只增加一种，未能探索组合效果，对比不够彻底。
  - 真实环境试验次数较少（每设置10次），统计可靠性有限。
  - 未报告不同随机种子下的方差，可能影响结论稳健性。

## 6. 论文的主要结论与发现

- DexScale能有效桥接Sim2Real间隙，在8种静态间隙和2种动态间隙下，完整DexScale的成功率显著高于仅技能或仅DR/DA的数据集。
- 自动化DR优于手工选择DR（手工DR真实成功率0.56 vs DexScale的0.40-0.60不等），尤其在多间隙组合下优势明显。
- DexScale可扩展至不同策略架构（变压器、扩散、VLA）和多种机器人平台，实现零样本部署。
- 场景投影和动作投影能够将真实世界信息有效复用到仿真环境中，保证语义一致性。

## 7. 优点：方法或实验设计上的亮点

- **方法论亮点**：提出了AI-DR和SA-DR的明确区分，并利用LLM自动化DR特征排序和参数分布学习，减少人工依赖。
- **数据投影**：将人类视频的动作和场景自动映射到仿真，降低了数据采集门槛。
- **实验设计亮点**：跨任务、跨机器人、跨策略架构的全面评估，验证了方法的通用性。
- **开源与可复现性**：提供了项目网页和实现细节（附录A.3详述了训练配置）。

## 8. 不足与局限

- **实验覆盖不足**：
  - 真实环境试验次数少（每设置10次），统计显著性未检验。
  - 仅测试了4种任务，未涉及长时任务或人形机器人等复杂场景。
  - 对抗干扰物（distractors）的实验中，真实成功率仅0.4，仍有较大差距。
- **偏差风险**：DexScale依赖预训练的大模型（如GPT-4、SAM2）进行场景生成和DR特征排序，可能引入这些模型的固有偏差。
- **应用限制**：动作投影依赖于高质量的人类视频和3D重建，在低质量视频或遮挡场景下可能失效；领域适应中的点云提取需要精确的掩码，在真实环境中的鲁棒性未充分验证。
- **可扩展性局限**：当前支持单臂/双臂，但未延伸至人形机器人；长时任务（如做饭）的自动分解和奖励设计尚未解决。

（完）
