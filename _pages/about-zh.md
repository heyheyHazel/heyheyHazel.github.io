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

目前我在**西安交通大学（XJTU）**攻读应用统计硕士，研究兴趣集中在 **Agentic Reinforcement Learning（Agentic RL）**、**Recursive Self-Improvement（RSI）**与 **LLM Infrastructure（LLM Infra）**三方面。此前我在**中国农业大学（CAU）**取得数据科学与大数据技术学士学位。

我曾在**腾讯**（WXG 电商推荐）、**百度**（商业广告大模型应用）与**美团**（金融服务平台大模型应用）实习，积累了构建并落地大规模 AI 系统的工程经验。


# 📖 教育经历 {#educations}
- *2025.09 - 2028.06*，**应用统计 硕士**，西安交通大学，西安。
- *2021.09 - 2025.06*，**数据科学与大数据技术 学士**，中国农业大学，北京。


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

**Tool-calling agent · Hybrid RRF retrieval · Turn-level SFT · GRPO/RLVR**

- **单 Agent 循环**：意图理解、query 改写、选品与文案都在同一个 tool-calling 循环内完成；闲聊 1 次 LLM 调用，购物咨询 2–4 次。
- **确定性工具**：关键词 + 本地 ONNX 向量混合召回（RRF 融合）、分位 RFM 画像、预算/类目硬过滤永不放宽。
- **ShopSimulator 数据**：基于 ShopSimulator 转换的 23,315 件中文商品、9 个类目与 4,009 个用户画像；带过滤召回中位 7–9 ms。
- **后训练**：教师轨迹 → turn 级 SFT（真实 loss mask）→ on-policy GRPO/RLVR；1.7B 全参 SFT 单卡 24 GB 可跑；117 个测试无需 GPU。
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><h3><a href="https://github.com/heyheyHazel/Investment-Research-Agent">M.I.A: Multi-Agent Investment Assistant</a></h3><img src="{{ '/images/mia.png' | relative_url }}" alt="M.I.A: Multi-Agent Investment Assistant" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**LangGraph · Supervisor-worker · Agentic RAG · DeepSeek-R1 · BGE-reranker-v2-m3**

- **八个专业 Agent**：Supervisor 负责任务分解与路由，协同研报 / 财报 / 新闻 / 公告 / 行情 / 代码 / 分析 / 质检 Agent，共享 LangGraph 状态。
- **Agentic RAG**：研报与财报解析进向量库（Chroma / FAISS / Milvus）与 DuckDB 表，由 BGE-reranker-v2-m3 重排。
- **代码 + 质检闭环**：代码 Agent 生成并执行 matplotlib 代码出图，质检 Agent 校验结果并驱动自我反思。
- **买方视角**：基于 AKShare 行情与实时舆情的盈利预测、分部估值与同业对比。
</div>
</div>


## 🛠️ 后训练 {#post-training}

<div class='paper-box'><div class='paper-box-image'><div><h3><a href="https://github.com/heyheyHazel/MedicalGPT">MedicalGPT: Medical LLM Post-Training</a></h3><img src="{{ '/images/medicalgpt.png' | relative_url }}" alt="MedicalGPT" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Qwen2.5-7B · CPT · SFT · RM · PPO · DPO · GRPO**

- **全链路训练**：增量预训练 → SFT → 奖励建模 → PPO → DPO → GRPO，每个阶段都提供 LoRA 与全参配方。
- **CPT + SFT**：医疗 C-Eval（basic_medicine / clinical / physician）79.91 → 82.79；baseline SFT 出现对齐税，知识匹配版 SFT 拉回 84.98。
- **数据合成**：把带噪音的偏好数据重做成 RLAIF 链路（主诉 / 现病史 / 核心问题重构 + DeepSeek-R1 非对称正负样本 + 4:1 通用域混合），并用 SFT 模型产出负样本构造 PPO 推理数据。
- **对开源项目的增量改进**：重写 GRPO 奖励（格式 / 语义相似度 / LLM 打分 / 困惑度惩罚）以获得显式 CoT，并把 PPO 适配到单卡与 DDP 多卡。
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><h3><a href="https://github.com/heyheyHazel/minimind">MiniMind: LLM from Scratch</a></h3><img src="{{ '/images/minimind.png' | relative_url }}" alt="MiniMind" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Llama-style · Native PyTorch · Pretraining · SFT · LoRA · DPO · RLAIF**

- **从零实现**：用原生 PyTorch 端到端实现 Llama 式模型——分词器、注意力与 Transformer 模块（GQA / MoE 变体）、预训练、SFT、LoRA、DPO 与 RLAIF（PPO / GRPO）。
- **架构与工程深度**：核心算法全部手写而非依赖高层封装；25.8M 参数（约 GPT-3 的 1/7000）在单卡 3090 上约 2 小时可训。
- **推理模型**：构建 R1-Zero 式推理模型，数据与权重全部开源。
</div>
</div>


# 💻 实习经历 {#internships}

<div class='paper-box intern-box'>
<div class='paper-box-image'><div><h3><a href="https://tencent.com">腾讯 WXG</a></h3><img src="{{ '/images/tencent.png' | relative_url }}" alt="Tencent"></div></div>
<div class='paper-box-text' markdown="1">

**Agentic RL · SFT · Slime · vLLM · ReAct** · *2026.06 - 至今*

- **Agentflow**：意图路由 + 场景 Agent；意图准确率 99%，P95 500ms。
- **Agent Loop**：基于 MCP 工具与背包 DP 的多约束推荐。
- **Agentic RL**：LoRA 冷启动 + Slime 上做 RL；HitRate +11pp，约束满足率 98%。
- **Highlight**：项目 owner（0→1），5 万条 query 与 benchmark，产出技术文章与分享。

</div>
</div>


<div class='paper-box intern-box'>
<div class='paper-box-image'><div><h3><a href="https://baidu.com">百度 商业广告</a></h3><img src="{{ '/images/baidu.png' | relative_url }}" alt="Baidu"></div></div>
<div class='paper-box-text' markdown="1">

**GRPO · veRL · LLM-as-a-Judge · Multi-agents · Skill** · *2026.02 - 2026.05*

- **策略挖掘**：HDBSCAN + Thompson Sampling；加微率 2.5% → 5.2%。
- **模型训练**：3k 条合成外呼数据；GRPO 将销售评分从 5.92 提升到 7.49。
- **评估体系**：LLM-as-a-Judge；图灵测试检出率 72%，模型胜率 48%。

</div>
</div>


<div class='paper-box intern-box'>
<div class='paper-box-image'><div><h3><a href="https://meituan.com">美团 金融服务平台</a></h3><img src="{{ '/images/meituan.png' | relative_url }}" alt="Meituan"></div></div>
<div class='paper-box-text' markdown="1">

**Workflow · Dify · CoT · Few-shot · RAG** · *2025.03 - 2025.06*

- **工单分类**：Dify 工作流中的 CoT 提示；准确率 >95%（+30pp）。
- **工单检索**：BM25 + 向量混合召回；Top-10 工单端到端打通。
- **Highlight**：项目 owner；LLM 用例交付给运营团队。

</div>
</div>
