# LLM-from-Scratch
> Large Language Model from a single neuron to a working chatbot.
This repository documents my complete journey learning how LLM works, built from scratch using Python and Numpy before moving to Pytorch and HuggingFace.

---

## Learning Path

| # | Topic | Key Concepts | Status |
|---|-------|-------------|--------|
| 01 | [Neural Networks](./01_neural_networks/) | neuron, activation, backprop, XOR | Done |
| 02 | [NLP Basics](./02_nlp_basics/) | tokenization, vocabulary, embedding |  Done  |
| 03 | [Attention Mechanism](./03_attention/) | Q, K, V, softmax, self-attention | Done  |
| 04 | [mini-GPT](./04_mini_gpt/) | transformer, text generation | In progress  |
| 05 | [HuggingFace & GPT2](./05_huggingface/) | pipeline, fine-tuning, real LLM | Done |
| 06 | [Finance NLP](./06_finance_nlp/) | stance detection, zero/few-shot, CoT | In progress  |

---

## What I Built

**From scratch (NumPy only):**
- A neural network that learns XOR — impossible with a straight line
- A tokenizer and embedding system from zero
- The full self-attention mechanism: `softmax(Q @ K.T / √d_k) @ V`
- A mini-GPT that generates text word by word

**With real tools:**
- GPT2 text generation using HuggingFace Transformers
- Fine-tuned GPT2 on custom data
- A chatbot with conversation memory
- Reproduced a research paper on financial stance detection (87.5% accuracy)

---

## Key Results

| Project | Result |
|---------|--------|
| XOR Neural Network | 100% accuracy ✓ |
| mini-GPT text generation | Coherent text ✓ |
| GPT2 fine-tuning | Loss: 2.78 after 3 epochs ✓ |
| Financial stance detection | 87.5% accuracy ✓ |

---

## Tech Stack

```
Python · NumPy · PyTorch · HuggingFace Transformers
Sentence-BERT · scikit-learn · Google Colab
```

---

## How to Run

All notebooks run on **Google Colab** — no setup needed.

1. Click any `.ipynb` file in this repo
2. Click **"Open in Colab"** button
3. Run all cells

---

## Background

I am a Data Science student with a background in supervised/unsupervised ML.
I built this to deeply understand how LLMs work — not just use them as black boxes.

Every component is explained in **English**.

---

## Repository Structure

```
llm-from-scratch/
├── 01_neural_networks/     # Single neuron → XOR network
├── 02_nlp_basics/          # Text → numbers → embeddings  
├── 03_attention/           # The heart of all LLMs
├── 04_mini_gpt/            # Build GPT from scratch
├── 05_huggingface/         # Real GPT2 with HuggingFace
└── 06_finance_nlp/         # LLMs for financial text
```

---


