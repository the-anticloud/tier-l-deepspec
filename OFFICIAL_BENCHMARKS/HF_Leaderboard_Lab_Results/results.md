# HF_Leaderboard_Lab_Results

**Project:** `L_DEEPSPEC`  
**Tier:** `TIER_4_INFERENCE_AGENTS`  
**Slug:** `SafeAILab/EAGLE`  
**Commit:** `cb7e0841fe0c`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **49.4 ms** |
| Min latency | 43.02 ms |
| Max latency | 53.94 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **37** |
| Tokenization latency | 1.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5863 |
| Classification latency | 75.77 ms |
| Status | **PASS** |

**Input text tokenized:**
```
L_DEEPSPEC (SafeAILab/EAGLE) — 90 files, 22131 source lines, licence Apache-2.0, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'l', '_', 'deep', '##sp', '##ec', '(', 'safe', '##ail', '##ab', '/', 'eagle', ')', '—', '90', 'files', ',', '221', '##31', 'source']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_