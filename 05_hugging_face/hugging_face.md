# 05 — HuggingFace & Real GPT-2

> From building from scratch to using production-ready models.

## What's Covered

| Notebook | Topic |
|----------|-------|
| `05_huggingface.ipynb` | GPT-2 pipeline, tokenizer, fine-tuning, save/load |

## Everything Connects to Previous Notebooks

| Concept | Our code (notebooks 01–04) | HuggingFace |
|---------|---------------------------|-------------|
| Tokenize | `word_to_idx['love'] = 7` | `tokenizer.encode('love') = [1842]` |
| Decode | `idx_to_word[7]` | `tokenizer.decode([1842])` |
| Forward pass | `forward(word_idx)` | `model(**inputs)` |
| Generate | our loop in notebook 04 | `model.generate()` |
| Fine-tune | training loop notebook 01 | same loop + PyTorch |

**The logic is identical — only the scale is different.**

## Parts

1. **Pipeline** — simplest way, 3 lines of code
2. **Tokenizer** — same as notebook 02, with 50,257 words
3. **Model forward pass** — same as notebook 04, with 12 transformer layers
4. **Generation strategies** — greedy, temperature, top-k, top-p
5. **Fine-tuning** — adapt GPT-2 to AI/ML domain
6. **Save and load** — persist your fine-tuned model

## Quick Start

```python
from transformers import pipeline

generator = pipeline('text-generation', model='gpt2')
result = generator('Deep learning is', max_new_tokens=20)
print(result[0]['generated_text'])
```

## GPT-2 vs Our mini-GPT

| | mini-GPT | GPT-2 |
|--|---------|-------|
| Vocabulary | 9 | 50,257 |
| Embedding dim | 8 | 768 |
| Layers | 1 | 12 |
| Parameters | ~200 | 124M |

## Run in Colab

Click `05_huggingface.ipynb` → Open in Colab → Run All

*Note: First run downloads GPT-2 (~500MB), cached after that.*

---
**Previous:** [04 mini-GPT](../04_mini_gpt/) | **Next:** [06 Finance NLP](../06_finance_nlp/)
