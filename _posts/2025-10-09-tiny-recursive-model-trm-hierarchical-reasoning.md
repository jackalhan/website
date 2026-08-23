---
layout: post
title: Tiny Recursive Model ; Small, Simple… and Surprisingly Strong 🤖🧩
date: 2025-10-09 09:30:00
description: The 7M-parameter Tiny Recursive Model (TRM) outperforms larger networks on reasoning puzzles like Sudoku, Maze, and ARC-AGI through clever recursion.
tags: AI MachineLearning DeepLearning Reasoning Recursion LLM AgenticAI GenAI Walmart WalmartGlobalTech
categories: research-notes
---

Small, simple… and surprisingly strong.

A few months back, the **Hierarchical Reasoning Model (HRM)** ([Paper](https://lnkd.in/e8z4yYKn)) showed that a 27M-param network could beat much larger LLMs on grid-based puzzles like Sudoku, Maze, and ARC-AGI. Now a follow-up paper proposes the **Tiny Recursive Model (TRM)** ([Paper](https://lnkd.in/eEczp_cd)): a 7M-param, single 2-layer network that out-generalizes HRM on the same tasks.

### What “recursion” means here

TRM iteratively (1) updates a latent reasoning state from the current question + answer, then (2) refines the answer from that state—repeating up to 16 times.  
Training runs several no-grad refinement loops and then backprops through one full recursion per step, which seems to help generalization.

### How TRM differs from HRM

- **Architecture:** one tiny 2-layer net vs. HRM’s two 4-layer nets.
- **Training:** TRM backprops through the full recursion; HRM only backprops the final evaluations (earlier steps are detached).
- **Halting:** TRM learns when to stop with a simple BCE “halt” head—no extra forward pass.

### Results (test accuracy)

- **Sudoku-Extreme:** TRM 87.4% (vs. HRM 55.0%)
- **Maze-Hard:** TRM 85.3% (vs. 74.5%)
- **ARC-AGI-1/2:** TRM 44.6% / 7.8% (vs. 40.3% / 5.0%)

### Neat tidbits

- **Fewer layers ≠ worse:** dropping from 4 to 2 layers improved Sudoku generalization (79.5% → 87.4%), likely reducing overfitting.
- **Replacing self-attention with an MLP** boosted accuracy on fixed-size grids like Sudoku (74.7% → 87.4%), though attention still helps on larger 30×30 grids (Maze/ARC).

Comparing these tiny, task-specific models to general-purpose LLMs isn’t apples-to-apples. But TRM is a compelling proof that **clever structure + recursion can rival (and sometimes surpass) sheer scale** on the right problems.  
Modules like this could easily become components within larger, tool-using AI systems.

Congrats to **Alexia Jolicoeur-Martineau** and the team!

[Paper](https://lnkd.in/eEczp_cd)

---

#AI #MachineLearning #DeepLearning #Reasoning #Recursion #LLM #AgenticAI #GenAI #Walmart #WalmartGlobalTech
