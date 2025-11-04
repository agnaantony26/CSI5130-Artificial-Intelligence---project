# CSI5130-Artificial-Intelligence---project
**Adaptive Prompt Optimization using Reinforcement Learning (RLHF-lite)**
 
## 1) Project Overview
Depending on how the input prompt is written, large language models (LLMs) such as Mistral and GPT-4 perform differently.  While poorly written prompts can result in misunderstandings or mistakes, well-written ones can inspire precise and imaginative answers.  The goal of this project is to develop an Adaptive Prompt Optimization system that uses Reinforcement Learning (RL) to automatically learn how to make prompts better.  Beginning with a straightforward prompt, the system will assess the model's output quality and gradually learn to produce better prompts that produce better outcomes.  This project is RLHF-lite, a condensed, lightweight variant of RLHF (Reinforcement Learning from Human Feedback) intended for small-scale testing.

## 2) Objectives
- **RL Agent:** Implement an agent that improves prompts for a chosen task (e.g., summarization or QA).  
- **Target Model:** Use an LLM (GPT‑3.5/GPT‑4/Mistral) as the response generator.  
- **Reward Function:** Define automatic metrics (BLEU/ROUGE/accuracy) to score each response.  
- **Learning Evidence:** Demonstrate improvement across training iterations (learning curves + examples).

## 3) Methodology
1. **Task selection.** Choose a simple generative task (e.g., summarization on a small dataset).  
2. **Base model.** Query GPT‑3.5/GPT‑4/Mistral via API as the environment’s response generator.  
3. **RL loop.** The agent proposes a new prompt (action) given state (previous prompt + stats), receives reward from metrics, and updates its prompt policy.  
4. **Reward.** Compute BLEU/ROUGE (or task accuracy) against references; optionally combine with style/length constraints.  
5. **Policy update.** Start with a simple Q‑learning baseline; optionally compare with a lightweight policy‑gradient (REINFORCE) variant.  

## 4) Evaluation Metrics
- **Task score:** BLEU/ROUGE improvement (summarization), or accuracy (QA/classification).  
- **Learning signal:** Average reward per iteration; smoothed learning curve.  
- **Stability:** Reward variance across seeds/runs.  
- **Qualitative:** Before/after prompt examples with side‑by‑side outputs.

## 5) Expected Outcome
An adaptive system that learns prompt edits which improve the target LLM’s performance on the chosen task. Deliverables include:
- Learning curves (reward/metric vs. iteration)  
- Ablations (Q‑learning vs. REINFORCE; different reward mixes)  
- Before/after prompt examples and outputs  
- Final report + demo


 Team Members:
 
 Agna Antony            - agnaantony@oakland.edu
 
 Vineela Rao Akasapu     - vineelaraoakasa@oakland.edu
 
 Mubassir Gamfoi        - mubassirgamfoi@oakland.edu 
