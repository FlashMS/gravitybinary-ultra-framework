# Ultra Engine (Deterministic Core)

The Ultra Engine defines the deterministic flow that powers the cockpit.  
It ensures that every EC action follows a stable, reversible, consequence‑aware sequence.

## Engine Cycle

### 1. Intake
- load instruction  
- load tests  
- load oracle  
- load patches  
- load config  

### 2. Structural Scan
- packaging integrity  
- test runner integrity  
- fixture existence  
- API existence  
- patch applicability  
- config alignment  

### 3. Alignment Scan
- instruction ↔ oracle  
- instruction ↔ tests  
- tests ↔ oracle  
- difficulty ↔ complexity  

### 4. Correction Cycle
- rebuild fail‑to‑pass  
- add regression tests  
- add ArgumentError tests  
- rewrite instruction  
- clean patches  
- restore packaging  

### 5. Determinism Scan
- run tests  
- verify stability  
- verify repeatability  

### 6. QC Pass Bar
- verify all 9 QC conditions  
- verify reviewer alignment  
- verify determinism  

## Purpose
The Ultra Engine is the deterministic core of the cockpit.  
It ensures stable, reversible, drift‑proof execution.
