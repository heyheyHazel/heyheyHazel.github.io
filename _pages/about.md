---
permalink: /home/
title: ""
excerpt: ""
author_profile: true
lang: en
nav_data: main
alt_lang_url: /zh/
redirect_from:
  - /about/
  - /about.html
---

# 👩‍💻 Who am I

Currently, I am a master student majoring in Applied Statistics at **Xi'an Jiaotong University (XJTU)**, where my research interests lie in **Agentic Reinforcement Learning**, **Recursive Self-Improvement**, and **LLM Infrastructure**. Previously, I received my B.S. in Data Science and Big Data Technology from **China Agricultural University (CAU)**.

I have gained hands-on industry experience through internships at **Tencent**, **Baidu**, and **Meituan**, where I developed practical skills in building and deploying AI systems at scale.


# 📖 Educations
- *2025.09 - 2028.06*, **M.S. in Applied Statistics**, Xi'an Jiaotong University, Xi'an.
- *2021.09 - 2025.06*, **B.S. in Data Science and Big Data Technology**, China Agricultural University, Beijing.


# 🎖 Honors and Awards
- *2025.10* **Special Academic Scholarship**, Xi'an Jiaotong University.
- *2025.09* **First-Class Scholarship for New Students**, Xi'an Jiaotong University.
- *2025.06* **Outstanding Graduate**, China Agricultural University.
- *2024.12* **First-Class Scholarship for Academic Excellence**, China Agricultural University.
- *2024.06* **National 3rd Prize** in the Market Research and Analysis Competition & **championship** in the university-level competition.
- *2023.10* **2nd Prize** in the National Undergraduate Mathematical Modeling Contest.

# 💻 Projects

## 🤖 Agent

<div class='paper-box'><div class='paper-box-image'><div><h3><a href="https://github.com/heyheyHazel/Awesome-Agentic-Shopping-Assistant">Agentic Shopping Assistant</a></h3><img src="{{ '/images/e-commerce.png' | relative_url }}" alt="Agentic Shopping Assistant" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Tool-calling agent · Hybrid RRF retrieval · SFT · RLVR · OPD**

- **Shopping data**: 23,315 real Chinese products over 9 categories and 4,009 shopper personas converted from the ShopSimulator release.
- **Agent loop**: intent, query rewriting, product picking and copywriting in a single tool-calling loop; 1 LLM call for chat, 2–4 per shopping turn.
- **Tool calling**: hybrid keyword + local ONNX vector recall (RRF), quantile RFM profiles and budget/category hard filters.
- **Post-training**: teacher trajectories → turn-level SFT → on-policy RLVR/OPD.
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><h3><a href="https://github.com/heyheyHazel/Investment-Research-Agent">M.I.A: Multi-Agent Investment Assistant</a></h3><img src="{{ '/images/mia.png' | relative_url }}" alt="M.I.A: Multi-Agent Investment Assistant" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**LangGraph · Supervisor-worker · Agentic RAG · DeepSeek-R1 · BGE-reranker-v2-m3**

- **Eight specialist agents**: a supervisor decomposes and routes tasks to report / financial / news / announcement / market / code / analysis / QC agents over a shared LangGraph state.
- **Agentic RAG**: research reports and financials into vector stores (Chroma / FAISS / Milvus) plus DuckDB tables, reranked by BGE-reranker-v2-m3.
- **Code + QC loop**: the code agent writes and runs matplotlib code for charts; the QC agent validates outputs and drives self-reflection before returning results.
- **Buy-side view**: earnings forecast, segment valuation and peer comparison over AKShare market data and live news sentiment.
</div>
</div>


## 🛠️ Post-Training

<div class='paper-box'><div class='paper-box-image'><div><h3><a href="https://github.com/heyheyHazel/MedicalGPT">MedicalGPT: Medical LLM Post-Training</a></h3><img src="{{ '/images/medicalgpt.png' | relative_url }}" alt="MedicalGPT" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Qwen2.5-7B · CPT · SFT · RM · PPO · DPO · GRPO**

- **Full training pipeline**: continual pre-training → SFT → reward modeling → PPO → DPO → GRPO, each stage with LoRA and full-parameter recipes.
- **CPT + SFT**: medical C-Eval (basic_medicine / clinical / physician) 79.91 → 82.79; baseline SFT exposed the alignment tax, knowledge-matched SFT recovered it to 84.98.
- **Data synthesis**: rebuilt DPO pairs from noisy data into an RLAIF pipeline (chief-complaint / history / question prompts, DeepSeek-R1 asymmetric pairs) and built PPO reasoning data with SFT-model negatives.
- **Incremental on the open-source project**: reworked the GRPO reward (format, semantic similarity, LLM judge, PPL penalty) to obtain explicit CoT, adapted PPO to single-card and DDP multi-card training.
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><h3><a href="https://github.com/heyheyHazel/minimind">MiniMind: LLM from Scratch</a></h3><img src="{{ '/images/minimind.png' | relative_url }}" alt="MiniMind" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Llama · Pretraining · SFT · LoRA · DPO · RLAIF**

- **From scratch in PyTorch**: implemented a Llama-style model end to end, including tokenizer training, attention and Transformer blocks (GQA / MoE variants), pretraining, SFT, LoRA, DPO and RLAIF (PPO / GRPO).
- **Architecture depth**: every core algorithm written in native PyTorch instead of high-level wrappers; the 25.8M-parameter model (~1/7000 of GPT-3) trains in about 2 hours on a single 4090.
- **Reasoning**: builds an R1-Zero-style reasoning model with fully open data and weights.
</div>
</div>


# 💻 Internships

<div class='paper-box intern-box'>
<div class='paper-box-image'><div><h3><a href="https://tencent.com">Tencent - WXG</a></h3><img src="{{ '/images/tencent.png' | relative_url }}" alt="Tencent"></div></div>
<div class='paper-box-text' markdown="1">

**Agentic RL · SFT · Slime · vLLM · ReAct**

- **Agentflow**: intent routing + scenario agents; 99% intent accuracy, 500ms P95.
- **Agent Loop**: multi-constraint recommendation via MCP tools and knapsack DP.
- **Agentic RL**: LoRA cold start + RL on Slime; HitRate +11pp, constraints 98%.
- **Highlight**: project owner (0→1), 50k queries + benchmark, tech article/talk.

</div>
</div>


<div class='paper-box intern-box'>
<div class='paper-box-image'><div><h3><a href="https://baidu.com">Baidu - Commercial Advertising</a></h3><img src="{{ '/images/baidu.png' | relative_url }}" alt="Baidu"></div></div>
<div class='paper-box-text' markdown="1">

**GRPO · veRL · LLM-as-a-Judge · Multi-agents · Skill**

- **Strategy mining**: HDBSCAN + Thompson Sampling; WeChat-add 2.5% → 5.2%.
- **Model training**: 3k synthesized calls; GRPO lifted sales score 5.92 → 7.49.
- **Evaluation**: LLM-as-a-Judge; Turing test 72% detection, 48% model win.

</div>
</div>


<div class='paper-box intern-box'>
<div class='paper-box-image'><div><h3><a href="https://meituan.com">Meituan - Financial Service Platform</a></h3><img src="{{ '/images/meituan.png' | relative_url }}" alt="Meituan"></div></div>
<div class='paper-box-text' markdown="1">

**Workflow · Dify · CoT · Few-shot · RAG**

- **Ticket classification**: CoT prompts in a Dify workflow; accuracy >95% (+30pp).
- **Ticket retrieval**: hybrid BM25 + vector recall; Top-10 tickets end to end.
- **Highlight**: project owner; LLM use case shipped to the operations team.

</div>
</div>
