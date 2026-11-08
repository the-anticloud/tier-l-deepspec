# Radon_Complexity_Lab_Results
**Project:** `L_DEEPSPEC` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `10`
- **average_complexity:** `{'grade': 'B', 'score': 5.274725274725275}`
- **complexity_grade:** `B`
- **complexity_score:** `5.274725274725275`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\L_DEEPSPEC\UPSTREAM\setup.py - A (100.00)
E:\fenta\Downloads\Th`

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\L_DEEPSPEC\UPSTREAM\eagle\modeling_eagle.py
    F 1002:0 generate_tree_buffers - D (27)
    F 625:0 generate_tree_buffers_for_eagle - C (19)
    F 1352:0 evaluate_posterior - C (18)
    M 352:4 EAGLEAttention.forward - C (15)
    M 747:4 EAGLEModel.forward - C (15)
    M 863:4 EAGLEModel.topK_genrate - C (13)
    F 1178:0 forward_with_tree_mask - C (12)
    M 1629:4 EAGLE.generate - C (12)
    C 1555:0 EAGLE - B (10)
    M 286:4 EAGLE_Config._rope_scaling_validation - B (9)
    F 1463:0 update_inference_inputs - B (7)
    C 175:0 EAGLE_Config - B (7)
    F 960:0 prepare_logits_processor - B (6)
    C 308:0 EAGLEAttention - B (6)
    M 714:4 EAGLEModel._prepare_decoder_attention_mask - B (6)
    M 1556:4 EAGLE.__init__ - B (6)
    F 1143:0 _prepare_decoder_attention_mask - A (5)
    M 458:4 EAGLEMLP.forward - A (5)
    C 695:0 EAGLEModel - A (5)
    M 332:4 EAGLEAttention._init_rope - A (4)
    C 447:0 EAGLEMLP - A (4)
    C 495:0 EAGLEDecoderLayer - A (4)
    M 506:4 EAGLEDecoderLayer.forward - A (4)
    C 584:0 Tree - A (4)
    C 149:0 EAGLEDynamicNTKScalingRotaryEmbedding - A (3)
    C 562:0 node - A (3)
    M 585:4 Tree.__init__ - A (3)
    M 602:4 Tree.num_node_wchild - A (3)
    M 609:4 Tree.get_node_wchild - A (3)
    M 616:4 Tree.indexnode - A (3)
    F 32:0 _make_causal_mask - A (2)
    F 50:0 _expand_mask - A (2)
    F 64:0 repeat_kv - A (2)
    F 1258:0 initialize_tree - A (2)
    F 1282:0 generate_candidates 
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_