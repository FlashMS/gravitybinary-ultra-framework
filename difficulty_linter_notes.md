# Difficulty Linter Notes (Ultra Cockpit)

The Difficulty Linter ensures that the task’s difficulty metadata matches the actual reviewer expectations and test complexity.

## Difficulty Signals

### 1. Instruction Complexity
- Number of requirements  
- Ambiguity level  
- Edge‑case density  

### 2. Test Complexity
- Number of fail‑to‑pass tests  
- Number of pass‑to‑pass tests  
- ArgumentError coverage  
- Regression depth  

### 3. Patch Complexity
- Size of golden patch  
- Number of hunks  
- Number of context lines  
- Presence of multi‑file changes  

### 4. Oracle Complexity
- Number of branches  
- Number of validations  
- Number of fixtures  
- Number of API calls  

### 5. Reviewer Expectations
- Determinism  
- Clarity  
- No leakage  
- No contradictions  

## Difficulty Mismatch Alerts
- Instruction says “easy” but tests require multi‑branch logic  
- Instruction says “medium” but oracle is trivial  
- Instruction says “hard” but patch is tiny  
- Tests require behavior not described in instruction  
- Instruction describes behavior not tested  

## Purpose
The Difficulty Linter prevents misalignment between instruction, tests, oracle, and reviewer expectations.
