# Developer Cookbook — L_DEEPSPEC
**Stack:** Python 3.11, Z3 (SMT solver), PAX 27B, AST, AIOSS_FORMAT
**Domain:** DeepSpec: formal specification and verification for PAX 27B generated code and logic

## Generate and verify a formal spec
```python
from l_deepspec import DeepSpec

spec = DeepSpec(
    pax_model="./pax-27b-q4.gguf",
    aioss_chain="./deepspec.aioss"
)

# Natural language requirement -> Z3 spec -> verification
result = spec.verify(
    requirement="The AIOSS chain append function must be monotonically increasing in entry count",
    code_path="./aioss_format.py",
    function_name="AIOSSChain.append"
)

print(f"Verified: {result.verified}")
if result.counterexample:
    print(f"Counterexample: {result.counterexample}")
print(f"Z3 spec: {result.z3_spec}")
print(f"Chain: {result.chain_hash}")
```

## Verify safety property
```python
# Robotics: robot must stop before hitting obstacle
safety_result = spec.verify_safety_property(
    property="robot_velocity > 0 IMPLIES distance_to_obstacle > min_safe_distance",
    controller_code="./rover_controller.py"
)
```

## Batch verification
```python
specs = spec.batch_verify([
    ("aioss_monotonic", "append increases entry count"),
    ("chain_hash_unique", "no two entries share chain hash"),
    ("timestamp_ordered", "timestamps are strictly increasing")
])
for name, r in specs.items():
    print(f"{name}: {'VERIFIED' if r.verified else 'FAILED'}")
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
