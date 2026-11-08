# 3-Seed Simulation — L_DEEPSPEC

**Seeds:** `65769` · `97106` · `31305`

**Seed method:** `sha256("L_DEEPSPEC")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `L_DEEPSPEC`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 7.093 | 0.1737 | ±0.3405 |
| throughput_tokens_per_sec | 560.4333 | 23.7981 | ±46.6443 |
| p50_latency_ms | 50.15 | 2.6384 | ±5.1713 |
| p99_latency_ms | 99.5 | 6.4058 | ±12.5554 |
| ttft_ms | 23.4533 | 1.2378 | ±2.4261 |
| mmlu_proxy | 0.7552 | 0.0304 | ±0.0596 |
| hellaswag_proxy | 0.7897 | 0.0254 | ±0.0498 |
| truthfulqa_proxy | 0.5519 | 0.0204 | ±0.04 |
| arc_proxy | 0.7075 | 0.0182 | ±0.0357 |
| complexity_cyclomatic | 4.4467 | 0.2894 | ±0.5672 |
| maintainability_index | 66.5733 | 4.1201 | ±8.0754 |
| security_issues_high | 1.0 | 0.8165 | ±1.6003 |
| dependency_freshness_pct | 82.0333 | 2.2647 | ±4.4388 |
| test_coverage_pct | 59.2 | 3.7532 | ±7.3563 |
| doc_coverage_pct | 62.8 | 6.4689 | ±12.679 |
| memory_mb | 596.1333 | 35.5439 | ±69.666 |
| gpu_util_pct | 65.0 | 5.0259 | ±9.8508 |
| openssf_score | 6.0733 | 0.531 | ±1.0408 |
| eu_ai_act_compliance_pct | 83.3667 | 0.7134 | ±1.3983 |
| slsa_level | 1.3333 | 0.4714 | ±0.9239 |

## Per-Seed Raw Results

| Metric | Seed 65769 | Seed 97106 | Seed 31305 |
|--------|------------|------------|------------|
| trl_score | 7.2 | 7.231 | 6.848 |
| throughput_tokens_per_sec | 593.6 | 538.9 | 548.8 |
| p50_latency_ms | 46.44 | 51.66 | 52.35 |
| p99_latency_ms | 93.47 | 96.66 | 108.37 |
| ttft_ms | 22.08 | 25.08 | 23.2 |
| mmlu_proxy | 0.7767 | 0.7766 | 0.7122 |
| hellaswag_proxy | 0.7929 | 0.7572 | 0.8191 |
| truthfulqa_proxy | 0.5787 | 0.5479 | 0.5292 |
| arc_proxy | 0.7328 | 0.6991 | 0.6906 |
| complexity_cyclomatic | 4.69 | 4.61 | 4.04 |
| maintainability_index | 63.63 | 72.4 | 63.69 |
| security_issues_high | 0 | 2 | 1 |
| dependency_freshness_pct | 79.7 | 85.1 | 81.3 |
| test_coverage_pct | 56.8 | 56.3 | 64.5 |
| doc_coverage_pct | 56.0 | 60.9 | 71.5 |
| memory_mb | 594.2 | 553.6 | 640.6 |
| gpu_util_pct | 71.0 | 65.3 | 58.7 |
| openssf_score | 5.5 | 6.78 | 5.94 |
| eu_ai_act_compliance_pct | 82.4 | 83.6 | 84.1 |
| slsa_level | 1 | 1 | 2 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._