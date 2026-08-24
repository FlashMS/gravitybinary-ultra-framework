# Eval Feedback Guide (Ultra Cockpit)

The Eval Feedback Guide defines how to interpret evaluation failures, classify them, and convert them into deterministic EC actions.

## Failure Categories

### 1. Packaging Failures
Symptoms:
- missing files  
- wrong file modes  
- broken patches  
- missing `.git`  
- stray files  

Action:
- restore packaging  
- restore file modes  
- restore `.git`  
- clean patches  

### 2. Test Runner Failures
Symptoms:
- tests not running  
- missing fixtures  
- missing test files  
- broken test.sh  

Action:
- restore tests  
- restore fixtures  
- restore test runner  

### 3. Fail‑to‑Pass Mismatches
Symptoms:
- missing fail‑to‑pass tests  
- incorrect assertions  
- incorrect naming  

Action:
- rebuild fail‑to‑pass  
- add missing tests  

### 4. Pass‑to‑Pass Mismatches
Symptoms:
- missing regression tests  
- incomplete coverage  

Action:
- add regression tests  
- ensure valid behavior coverage  

### 5. ArgumentError Mismatches
Symptoms:
- invalid inputs not raising errors  
- missing invalid‑input tests  

Action:
- add ArgumentError tests  
- align instruction  

### 6. Instruction Mismatches
Symptoms:
- unclear requirements  
- contradictions  
- missing behavior  

Action:
- rewrite instruction.md  
- align with oracle and tests  

### 7. Patch Mismatches
Symptoms:
- golden.patch does not apply  
- unrelated hunks  
- missing context  

Action:
- clean patch  
- restore base  
- reapply correctly  

### 8. Difficulty Mismatches
Symptoms:
- difficulty field does not match task  
- instruction complexity mismatch  

Action:
- correct difficulty  
- align config.json  

### 9. Determinism Failures
Symptoms:
- flaky tests  
- nondeterministic behavior  

Action:
- stabilize tests  
- ensure deterministic flow  

## Purpose
The Eval Feedback Guide converts evaluation failures into deterministic EC actions.
