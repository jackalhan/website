---
layout: post
title: Llama 4 ; Meta Scales MoE, Online RL, and Multimodal Innovation 🦙💡
date: 2025-04-15 09:00:00
description: Impressions and highlights from Meta’s Llama 4 launch—scaling MoE, continuous online RL, multimodal fusion, and more.
tags: AI MachineLearning LLM GenAI Llama4 MixtureOfExperts TechInnovation
categories: research-notes
---

Just read Meta's announcement on the Llama 4 lineup and I'm impressed by their technical approach! Some highlights that caught my attention:

- **Architecture Innovation:** First time we're seeing Meta implement MoE (Mixture-of-Experts) at scale. Llama 4 Maverick has 17B active parameters but 400B total, using a hybrid approach with alternating dense and MoE layers. Each token activates both a shared expert and one of 128 routed experts.

- **Training Efficiency:** They achieved 390 TFLOPs/GPU during pre-training using FP8 precision across 32K GPUs without quality degradation. That's serious compute optimization.

- **Novel RL Approach:** Their "continuous online RL strategy" alternates between model training and self-filtering of prompts based on difficulty. They've discovered that SFT and DPO can actually limit exploration during RL, leading them to remove over 50% of "easy" training data.

- **iRoPE Architecture:** The interleaved attention layers without positional embeddings is fascinating—it's what enables their 10M token context window (up from 128K in Llama 3). They also implement inference-time temperature scaling of attention for better length generalization.

- **Multimodal Integration:** Early fusion approach for merging text and vision tokens in pre-training, with a MetaCLIP-based vision encoder specifically adapted to work with a frozen Llama model.

- **Meta's 2T Parameter Game:** Llama 4 Behemoth (288B active params, 16 experts, ~2T total) required completely revamping their infrastructure. Their fully asynchronous online RL training framework achieved about 10x improvement in training efficiency!

🤔 Worth noting: Despite all these advances, Llama 4 Maverick scores slightly worse than Llama 3.1 on the Multilingual TydiQA benchmark (31.7 vs 34.3) with only marginal improvement on MMLU 5-shot reasoning (85.5 vs 85.2). Trade-offs in the multimodal space?

Congrats to the team at AI at Meta

[Blog link](https://lnkd.in/gW6ej-ZT)

---

#AI #MachineLearning #LLM #GenAI #Llama4 #MixtureOfExperts #TechInnovation
