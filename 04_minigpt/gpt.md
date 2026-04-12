# 04 — mini-GPT: Text Generation from Scratch

> Everything from notebooks 01–03 combined into a working language model.

## What's Covered

| Notebook | Topic |
|----------|-------|
| `04_mini_gpt.ipynb` | Complete language model with text generation |

## Architecture

```
Input word
    ↓
Embedding Layer      (notebook 02 — word → vector)
    ↓
Self-Attention       (notebook 03 — understand context)
    ↓
Feed Forward         (notebook 01 — neural network)
    ↓
Output Layer         (scores for each word in vocabulary)
    ↓
Softmax → Sample     (pick next word)
```

## Results

```
After training:

  'i'    → 'love'     99.7%  ✓
  'deep' → 'learning' 99.5%  ✓
  'ai'   → 'is'       99.1%  ✓

Text generation:
  'deep' → "deep learning is amazing the"  ✓
  'ai'   → "ai is the future i"            ✓
```

## Key Concepts

**Training:** The model learns by predicting the next word and comparing to the correct answer. Loss goes down = model is learning.

**Temperature:** Controls how creative the output is.
- `0.5` = safe and predictable
- `0.8` = balanced
- `1.5` = creative and surprising

**Cross-Entropy Loss:** `-log(probability of correct word)` — lower is better.

## Comparison: Our Model vs Real LLMs

| | mini-GPT | GPT-2 | GPT-4 |
|--|---------|-------|-------|
| Vocabulary | 9 words | 50,257 | 100k+ |
| Embedding | 8 dims | 768 | 12,288 |
| Layers | 1 | 12 | 96+ |
| Parameters | ~200 | 124M | ~1.8T |

The **logic is identical** — only the scale is different.

## Run in Colab

Click `04_mini_gpt.ipynb` → Open in Colab → Run All

---
**Previous:** [03 Attention](../03_attention/) | **Next:** [05 HuggingFace](../05_huggingface/)
