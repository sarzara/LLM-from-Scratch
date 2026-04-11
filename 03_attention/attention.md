# 03 — Self-Attention Mechanism

> The single most important concept in modern AI — implemented from scratch.

## The Formula

```
Attention(Q, K, V) = softmax( Q @ K.T / √d_k ) @ V
```

This one formula is the heart of GPT, Claude, BERT, and every modern LLM.

## What's Covered

| Notebook | Topic |
|----------|-------|
| `03_attention.ipynb` | Full self-attention from scratch, step by step |

## 6 Steps Explained

```
Step 1: X           → input embeddings (from notebook 02)
Step 2: W_Q, W_K, W_V → weight matrices (learned during training)
Step 3: Q = X@W_Q   → "What is each word asking for?"
        K = X@W_K   → "What does each word offer?"
        V = X@W_V   → "What is the actual content?"
Step 4: scores = Q @ K.T / √d_k  → how related are words?
Step 5: weights = softmax(scores) → convert to probabilities (sum=1)
Step 6: output = weights @ V      → context-aware representation
```

## Key Insight

**Before attention:** each word only knows about itself.

**After attention:** each word contains information from ALL related words, weighted by relevance.

```
"The animal didn't cross the street because it was too tired."
                                               ↑
                              Attention tells us this refers to "animal."
```

## Run in Colab

Click `03_attention.ipynb` → Open in Colab → Run All

---
**Previous:** [02 NLP Basics](../02_nlp_basics/) | **Next:** [04 mini-GPT](../04_mini_gpt/)
