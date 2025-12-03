# Adaptive Prompt Optimization using Reinforcement Learning (RLHF-Lite)
```python
print("Hello World")
```

**CSI 5130 – Artificial Intelligence Project**



## 1. Project Overview
Large Language Models (LLMs) such as T5, GPT-4, and Mistral are highly sensitive to how prompts are phrased.  
A well-crafted prompt produces clear, accurate responses, while a poorly phrased one may result in irrelevant or incorrect output.

This project builds a small-scale Adaptive Prompt Optimization system using a simplified RLHF approach called RLHF-Lite, where automated metrics (ROUGE-1 + BLEU) replace human feedback.  
A lightweight Q-learning agent interacts with FLAN-T5-Base and learns which prompt template yields better summarization quality over time.


## 2. Objectives
- Implement a Q-learning agent to choose the best prompt template  
- Use FLAN-T5-Base as the summarization model  
- Design a reward function using ROUGE-1 + BLEU  
- Show improvement in prompt selection over training iterations  
- Produce a final report and demonstration notebook


## 3. Methodology
The system operates on a small summarization task using a few handcrafted text–summary pairs.

- The environment is the FLAN-T5-Base model  
- The agent chooses from five prompt templates (e.g., `"Summarize the following:"`, `"TL;DR:"`)  
- At each step:
  1. Agent selects a prompt via ε-greedy
  2. FLAN-T5 generates a summary  
  3. Reward computed using ROUGE-1 + BLEU  
  4. Q-values updated  
- Training runs for a limited number of iterations on Google Colab

This lightweight setup avoids large-scale RLHF infrastructure and focuses only on prompt selection.


## 4. Evaluation Plan
Evaluation is based on:

- ROUGE-1 and BLEU scores (combined into a single reward)  
- Reward trend across iterations  
- Q-value progression to detect template preference  
- Before/after comparisons of summaries  


## 5. Expected Outcomes
- A reinforcement-learning-based prompt selector 
- Evidence of learning through reward curves** and Q-value updates  
- Improved summarization quality after training  
- A complete written report and Colab demonstration notebook

 Team Members:
 
 Agna Antony            - agnaantony@oakland.edu
 
 Vineela Rao Akasapu     - vineelaraoakasa@oakland.edu
 
 Mubassir Gamfoi        - mubassirgamfoi@oakland.edu 

