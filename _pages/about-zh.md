---
permalink: /zh/
title: ""
excerpt: ""
author_profile: true
lang: zh
nav_data: main_zh
home_label: "首页"
alt_lang_url: /home/
description: "西安交通大学应用统计硕士在读，研究方向为 Agentic RL、Recursive Self-Improvement (RSI) 与 LLM Infra。"
redirect_from:
  - /zh.html
---

# 👩‍💻 我是谁 {#who-am-i}

我目前在**西安交通大学（XJTU）**攻读应用统计硕士，主要关注 **Agentic Reinforcement Learning**、**Recursive Self-Improvement** 和 **LLM Infrastructure**。本科就读于**中国农业大学（CAU）**数据科学与大数据技术专业。

我曾在**腾讯**、**百度**和**美团**实习，主要从事面向实际业务场景的 LLM 后训练，以及 AI 系统的构建与部署。


# 📖 教育经历 {#educations}
- *2025.09 - 2028.06*，**应用统计硕士**，西安交通大学，西安。
- *2021.09 - 2025.06*，**数据科学与大数据技术学士**，中国农业大学，北京。


# 🎖 荣誉奖项 {#honors}
- *2025.10* **学业特等奖学金**，西安交通大学。
- *2025.09* **新生一等学业奖学金**，西安交通大学。
- *2025.06* **优秀毕业生**，中国农业大学。
- *2024.12* **一等学业奖学金**，中国农业大学。
- *2024.06* 全国市场调查与分析大赛**国家三等奖**，校赛**冠军**。
- *2023.10* 全国大学生数学建模竞赛**国家二等奖**。


# 💻 项目 {#projects}

## 🤖 Agent {#agent}

<div class='paper-box'><div class='paper-box-image'><div><h3><a href="https://github.com/heyheyHazel/Awesome-Agentic-Shopping-Assistant">Agentic Shopping Assistant</a></h3><img src="{{ '/images/e-commerce.png' | relative_url }}" alt="Agentic Shopping Assistant" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Tool-calling agent · Hybrid RRF retrieval · SFT · RLVR · OPD**

- **购物数据**：基于 ShopSimulator 数据整理了 23,315 件真实商品的中文信息，涵盖 9 个类目，并转换得到 4,009 个用户画像。
- **Agent 流程**：在同一工具调用循环中完成意图理解、查询改写、选品和文案生成；闲聊仅需调用 1 次 LLM，每轮购物咨询调用 2–4 次。
- **工具调用**：通过 RRF 融合关键词检索与本地 ONNX 向量召回，结合基于分位数的 RFM 用户画像，并按预算和商品类目进行硬性过滤。
- **后训练**：以教师模型的交互轨迹构建逐轮 SFT 数据，再进行 on-policy RLVR/OPD 训练。
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><h3><a href="https://github.com/heyheyHazel/Investment-Research-Agent">M.I.A: Multi-Agent Investment Assistant</a></h3><img src="{{ '/images/mia.png' | relative_url }}" alt="M.I.A: Multi-Agent Investment Assistant" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**LangGraph · Supervisor-worker · Agentic RAG · DeepSeek-R1 · BGE-reranker-v2-m3**

- **多 Agent 协作**：Supervisor 分解任务并分派给研报、财报、新闻、公告、行情、代码、分析和质检八类 Agent，通过 LangGraph 共享状态。
- **Agentic RAG**：解析研报与财报，将内容存入向量库（Chroma / FAISS / Milvus）和 DuckDB 数据表，再使用 BGE-reranker-v2-m3 对检索结果重排。
- **图表生成与质检**：代码 Agent 编写并运行 matplotlib 代码生成图表，质检 Agent 检查输出，并通过反馈推动自我反思与修正。
- **买方投研分析**：结合 AKShare 行情数据与实时新闻情绪，开展盈利预测、分部估值和同业比较。
</div>
</div>


## 🛠️ 后训练 {#post-training}

<div class='paper-box'><div class='paper-box-image'><div><h3><a href="https://github.com/heyheyHazel/MedicalGPT">MedicalGPT: Medical LLM Post-Training</a></h3><img src="{{ '/images/medicalgpt.png' | relative_url }}" alt="MedicalGPT" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Qwen2.5-7B · CPT · SFT · RM · PPO · DPO · GRPO**

- **完整训练流程**：覆盖持续预训练、SFT、奖励模型训练以及 PPO、DPO、GRPO，各阶段均提供 LoRA 和全参数训练方案。
- **CPT + SFT**：在医疗 C-Eval 子集（basic_medicine / clinical / physician）上，CPT 将得分从 79.91 提升至 82.79；基线 SFT 出现知识能力下降（alignment tax），采用知识匹配的 SFT 数据后，得分进一步提升至 84.98。
- **数据合成**：针对含噪声的偏好数据，围绕主诉、病史和问题重构提示词，利用 DeepSeek-R1 构造非对称偏好样本对，形成 RLAIF 数据流程；同时使用 SFT 模型生成负样本，构建 PPO 推理训练数据。
- **开源项目改进**：重新设计 GRPO 奖励，综合格式、语义相似度、LLM 评分和困惑度惩罚，引导模型生成显式 CoT；适配 PPO 的单卡训练与 DDP 多卡训练。
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><h3><a href="https://github.com/heyheyHazel/minimind">MiniMind: LLM from Scratch</a></h3><img src="{{ '/images/minimind.png' | relative_url }}" alt="MiniMind" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Llama · Pretraining · SFT · LoRA · DPO · RLAIF**

- **从零实现**：使用原生 PyTorch 实现 Llama 风格的模型，涵盖分词器训练、注意力机制与 Transformer 模块（GQA / MoE 变体），以及预训练、SFT、LoRA、DPO 和 RLAIF（PPO / GRPO）。
- **核心算法与训练**：使用原生 PyTorch 编写各项核心算法；25.8M 参数模型（约为 GPT-3 的 1/7000）在单张 4090 上约 2 小时即可完成训练。
- **推理模型**：构建 R1-Zero 风格的推理模型，训练数据与模型权重均开源。
</div>
</div>


# 💻 实习经历 {#internships}

<div class='paper-box intern-box'>
<div class='paper-box-image'><div><h3><a href="https://tencent.com">腾讯 WXG</a></h3><div class="intern-logo intern-logo--tencent"><img src="{{ '/images/tencent.png' | relative_url }}" alt="Tencent"></div></div></div>
<div class='paper-box-text' markdown="1">

**Agentic RL · SFT · Slime · vLLM · ReAct**

- **Agentflow**：搭建意图路由与场景 Agent，意图识别准确率达 99%，P95 延迟为 500 ms。
- **Agent Loop**：结合 MCP 工具与背包动态规划，实现满足多项约束的推荐。
- **Agentic RL**：通过 LoRA 完成冷启动，再使用 Slime 进行 RL 训练；HitRate 提升 11 个百分点，约束满足率达 98%。
- **项目职责**：负责项目从零到一的开发，构建 5 万条查询数据与评测基准，并撰写技术文章、开展技术分享。

</div>
</div>


<div class='paper-box intern-box'>
<div class='paper-box-image'><div><h3><a href="https://baidu.com">百度 商业广告</a></h3><div class="intern-logo intern-logo--baidu"><img src="{{ '/images/baidu.png' | relative_url }}" alt="Baidu"></div></div></div>
<div class='paper-box-text' markdown="1">

**GRPO · veRL · LLM-as-a-Judge · Multi-agents · Skill**

- **策略挖掘**：结合 HDBSCAN 与 Thompson Sampling，将微信添加率从 2.5% 提升至 5.2%。
- **模型训练**：合成 3,000 条外呼对话数据，通过 GRPO 将销售评分从 5.92 提升至 7.49。
- **效果评估**：采用 LLM-as-a-Judge 进行评估；图灵测试检出率为 72%，模型胜率为 48%。

</div>
</div>


<div class='paper-box intern-box'>
<div class='paper-box-image'><div><h3><a href="https://meituan.com">美团 金融服务平台</a></h3><div class="intern-logo intern-logo--meituan"><img src="{{ '/images/meituan.png' | relative_url }}" alt="Meituan"></div></div></div>
<div class='paper-box-text' markdown="1">

**Workflow · Dify · CoT · Few-shot · RAG**

- **工单分类**：在 Dify 工作流中设计 CoT 提示词，分类准确率超过 95%，较原方案提升 30 个百分点。
- **工单检索**：融合 BM25 与向量召回，实现从查询到返回 Top-10 相关工单的完整流程。
- **项目职责**：负责项目开发与落地，将 LLM 应用交付给运营团队使用。

</div>
</div>
