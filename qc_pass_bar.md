# QC Pass Bar (Ultra Cockpit)

The QC Pass Bar defines the minimum conditions required for an Ultra task correction to be considered complete, stable, and reviewer‑aligned.

## 1. All Fail‑to‑Pass Tests Added
Every requirement in instruction.md must have:
- at least one fail‑to‑pass test  
- correct naming  
- correct structure  
- correct assertions  

## 2. All Pass‑to‑Pass Tests Added
Regression coverage must include:
- valid inputs  
- valid outputs  
- edge‑case behavior  
- multi‑branch behavior  

## 3. ArgumentError Coverage
Invalid inputs must:
- raise ArgumentError  
- match instruction.md  
- match oracle behavior  

## 4. Instruction.md Rewritten
Instruction must be:
- deterministic  
- unambiguous  
- aligned with tests  
- aligned with oracle  

## 5. Packaging Integrity
- `.git` restored  
- file modes restored  
- no stray files  
- no placeholders  

## 6. Patch Integrity
- golden.patch applies cleanly  
- no unrelated hunks  
- no missing context  
- no duplicate hunks  

## 7. Config Integrity
- difficulty matches  
- no network_mode  
- no allowed_hosts  
- config.json matches tests  

## 8. No Leakage
- no benchmark leakage  
- no oracle leakage  
- no hidden hints  

## 9. Determinism
- all tests pass consistently  
- no flaky behavior  
- no nondeterministic branches  

## Purpose
The QC Pass Bar defines the minimum standard for a correct Ultra task correction.
