# Ultra Control Panel (Nano Version)

The Ultra Control Panel defines the cockpit interface for deterministic EC execution. It provides a compressed, high‑clarity operational map for staying aligned with reviewer expectations and preventing drift.

## Verdict Lock
- FIXABLE
- Infra failures ≠ task defects
- Retry eval; flag UID if persistent

## Scope Lock
EC CAN FIX:
- instruction.md
- tests/
- tests.patch
- golden.patch
- task.toml (metadata only)
- packaging (.git, file modes)

EC CANNOT FIX:
- repo code
- library logic
- HTMLProofer internals
- environment/repo/**

## 13‑Point Checklist
1. Verdict correction  
2. Rebuild fail‑to‑pass  
3. Add new fail‑to‑pass  
4. ArgumentError coverage  
5. Populate pass‑to‑pass  
6. Restore .git  
7. Restore file modes  
8. Rewrite instruction.md  
9. Remove leakage  
10. Difficulty mismatch  
11. Patch cleanup  
12. Network settings  
13. Determinism

## Execution Rules
A. No repo edits  
B. No debugging failing tests  
C. No solving the PR  
D. Every action maps to checklist  
E. Every step reversible  
F. Keep running log

## Control Panel State
- Current Verdict: FIXABLE  
- Current Scope: tests/instruction/packaging only  
- Current Step: <fill>  
- Next Step: <fill>  
- Blocked On: <fill>  

## Drift Alerts
- touching repo code  
- debugging failing tests  
- fixing HTMLProofer  
- forgetting checklist  

## Structural Layer
Check:
- packaging integrity  
- test runner integrity  
- test existence  
- fixture existence  
- API existence  
- patch applicability  
- instruction/oracle alignment  
- repo/oracle alignment  
- base/oracle alignment  
- file modes  
- .git  
- config integrity  
