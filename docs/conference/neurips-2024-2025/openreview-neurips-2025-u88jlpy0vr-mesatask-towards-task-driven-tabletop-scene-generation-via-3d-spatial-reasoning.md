---
title: "MesaTask: Towards Task-Driven Tabletop Scene Generation via 3D Spatial Reasoning"
title_zh: MesaTask：通过3D空间推理实现面向任务的桌面场景生成
authors: "Jinkun Hao, Naifu Liang, Zhen Luo, Xudong XU, Weipeng Zhong, Ran Yi, Yichen Jin, Zhaoyang Lyu, Feng Zheng, Lizhuang Ma, Jiangmiao Pang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=U88JlpY0vR"
tags: ["query:ur"]
score: 7.0
evidence: 面向任务的桌面场景大规模数据集生成
tldr: 该论文提出MesaTask-10K，一个包含约10700个合成桌面场景的大规模数据集，通过3D空间推理生成任务相关布局。解决了传统手动布局耗时且与任务对齐不佳的问题。该数据集可用于训练机器人理解指令并执行操作任务，其生成方法论可推广到其他机器人场景数据集构建。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-u88jlpy0vr/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1441, \"height\": 754, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-u88jlpy0vr/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1422, \"height\": 711, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-u88jlpy0vr/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1419, \"height\": 772, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-u88jlpy0vr/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1447, \"height\": 635, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-u88jlpy0vr/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1431, \"height\": 679, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-u88jlpy0vr/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1372, \"height\": 749, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-u88jlpy0vr/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1435, \"height\": 728, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-u88jlpy0vr/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1418, \"height\": 1216, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-u88jlpy0vr/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 664, \"height\": 331, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-u88jlpy0vr/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1423, \"height\": 412, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-u88jlpy0vr/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1451, \"height\": 2195, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-u88jlpy0vr/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1411, \"height\": 1818, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-u88jlpy0vr/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1410, \"height\": 1905, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-u88jlpy0vr/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1410, \"height\": 1780, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-u88jlpy0vr/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1456, \"height\": 478, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-u88jlpy0vr/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1444, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-u88jlpy0vr/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1380, \"height\": 923, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-u88jlpy0vr/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1243, \"height\": 321, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-u88jlpy0vr/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1431, \"height\": 185, \"label\": \"Table\"}]"
motivation: 机器人需要任务相关的训练场景，但手动设计耗时且随机布局缺乏合理性。
method: 基于3D空间推理，从高层任务指令自动生成场景物体布局。
result: 构建了包含10700个场景的数据集，场景与任务指令对齐。
conclusion: 该方法可提升机器人任务理解能力，并为场景数据集构建提供新范式。
---

## Abstract
The ability of robots to interpret human instructions and execute manipulation tasks necessitates the availability of task-relevant tabletop scenes for training. However, traditional methods for creating these scenes rely on time-consuming manual layout design or purely randomized layouts, which are limited in terms of plausibility or alignment with the tasks. In this paper, we formulate a novel task, namely task-oriented tabletop scene generation, which poses significant challenges due to the substantial gap between high-level task instructions and the tabletop scenes. To support research on such a challenging task, we introduce \textbf{MesaTask-10K}, a large-scale dataset comprising approximately 10,700 synthetic tabletop scenes with \emph{manually crafted layouts} that ensure realistic layouts and intricate inter-object relations. To bridge the gap between tasks and scenes, we propose a \textbf{Spatial Reasoning Chain} that decomposes the generation process into object inference, spatial interrelation reasoning, and scene graph construction for the final 3D layout. We present \textbf{MesaTask}, an LLM-based framework that utilizes this reasoning chain and is further enhanced with DPO algorithms to generate physically plausible tabletop scenes that align well with given task descriptions. Exhaustive experiments demonstrate the superior performance of MesaTask compared to baselines in generating task-conforming tabletop scenes with realistic layouts.

---

## 论文详细总结（自动生成）

### 论文核心问题与整体含义（研究动机和背景）

- **研究动机**：机器人执行人类指令需要任务相关的桌面场景进行训练。传统手动布局设计耗时且多样性受限，纯随机布局缺乏合理性和任务对齐性。因此，自动从高层任务指令生成物理合理的桌面场景成为关键问题。
- **核心问题**：如何弥合高层任务描述与具体3D场景布局之间的巨大鸿沟，同时保证场景的交互性、真实性和复杂物体间关系（如堆叠、包含）。
- **本文贡献**：
    - 首次定义“任务驱动桌面场景生成”任务。
    - 构建大规模数据集 **MesaTask-10K**（约10,700个合成桌面场景，包含12,000+ 3D资产，6种常见桌面类型，手工精修布局）。
    - 提出基于LLM的框架 **MesaTask**，通过**空间推理链**和**直接偏好优化（DPO）** 生成符合任务指令的物理合理场景。

### 方法论

- **核心思想**：利用空间推理链将任务到场景的生成分解为结构化推理步骤，并借助LLM（Qwen3-8b）通过SFT和DPO训练实现端到端布局生成。
- **关键技术细节**：
    1. **空间推理链**：
        - 步骤1：**对象推理**——根据任务相关物体补全完整物体列表。
        - 步骤2：**空间关系推理**——基于任务和物体共现模式推理物体间空间关系（用自然语言描述）。
        - 步骤3：**场景图构建**——以物体为节点、关系为边形成场景图，并进一步量化每个物体的粗位置（3×3网格）和朝向（8方向离散）。
    2. **训练数据构建**：
        - 利用MesaTask-10K中每个场景的3D布局，自动提取场景图（通过几何规则确定左右、前后、包含等关系）。
        - 使用MLLM（GPT-4o）结合场景渲染图和场景图，生成详细的场景描述、任务指令及完整推理链（对象列表+关系+场景图）。
    3. **LLM训练**：
        - **SFT阶段**：使用50,000个任务-场景对（每个场景生成5条任务）进行全参数微调，注入3D空间推理能力。
        - **DPO阶段**：为缓解SFT后的物体碰撞、任务相关物体遗漏、关系错误等问题，构造正负样本对：
            - 正样本：来自MesaTask-10K的原始布局。
            - 负样本：通过三种方式随机破坏正样本获得——几何扰动（诱发碰撞）、关系损坏（改变关系类型）、关键物体删除。
        - DPO优化目标：最大化正样本相对于负样本的偏好对数概率。
    4. **后处理**：根据生成的布局从3D资产库中检索最匹配的物体（结合文本相似度和尺寸相似度，权重α=0.9, β=0.1），放入物理模拟器验证无碰撞。
- **算法流程**（文字描述）：
    - 输入：任务指令T → 通过GPT-4o提取环境E、子目标G、任务相关物体O。
    - 空间推理链：LLM基于[E,G,O]依次输出完整物体列表V、关系描述E、场景图G(V,E)。
    - 从场景图生成最终3D布局L（各物体的位置、尺寸、旋转、描述）。
    - 3D资产检索与放置，得到最终场景S。

### 实验设计

- **数据集与基准**：
    - **训练集**：MesaTask-10K的10,000个场景，每个场景生成5条任务，共50,000对。
    - **DPO数据集**：5,000个未见场景，每个构造约2个负样本，共10,000对。
    - **测试集**：500个场景（来自MesaTask-10K测试集）。
    - **泛化测试**：4个未见桌面类别（床头柜、电视柜、边桌、收银台），每类16个任务。
- **对比方法**：
    - **闭源LLM**：GPT-4o（零样本）。
    - **模块化方法**：Holodeck-table、I-Design-table（改编自室内场景生成方法）。
- **评价指标**：
    - **Success Rate**：LLM输出格式正确率。
    - **FID**（Fréchet Inception Distance）：衡量生成场景渲染图的真实感。
    - **GPT Score**：多维VLM评估（5个维度：任务一致性CwT、物体尺寸合理性OSR、放置合理性PPI、布局连贯性LCR、物体可见性OV，每项1-10分）。
    - **用户研究**：127名参与者，从真实感、任务对齐、空间连贯性三个维度打分（7分制）。
- **消融实验**：
    - 移除空间推理链（“w/o reason.”）
    - 移除DPO训练（“w/o DPO”）
- **附加实验**：
    - 在MesaTask-10K上对比ATISS、DiffuScene、PhyScene（表3，使用FID、KID、CKL）。
    - 任务复杂度分析（Level 1-4，表5）。
    - 碰撞率对比（表6）。

### 资源与算力

- **GPU配置**：8块NVIDIA A800 GPU。
- **训练设置**：
    - SFT：学习率 1×10⁻⁵，1个epoch。
    - DPO：学习率 1×10⁻⁶，1个epoch。
    - 均采用全参数微调。
- **未明确说明**总训练时长、推理效率等具体时间消耗。

### 实验数量与充分性

- **主要实验结果**（表1）：涵盖4种方法（含消融变体）在Success Rate、FID、GPT Score 5个子项及用户研究上的对比，共约20个数值。
- **消融实验**：明确对比了w/o reason、w/o DPO、完整MesaTask三个配置，验证了空间推理链和DPO的贡献。
- **泛化实验**（表2）：在4个未见桌类上测试，所有指标结果与已见类别相当。
- **附加实验**：含表3（与其他生成方法对比）、表5（任务复杂度）、表6（碰撞率），均提供了定量数据。
- **用户研究**：127名参与者，随机采样5个场景/人，共约635次评估。
- **充分性评估**：实验设计较为全面，覆盖了主要基线、消融、泛化、物理仿真验证及人因评估。但部分实验（如不同任务复杂度的FID差异）未给出充分解释；此外，所有测试数据均为合成场景，缺乏真实场景或域外迁移测试，存在一定局限性。

### 主要结论与发现

- MesaTask在FID、GPT Score、用户研究中**全面优于**GPT-4o、Holodeck-table、I-Design-table，尤其在任务对齐（CwT）和布局连贯性（LCR）上有显著优势。
- **空间推理链**有效弥合了任务与场景间的语义鸿沟，**DPO训练**进一步减少了物体碰撞和关系错误，提升了生成质量。
- 框架在**未见过桌面类别**上展现了良好的泛化能力，能准确推断新物体的描述、尺寸和放置。
- 物理后处理（仿真器检查）使碰撞率降至0%，保证物理合理性。

### 优点

1. **高质量数据集**：MesaTask-10K规模大（10,700场景）、手工精修布局、涵盖6种桌面类型、200+物体类别，包含复杂物体间关系，为同类研究提供了坚实基础。
2. **创新推理链**：将任务到场景的生成分解为可训练的链式步骤（对象→关系→场景图→布局），显著降低LLM学习难度。
3. **DPO有效改进**：通过构造多种物理/语义负样本，显式惩罚物体碰撞、关系错误和物体缺失，提升了生成的实用性和可靠性。
4. **多维度评估**：除传统图像质量（FID）外，设计了VLM驱动的GPT Score和用户研究，从任务对齐、物理合理性、布局真实感等多角度衡量，评估较全面。
5. **可推广性**：方法可扩展到未见过桌类和新任务复杂度，具备一定通用性。

### 不足与局限

1. **物体多样性受限**：依赖预先定义的3D资产库进行检索，无法生成资产库中不存在的物体；作者指出未来需结合3D物体生成方法（如基于边界框条件生成）突破此限制。
2. **训练数据偏差**：SFT训练数据中任务复杂度以Level 4（抽象目标描述）为主（83.8%），可能导致模型在低复杂度具体指令上的性能略逊（如Level 1-2虽评分高但FID较差），存在一定分布偏移。
3. **场景来源为合成图像**：MesaTask-10K基于文本到图像模型生成的图像构造，虽然手工精修，但与真实拍摄的桌面场景仍有差距，可能影响在真实机器人环境中的直接迁移。
4. **缺乏真实域实验**：所有实验均在合成场景上完成，未涉及真实世界桌面场景或域迁移测试，泛化能力验证局限于未见类别（仍为合成数据）。
5. **计算资源与效率未充分报告**：未提供训练时间、推理时间等实际效率数据，不利于可重复性评估。
6. **用户研究设计**：仅基于渲染图像，未提供交互性体验（如模拟任务执行），评价维度可能不够全面。

（完）
