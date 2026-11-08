# Deploy Guide — L_DEEPSPEC
**Tier:** TIER_4_INFERENCE_AGENTS | **Stack:** Python 3.11, Z3 (SMT solver), PAX 27B, AST, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, z3-solver 4.12+, PAX 27B weights, ast (stdlib).

## Environment
4GB RAM. CPU-only (Z3 is CPU-bound). GPU for PAX spec generation.

## AIOSS Integration
```bash
aioss init --module L_DEEPSPEC --output ./l_deepspec.aioss
aioss append --chain ./l_deepspec.aioss --payload ./output.bin --module L_DEEPSPEC
aioss verify --chain ./l_deepspec.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="L_DEEPSPEC",
    aioss_chain="./L_DEEPSPEC.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./L_DEEPSPEC.aioss --verbose
python -m L_DEEPSPEC.tests.smoke
```
