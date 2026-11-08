# Reproduction - L_DEEPSPEC

```
cd E:/fenta/Downloads/The Anticloud/TIER_4_INFERENCE_AGENTS\L_DEEPSPEC\anticloud
python tools/run_bench.py --out BENCH.json --quiet   # pass 1: generate
python tools/run_bench.py --out BENCH.json --quiet   # pass 2: record
```
Exit code 0 means all 16 checks passed. Evidence: `04_Evidence/run_bench_output.txt`.
