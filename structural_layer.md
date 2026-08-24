# Structural Layer (Ultra Cockpit)

The Structural Layer defines the physical integrity checks that the agentic judge does not perform. It ensures that every Ultra task bundle is complete, valid, and runnable.

## Structural Checkpoints

### 1. Packaging Integrity
- No stray files  
- No duplicated files  
- No placeholder files  
- No broken specs  
- No syntax errors  
- No task-authoring residue  
- No agent-visible patches inside repo  

### 2. Test Runner Integrity
- `tests/test.sh` must run real tests  
- `tests/tests.patch` must apply real test files  
- No placeholders  
- No empty patches  

### 3. Test Existence
- Every fail-to-pass test must exist  
- Every pass-to-pass test must exist  
- Every test name in config.json must map to a real RSpec example  

### 4. Fixture Existence
- Every referenced fixture must exist  
- No phantom fixture paths  
- No missing HTML files  

### 5. API Existence
- Every method used in tests must exist  
- No calls to nonexistent APIs  

### 6. Patch Applicability
- Golden patch must apply cleanly  
- No base/patch mismatches  
- No duplicate hunks  
- No missing context  

### 7. Instruction/Oracle Alignment
- Instruction must allow what the oracle does  
- Oracle must satisfy instruction  
- No contradictions  

### 8. Repo/Oracle Alignment
- Oracle must not modify forbidden files  
- Oracle must not rely on missing APIs  
- Oracle must not rely on missing fixtures  

### 9. Base/Oracle Alignment
- Base must not already contain solved state  
- Oracle must not reapply existing changes  

### 10. File Mode Integrity
- Executables: 0755  
- Non-executables: 0644  
- No 777 repacks  

### 11. .git Integrity
- `.git` must exist  
- HEAD must match base commit  
- `git apply --3way` must work  

### 12. Config Integrity
- Difficulty fields must match  
- Network_mode removed  
- Allowed_hosts removed  
- Config.json must match tests  

## Purpose
The Structural Layer catches everything the agentic judge cannot.
