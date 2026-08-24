# Reviewer Checklist (13‑Point Ultra Standard)

This checklist defines the 13 mandatory reviewer alignment points for Ultra task correction.  
Every EC action must map to one of these items.

## 1. Verdict Correction
Ensure the verdict is FIXABLE unless explicitly proven otherwise.

## 2. Rebuild Fail‑to‑Pass
Reconstruct the fail‑to‑pass list based on instruction requirements.

## 3. Add New Fail‑to‑Pass
Add missing tests for requirements not covered.

## 4. ArgumentError Coverage
Ensure invalid inputs trigger ArgumentError where required.

## 5. Populate Pass‑to‑Pass
Add regression tests for valid behavior.

## 6. Restore .git
Ensure `.git` directory exists and is correct.

## 7. Restore File Modes
Executable files: 0755  
Non‑executables: 0644

## 8. Rewrite Instruction.md
Fix clarity, determinism, and requirement mapping.

## 9. Remove Leakage
No benchmark leakage, no oracle leakage, no hidden hints.

## 10. Difficulty Mismatch
Ensure difficulty fields match task expectations.

## 11. Patch Cleanup
Remove unrelated changes from patches.

## 12. Network Settings
Remove network_mode, allowed_hosts, and similar fields.

## 13. Determinism
Ensure deterministic behavior across all runs.

## Purpose
The 13‑point checklist is the EC’s alignment map for reviewer expectations.
