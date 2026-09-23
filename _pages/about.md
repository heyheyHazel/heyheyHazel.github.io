---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

# 👩‍💻 Who am I

Currently, I am an master student majoring in Applied Statistics at **Xi'an Jiaotong University (XJTU)**, where my research interests lie in **Agentic Reinforcement Learning**, **self-evolving systems**, and **generative recommendation**. Previously, I received my B.S. in Data Science and Big Data Technology from **China Agricultural University (CAU)**.

I have gained hands-on industry experience through internships at **Tencent** (ecommerce recommendation at WXG), **Baidu** (LLM applications in commercial advertising), and **Meituan** (LLM applications on the financial service platform), where I developed practical skills in building and deploying AI systems at scale.


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

<div class='paper-box'><div class='paper-box-image'><div><img src='images/e-commerce.png' alt="Recommendation Agent" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Multi-Agent Shopping Assistant](https://github.com/heyheyHazel/Multi-Agent-Ecommerce-System)

**LangGraph · Multi-agent · Redis · FastAPI · React**

- A multi-agent e-commerce shopping assistant that orchestrates recommendation, copywriting, and inventory agents through a Supervisor pattern. Features include user profiling with RFM clustering, LLM reranking, Thompson Sampling for A/B testing, and SSE streaming responses.
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><img src='images/mia.png' alt="Investment Agent" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[MIA: Multi-Agent Investment Assistant](https://github.com/heyheyHazel/Investment-Research-Agent)

**LangGraph · Supervisor-worker · BGE-M3 · Milvus · Streamlit**

- M.I.A. is a multi-agent investment research and analysis system designed using LangGraph. Employing a multi-agent architecture, it implements Agentic RAG and supports intelligent Q&A regarding research reports, automated generation of financial charts, and multi-source data fusion analysis, aiming to provide buy-side participants in the secondary market with precise market insights and investment recommendations.
</div>
</div>


## 🛠️ Post-Training

<div class='paper-box'><div class='paper-box-image'><div><img src='images/medicalgpt.png' alt="MedicalGPT" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[MedicalGPT](https://github.com/heyheyHazel/MedicalGPT)

**CPT · SFT · PPO · GRPO · DPO · LLM-as-a-Judge**

- A medical large language model trained through a comprehensive pipeline encompassing continual pre-training, supervised fine-tuning, RLHF (including reward modeling and reinforcement learning training), and DPO (Direct Preference Optimization).
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><img src='images/minimind.png' alt="minimind" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[minimind](https://github.com/heyheyHazel/minimind)

**Llama · Pretraining · SFT · RLHF**

- Build and train a small-scale Llama language model from scratch, covering tokenization, Transformer architecture, pretraining, and supervised fine-tuning.
</div>
</div>


# 💻 Internships

### [Tencent - WXG](https://tencent.com) · June. 2026 - now

**Agentic RL · SFT · Slime · vLLM · ReAct**

- **Agentflow**: built an intent-classification → routing → scenario-agent architecture covering product recommendation, coupon claiming and customer service; 99% accuracy on 7-class intent recognition at 500ms P95 latency.
- **Agent Loop**: defined combined recommendation under multi-dimensional constraints; built profile, memory and product-search MCP tools, solved coupon and budget constraints with grouped-knapsack DP, and bounded the loop with ReAct.
- **Agentic RL**: cold-started Qwen3-4B with a 200-step LoRA on 3k curated teacher trajectories; built the RL pipeline on Slime with outcome, process and format rewards, reaching 98% constraint satisfaction and +11pp HitRate.
- **Highlight**: project owner from 0 to 1, leading architecture selection, data engineering, benchmark and evaluation; built 50k shopping queries with a frozen 1k benchmark; wrote an internal tech article and gave a team tech talk.


### [Baidu - Commercial Advertising](https://baidu.com) · Feb. 2026 - May. 2026

**GRPO · veRL · LLM-as-a-Judge · Multi-agents · Skill**

- **Dynamic strategy selection**: mined high-conversion scripts from real sales calls with Embedding + HDBSCAN clustering; matched strategy clusters by intent at inference with Thompson Sampling and an over-heating guard; WeChat-add rate 2.5% → 5.2% in small-traffic tests.
- **Model training**: designed a data synthesis pipeline (multi-agent simulation + real-dialogue injection + quality filtering) yielding 3k human-level calls; GRPO with semantic-similarity, length and Bayesian-reasoning rewards lifted the sales score 5.92 → 7.49 (+26.5%).
- **Evaluation**: built an LLM-as-a-Judge pipeline covering 6 core sales skills and 7 fine-grained metrics; ran a Turing test with frontline sales (72% human detection rate, 48% model-win rate).


### [Meituan - Financial Service Platform](https://meituan.com) · Mar. 2025 - Jun. 2025

**Workflow · Dify · CoT · Few-shot · RAG**

- **Complaint ticket classification**: built the complaint taxonomy across business lines along the user journey; designed Multi-step CoT + Few-shot prompts on a business knowledge base; shipped a Dify workflow (load → preprocess → inference → parse/output) with >95% accuracy (+30pp).
- **Ticket retrieval assistant**: rewrote retrieval queries into structured search plans; used parent-child document indexing with hybrid BM25 + vector recall, re-ranked by term frequency and business weights, and returned Top-10 tickets through an end-to-end workflow.
- **Highlight**: project owner, driving the LLM application on the complaint data platform from 0 to 1 — annotation workflow plus a retrieval assistant delivered to the operations team.
