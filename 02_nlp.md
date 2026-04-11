# 02 — NLP Basics

> How computers understand human language: from raw text to meaningful numbers.

## What's Covered

| Notebook | Topic | Key Concept |
|----------|-------|-------------|
| `02_nlp_basics.ipynb` | Full NLP pipeline | tokenize → encode → embed |

## The Pipeline

```
"I love AI"
    ↓ tokenize
['i', 'love', 'ai']
    ↓ encode (vocabulary lookup)
[4, 7, 0]
    ↓ embedding
'i'    → [ 0.24, -1.91, -1.72]
'love' → [-0.23,  0.07, -1.42]
'ai'   → [ 0.50, -0.14,  0.65]
    ↓
Ready for neural network ✓
```

## Key Concepts

**Tokenization** — Split text into pieces. Simple approach: one word = one token.

**Vocabulary** — A dictionary mapping every unique word to a number. GPT2 has 50,257 words.

**One-Hot Encoding** — Old method. Each word is a vector with one `1` and rest `0`. Problem: all words are equally distant — no meaning.

**Embedding** — Modern method. Each word is a dense vector of real numbers. Similar words have similar vectors. These numbers are *learned* during training.

## Why This Matters

When you send a message to GPT or Claude, the very first step is this exact pipeline — your text gets tokenized and converted to embeddings before the model processes it.

## Run in Colab

Click `02_nlp_basics.ipynb` → Open in Colab → Run All

---
**Previous:** [01 Neural Networks](../01_neural_networks/) | **Next:** [03 Attention](../03_attention/)
